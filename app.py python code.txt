import streamlit as st
import pandas as pd

# Page Configuration
st.set_page_config(
    page_title="Smart Retail & Inventory Intelligence",
    page_icon="📦",
    layout="wide"
)

# App Title & Subtitle
st.title("📦 Smart Retail & Inventory Intelligence Platform")
st.markdown("### *Dynamic Inventory Optimization, Safety Stock, and Replenishment Dashboard*")
st.markdown("---")

# Load Data
@st.cache_data
def load_data():
    return pd.read_excel('inventory_optimization_data.xlsx')

df = load_data()

# Sidebar Filters
st.sidebar.header("Control Panel")
selected_status = st.sidebar.selectbox(
    "Filter by Inventory Status",
    options=["All"] + list(df['Inventory_Status'].unique())
)

# Filter Data based on sidebar selection
if selected_status != "All":
    filtered_df = df[df['Inventory_Status'] == selected_status]
else:
    filtered_df = df

# Top Row: KPI Metrics
col1, col2, col3 = st.columns(3)

total_skus = len(filtered_df)
skus_at_risk = len(filtered_df[filtered_df['Inventory_Status'].isin(["Critical Stockout Risk", "Reorder Required"])])
total_order_qty = filtered_df['Recommended_Order_Qty'].sum()

col1.metric("Total SKUs Monitored", total_skus)
col2.metric("SKUs At Risk / Needing Reorder", skus_at_risk, delta_color="inverse")
col3.metric("Total Recommended Order Qty", f"{total_order_qty:,.0f} units")

st.markdown("---")

# Main Data Table Display
st.subheader("📋 Item-Level Inventory Control Table")
st.dataframe(filtered_df, use_container_width=True)

# Footer Note
st.markdown("---")
st.markdown("*Platform Engine: Python, Pandas, NumPy & Streamlit Cloud Deployment.*")
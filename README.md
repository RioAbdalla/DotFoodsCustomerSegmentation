# Dot Foods Sales Dashboard & Customer Segmentation

## 📌 Project Overview
This project was developed for **Dot Foods**, the largest food redistributor in North America, to design a **Power BI-based 360° sales performance and customer segmentation dashboard**.  

The goal is to provide sales and logistics teams with **real-time insights into customer behavior, shipment efficiency, and operational performance**. By integrating clustering analysis with interactive dashboards, the project supports **strategic decision-making, resource allocation, and customer engagement**.

---

## 📊 Methodology
1. **Customer Segmentation (Machine Learning)**  
   - Applied **K-Means clustering** on ~92K customer records.  
   - Preprocessed data: removed invalid values, capped outliers (IQR method), log-transformed skewed features.  
   - Selected 5 representative features for clustering.  
   - Identified **4 distinct customer clusters**, validated using PCA.  

   **Cluster Profiles:**  
   - **Cluster 0**: Small-to-Medium Volume Clients, fast loading, large single orders.  
   - **Cluster 1**: Medium-to-High Volume Clients, stable orders, moderate vehicle distribution.  
   - **Cluster 2**: Low-Volume, infrequent clients, small orders, fast turnaround.  
   - **Cluster 3**: Strategic Clients, very high volume & order frequency, complex loading.  

2. **Dashboard Development (Power BI)**  
   - Built dynamic dashboards with multiple perspectives:  
     - **Period Dashboard**: Tracks KPIs (dock time, PO count, cases/load, item spread) over 13 time periods.  
     - **Tier Dashboard**: Benchmarks performance across tiers (Tier I, II, Corporate, etc.).  
     - **Company Dashboard**: Provides customer-specific KPIs for operational efficiency.  
   - Visuals highlight top/bottom performers, identify bottlenecks, and support benchmarking.  

3. **Architecture**  
   - Data Source: MySQL, MongoDB, APIs, Excel, S3  
   - Data Ingestion: Apache Airflow  
   - Data Processing: Snowpipe  
   - Storage: Data Lakehouse (Azure, Hive, Datamart)  
   - Advanced Analytics: Snowflake ML, Amazon SageMaker  
   - Consumption: Power BI, Tableau, Excel  

---

## 📈 Key Insights
- Dock time, PO count, and SKU diversity are **critical drivers** of efficiency.  
- **Tier-based benchmarking** identifies top/bottom performers for resource prioritization.  
- Customer clusters reveal clear **strategic vs. low-priority clients**, enabling tailored engagement strategies.  
- Power BI dashboards provide **real-time slicing** by company, customer type, tier, region, and period.  

---

## 🛠️ Tech Stack
- **Data Science**: Python (`pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`)  
- **Machine Learning**: K-Means clustering, PCA  
- **Visualization**: Power BI, Tableau  
- **Architecture**: Snowflake ML, SageMaker, Airflow, Snowpipe, Azure Data Lakehouse  

---

## 📂 Repository Structure
```
├── cluster-analysis.ipynb                 # Notebook for K-Means clustering & PCA
├── clean_with_clusters.csv                # Preprocessed dataset with clusters
├── Architecture (2).jpg                   # System architecture diagram
├── FinalEdit1.pptx                        # Presentation slides
└── README.md                              # Project documentation
```

---

## 🚀 How to Run
1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/dotfoods-dashboard.git
   cd dotfoods-dashboard
   ```
2. Install Python dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```
3. Run clustering analysis:
   ```bash
   jupyter notebook cluster-analysis.ipynb
   ```
4. Explore dashboards in Power BI (PBIX files to be added).

---

## 🤝 Contributors
- Damario Abdalla
- Haiyang Yuan
- Jiahe Li
- Ziyuan Wang
- Puyue Zou
- Daniel McGhee
- Mrinali Dole

---

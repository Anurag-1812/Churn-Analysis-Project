# 📊 Churn Analysis Project

[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Anurag-1812/Churn-Analysis-Project)
[![Data Analysis](https://img.shields.io/badge/Data_Analysis-4285F4?style=for-the-badge&logo=google-analytics&logoColor=white)](#)

> **Comprehensive customer churn analysis dashboard built with Power BI, featuring predictive insights and detailed customer segmentation**

![Dashboard Preview](https://github.com/Anurag-1812/Churn-Analysis-Project/blob/main/Power%20BI%20Dashboard/Dashboard%20Summary.png)

---

## 🎯 Project Overview

This project delivers a complete customer churn analysis solution using Power BI, providing actionable insights into customer retention patterns. The dashboard identifies key factors contributing to customer churn and enables data-driven decision making for customer retention strategies.

### 🔍 Key Insights at a Glance
- **6,418** Total Customers analyzed
- **26.99%** Overall Churn Rate
- **1,732** Customers lost to churn
- **411** New customer acquisitions

---

## 📁 Repository Structure

```
Churn-Analysis-Project/
├── 📸 Background/
│   ├── Prediction.PNG
│   └── Summary.PNG
├── 📊 Data/
│   └── Customer_Data.csv
├── 🖼️ Images/
│   ├── Ico_Gender.png
│   └── Ico_Gender2.png
├── 📈 Power BI Dashboard/
│   ├── Churn Analysis.pbix
│   └── Dashboard Summary.png
├── 📝 Queries & DAX/
│   ├── Power Query Transformations & Measures - Anurag.docx
│   └── SQL Queries - Anurag.docx
└── 📖 README.md
```

---

## 🚀 Features

### 📊 Dashboard Components

#### **Summary Page**
- **KPI Cards**: Total customers, churn rate, new joiners
- **Geographic Analysis**: State-wise churn distribution
- **Service Analysis**: Internet service type impact on churn
- **Demographic Insights**: Age group and gender-based analysis
- **Contract Analysis**: Monthly vs yearly contract performance

#### **Churn Prediction Page**
- **Predictive Model Integration**: ML-based churn predictions
- **Risk Segmentation**: Customer risk categorization
- **Retention Strategies**: Targeted intervention recommendations

### 🔧 Technical Features

#### **Power Query Transformations**
- ✅ **Churn Status Binary Encoding**: Automated 0/1 conversion
- ✅ **Monthly Charge Categorization**: Smart binning (<20, 20-50, 50-100, >100)
- ✅ **Age Group Mapping**: Demographic segmentation with sorting
- ✅ **Tenure Group Classification**: Customer lifecycle stages
- ✅ **Service Unpivoting**: Normalized service usage analysis

#### **DAX Measures**
```dax
Total Customers = COUNT(prod_Churn[Customer_ID])
New Joiners = CALCULATE(COUNT(prod_Churn[Customer_ID]), prod_Churn[Customer_Status] = "Joined")
Total Churn = SUM(prod_Churn[Churn Status])
Churn Rate = [Total Churn] / [Total Customers]
```

---

## 📈 Key Performance Indicators

| Metric | Value | Insight |
|--------|--------|---------|
| **Total Customers** | 6,418 | Complete customer base analysis |
| **Churn Rate** | 26.99% | Above industry average - requires attention |
| **New Joiners** | 411 | Customer acquisition tracking |
| **Gender Distribution** | 64.1% Female, 35.9% Male | Female customers show higher churn |
| **High-Risk Services** | Fiber Optic (41.10%) | Service quality improvement needed |
| **Contract Performance** | Month-to-Month (46.53%) | Short-term contracts correlate with churn |

---

## 🎨 Visual Highlights

### 🌍 Geographic Analysis
- **Top Churn States**: Jammu (57.19%), Assam (38.13%), Jharkhand (34.51%)
- **Interactive State Filtering**: Drill-down capability for regional insights

### 📱 Service Analysis
- **Internet Service Impact**: Fiber Optic customers show highest churn (41.10%)
- **Service-wise Breakdown**: Comprehensive analysis across all service offerings
- **Usage Patterns**: Correlation between service usage and retention

### 👥 Demographic Insights
- **Age Group Analysis**: 36-50 age group shows highest churn (31.55%)
- **Payment Method Impact**: Mailed invoices correlate with higher churn (37.82%)
- **Contract Duration**: Month-to-month contracts show 46.53% churn rate

---

## 🛠️ Getting Started

### Prerequisites
- Power BI Desktop (Latest Version)
- Basic understanding of DAX and Power Query

### Installation Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Anurag-1812/Churn-Analysis-Project.git
   cd Churn-Analysis-Project
   ```

2. **Open Power BI Dashboard**
   - Navigate to `Power BI Dashboard/`
   - Open `Churn Analysis.pbix` in Power BI Desktop

3. **Data Refresh** (if needed)
   - Ensure `Customer_Data.csv` is in the correct path
   - Refresh data model in Power BI

---

## 🔍 Deep Dive Analysis

### Churn Drivers Identified

#### **High-Risk Segments**
1. **Fiber Optic Customers**: 41.10% churn rate
2. **Month-to-Month Contracts**: 46.53% churn rate
3. **Mailed Invoice Users**: 37.82% churn rate
4. **Short Tenure Customers**: < 6 months show highest churn

#### **Retention Opportunities**
- **Contract Migration**: Convert month-to-month to annual contracts
- **Service Quality**: Address fiber optic service issues
- **Payment Modernization**: Migrate from mailed to digital invoices
- **Early Intervention**: Target customers in first 6 months

### Business Impact

| Strategy | Potential Impact | Implementation Priority |
|----------|------------------|------------------------|
| **Contract Incentives** | 15-20% churn reduction | 🔴 High |
| **Service Quality Improvement** | 10-15% churn reduction | 🔴 High |
| **Payment Method Migration** | 8-12% churn reduction | 🟡 Medium |
| **Early Intervention Program** | 20-25% churn reduction | 🔴 High |

---

## 📚 Documentation

### Available Resources
- **[Power Query Transformations](Queries%20&%20DAX/Power%20Query%20Transformations%20&%20Measures%20-%20Anurag.docx)**: Complete transformation logic
- **[SQL Queries](Queries%20&%20DAX/SQL%20Queries%20-%20Anurag.docx)**: Data preparation queries
- **Dashboard Screenshots**: Visual references in `Background/` folder

### Data Dictionary

| Column | Description | Type |
|--------|-------------|------|
| Customer_ID | Unique customer identifier | Text |
| Customer_Status | Current status (Active/Churned/Joined) | Text |
| Age | Customer age | Number |
| Monthly_Charge | Monthly subscription fee | Currency |
| Tenure_in_Months | Customer relationship duration | Number |
| Various Services | Service subscription status | Boolean |

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Commit changes**: `git commit -m 'Add amazing feature'`
4. **Push to branch**: `git push origin feature/amazing-feature`
5. **Open a Pull Request**

### Contribution Areas
- 📊 Additional visualizations
- 🔍 Enhanced DAX measures
- 📈 Predictive model improvements
- 📝 Documentation enhancements

---

## 📞 Contact & Support

**Author**: Anurag  
**Repository**: [Churn-Analysis-Project](https://github.com/Anurag-1812/Churn-Analysis-Project)

### Questions or Issues?
- 📧 Create an issue on GitHub
- 💬 Start a discussion in the repository
- ⭐ Star the repo if you find it useful!

---

## 🏆 Acknowledgments

- Power BI Community for visualization inspirations
- Data analytics best practices from industry leaders
- Open source community for continuous learning

---

<div align="center">

**Made with ❤️ and Power BI**

[![GitHub Stars](https://img.shields.io/github/stars/Anurag-1812/Churn-Analysis-Project?style=social)](https://github.com/Anurag-1812/Churn-Analysis-Project/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Anurag-1812/Churn-Analysis-Project?style=social)](https://github.com/Anurag-1812/Churn-Analysis-Project/network/members)

</div>

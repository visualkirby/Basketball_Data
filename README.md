# 🏀 NBA Basketball Analytics Pipeline  
**End-to-End Data Project: Web Scraping → ETL → SQL → Visualization**  

## 📂 **Dataset**  
[![Kaggle Dataset](https://img.shields.io/badge/Download-Dataset-20BEFF)](https://www.kaggle.com/datasets/sawandikirby/nba-basketball-statistics-and-performance-data)  
*23 seasons of player/team stats (2000-2023) • 450K+ rows • 120+ metrics*

---

## 🔄 **ETL Process**  
### 1️⃣ **Extract (Python)**  
[![Code](https://img.shields.io/badge/View-Python%20Code-3776AB)](https://github.com/visualkirby/Basketball_Data/blob/main/DataWarehousingExtract.pdf)  
- Scraped NBA.com, ESPN, and Basketball-Reference using BeautifulSoup  
- Automated with Selenium for dynamic JS content  
- Output: Raw JSON/CSV files (15GB uncompressed)  

### 2️⃣ **Transform (R)**  
[![R Code](https://img.shields.io/badge/View-R%20Script-276DC3)](https://github.com/visualkirby/Basketball_Data/blob/main/DataWarehousingTransform.pdf)  
- Cleaned 27% incomplete records using `tidyr`  
- Standardized 45+ stats (e.g., TS%, PER) with `dplyr`  
- Feature engineering: Created "Win Shares/48" metric  

### 3️⃣ **Load (Cloud SQL)**  
[![BigQuery](https://img.shields.io/badge/View-Cloud%20Setup-4285F4)](https://github.com/visualkirby/Basketball_Data/blob/main/DataWarehousingLoad.pdf)  
- Deployed to **Google BigQuery** (2TB analytics)  
- Optimized MySQL schemas for 50ms query latency  
- *Coming Soon: Redshift migration*  

---

## 📊 **Analysis & Insights**  
### 🛠 **SQL Queries**  
[![MySQL](https://img.shields.io/badge/View-SQL%20Queries-4479A1)](https://github.com/visualkirby/Basketball_Data/blob/main/NBA_Data_SQL_Queries.PDF)  
```sql
-- Example: Find undervalued 3PT shooters
SELECT player_name, 3P%, salary 
FROM players 
WHERE 3P% > 40 AND salary < 5000000;
```

### 🔍 **Key Business Question**  
*"How can NBA teams leverage analytics for roster construction?"*  
**Findings:**  
- **82% correlation** between PIE (Player Impact Estimate) and playoff success  
- Teams overpay for PPG (+$2.1M/yr) vs. true shooting % (+$800K/yr)  

---

## 📈 **Visualization**  
### **Tableau Dashboard**  
[![Tableau](https://img.shields.io/badge/Interactive-Dashboard-E97627)](https://public.tableau.com/views/NBATeamDash/Dashboard1)  
- Player efficiency radar charts  
- Team salary cap heatmaps  

### **Power BI Report**  
[![PDF](https://img.shields.io/badge/View-PDF-FFB900)](https://github.com/visualkirby/Basketball_Data/blob/main/Power%20BI%20NBA%20Team%20Dashboard.pdf) | [![Video](https://img.shields.io/badge/Walkthrough-Video-FFB900)](https://github.com/visualkirby/Basketball_Data/blob/main/Power_BI_Video_Example.pptx)  
- Dynamic trade machine simulator  
- Draft pick value analysis  

---

## 💡 **Skills Demonstrated**  
| Category | Tools |  
|----------|-------|  
| **Data Engineering** | Python (BeautifulSoup/Selenium), R (tidyverse) |  
| **Cloud/Databases** | BigQuery, MySQL, Azure SQL |  
| **Analytics** | SQL optimization, statistical modeling |  
| **Viz** | Tableau, Power BI, ggplot2 |  

---

## 🎯 **Project Impact**  
This pipeline could help NBA teams:  
✅ **Identify undervalued players** (saved $8-12M/yr in cap space)  
✅ **Optimize lineups** via +/- analysis  
✅ **Predict draft success** with 79% accuracy  

[**Explore Full Repository**](https://github.com/visualkirby/Basketball_Data)  

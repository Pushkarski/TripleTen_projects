# 🏙️ Airbnb Market Analysis - Advanced Spreadsheets Project

This project analyzes the Manhattan Airbnb market to determine which neighborhoods and property sizes are most attractive for vacation rentals, and which listings generate the highest revenue.
This project was completed as part of the TripleTen Data Analysis Bootcamp.

---

## 🎯 Project Objectives
- Identify top neighborhoods for short-term rentals  
- Determine most in-demand property sizes  
- Estimate revenue for top listings  
- Provide investment recommendations  

---

## 📊 Key Insights
- **Top neighborhoods:** Lower East Side, Hell’s Kitchen, Harlem  
- **Most popular property size:** 1-bedroom (except Midtown → studios)  
- **Top listing:** ID **49946551**, highest 30-day and annualized revenue  
- **Estimated annual revenue of all recommended listings:** **$5.47M**

**Recommendation:**  
Focus on **1-bedroom units** in Lower East Side, Hell’s Kitchen, and Harlem.  
For Midtown, **studios** perform best.

---

## 🧹 Data Preparation
- Standardized neighborhood names (`PROPER()`)  
- Cleaned missing bedroom values (treated as studios = `0`)  
- Added helper fields:
  - `top_listing` - marks listings matching optimal criteria  
  - `revenue_earned` - 30-day revenue per listing (via `SUMIF()`)  

---

## 🔧 Tools & Techniques
- Google Sheets / Excel  
- Pivot tables  
- Formulas: `IF()`, `AND()`, `OR()`, `SUMIF()`, `PROPER()`  
- Bar charts and summary tables  

---

## 📂 Project Structure
```
01_advanced_spreadsheets_airbnb/
│
├── README.md
└── Airbnb_Analysis.xlsx
```
---

## 📝 Summary
Data shows strong demand for 1-bedroom properties in key Manhattan neighborhoods.  
This insight can guide investors toward listings with the highest revenue potential.

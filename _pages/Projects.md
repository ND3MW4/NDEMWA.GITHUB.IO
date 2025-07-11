---
layout: single
title: "Projects"
permalink: /projects/
author_profile: true
---

# 🛠 Projects

Here’s a selection of projects showcasing my work in **Data Science & AI**

---

## 🧠 Data Science & AI Projects

### 📌 Web Scraping
---
layout: single
title: "📊 Web Scraping Project: Hockey Teams Data"
permalink: /projects/webscraping/
author_profile: true
---

# 📊 **Web Scraping Project: Hockey Teams Dataset**

**By Denis Ndemwa (CS-DA01-25056)**  
📅 **Date:** May 14, 2025

> 👉 [Colab Notebook 📓](https://colab.research.google.com/drive/1rSLb2pOrwiHzXmmwtShroFnm0r1Xbe7Z?authuser=0#scrollTo=reowsSH7GmF2)

---

## ✅ **Project Objectives**
1. Introduce web scraping and explain its importance.
2. Choose a suitable target website to scrape data from.
3. Build and run a Python script to extract, clean, and save data for analysis.

---

## 🌐 **Target Website**
We scraped data from:
> [https://www.scrapethissite.com/pages/forms/?page_num=16](https://www.scrapethissite.com/pages/forms/?page_num=16)

✅ Reason for choosing this site:
- Publicly available structured data in HTML tables.
- Great practice for table parsing and automation.
- Ethical scraping (no login / no violation of terms).

---

## 🧰 **Tools & Libraries**
- **Python**: Programming language
- **Requests**: Fetch HTML pages
- **BeautifulSoup**: Parse HTML content
- **Pandas**: Data analysis & CSV export

---

## 🧩 **Project Workflow**
**1️⃣ Load libraries & fetch HTML**
```python
import requests
from bs4 import BeautifulSoup
import pandas as pd

url = 'https://www.scrapethissite.com/pages/forms/?page_num=16'
response = requests.get(url)
soup = BeautifulSoup(response.text, 'html.parser')


---

### 📌 Data Wrangling Project
Cleaned, transformed, and prepared real-world datasets to make them ready for modeling.
- **Tools used:** Python (Pandas, NumPy)

---

### 📌 Exploratory Data Analysis (EDA)
Visualized key patterns and trends to generate actionable insights.
- **Tools used:** Python (Matplotlib, Seaborn), Jupyter Notebook

---

### 📌 Business Intelligence with Power BI
Created interactive dashboards and reports to help stakeholders track KPIs.
- **Tools used:** Power BI

---

### 📌 Data Visualization using Tableau
Designed compelling visual stories from complex datasets.
- **Tools used:** Tableau

---

### 📌 Linear Regression Model
Built and evaluated a regression model to predict numerical outcomes.
- **Tools used:** scikit-learn, Python

---

### 📌 Classification Models
Developed machine learning classifiers to automate decision-making tasks.
- **Tools used:** scikit-learn, Python



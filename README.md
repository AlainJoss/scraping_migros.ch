# 🛒 Project SMO: Scraping Migros Online

![Status](https://img.shields.io/badge/status-in%20progress-yellow)
![License](https://img.shields.io/badge/license-MIT-blue)

## 📖 Table of Contents

- [Overview](#-overview)
- [Motivation](#-motivation)
- [Features](#-features)
- [Data Collected](#-data-collected)
- [Project Structure](#-project-structure)
- [Tools](#️-tools)
- [Progress](#-progress)
- [Disclaimer](#-disclaimer)

## 📖 Overview

**Project SMO** is a web scraping project that aims to collect data from the Migros online store.

## 🎯 Motivation

The goals of this project are:
- **Generate a clean dataset** for others to use in their own projects.
- **Analyze** the food we buy and consume from both a price and nutritional perspective.
- **Gather insights** to make informed dietary decisions.

## 🌟 Features

- Scrapes detailed product information including prices, nutritional values, and categories.
- Cleans and organizes data into a structured format.
- Provides insights into consumer products for data analysis projects.

## 📊 Data Collected

For each product, the following information (75 attributes) is collected:
- 🏷️ **Product Name**
- 🔗 **URL**
- 🗂️ **Category**
- 🗃️ **Subcategory**
- 💰 **Price**
- 💲 **Price per unit**
- 📏 **Price unit**
- 📦 **Quantity**
- ⚖️ **Weight per unit**
- 📏 **Weight unit**
- 🥦 **Nutritional Values**:
  - 🔋 **Energy kJ**
  - 🔥 **Energy kcal**
  - 🧈 **Fat (g)**
  - 🧊 **of which saturates (g)**
  - 🍞 **Carbohydrate (g)**
  - 🍬 **of which sugars (g)**
  - 🌾 **Fibre (g)**
  - 💪 **Protein (g)**
  - 🧂 **Salt**
  - ...

**Dataset Summary:**

- **Number of rows:** 9,602 (9,545 unique products)
- **Number of attributes:** 75
- **Anomalies:** The price per unit is not always correct due to incorrect information provided on the website.

## 📂 Project Structure

```
Project-SMO/
├── data/
│   └── products.csv
├── scripts/
│   ├── scraper.py
│   └── data_cleaning.py
├── images/
│   └── sample_product_page.png
├── LICENSE
├── README.md
└── requirements.txt
```

## 🛠️ Tools

I use the following libraries and tools:
- **Web Scraping**: `selenium` and `beautifulsoup4` 
- **Data Processing**: `pandas` and `numpy`
- **Data Storage**: CSV 

## 🚧 Progress

The project is currently **in progress**. So far I've beein able to scrape the data and clean it. The next steps are to analyze the data and gather insights.


## 📝 Disclaimer

This project is for educational purposes only. Please respect the website's terms of service and robots.txt file. The author is not responsible for any misuse of this code.
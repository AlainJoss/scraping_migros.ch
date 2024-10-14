# 🛒 Project SMO: Scraping Migros Online

![Status](https://img.shields.io/badge/status-in%20progress-yellow)

## 📖 Table of Contents

- [Overview](#-overview)
- [Motivation](#-motivation)
- [Data Collected](#-data-collected)
- [Scraping Process](#-scraping-process)
- [Tools](#️-tools)
- [Limitations](#️-limitations)
- [Next Steps](#️-next-steps)
- [Disclaimer](#-disclaimer)

## 📖 Overview

**Project SMO** is a web scraping project in which I collect product information from [Migros Online](https://www.migros.ch/en). 

The data was collected on **2024-10-14**.

## 🎯 Motivation

The goals of this project are:
- **Generate a clean dataset** for others to use in their own projects.
- **Analyze** the food we buy and consume from both a price and nutritional perspective.

## 📊 Data Collected

The final dataset contains 9,602 rows with 75 attributes. 
The number of unique products is 9,545. Duplicates are due to products appearing in multiple subcategories.

Here are some of the attributes collected:

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

## 📜 Scraping Process

The dataset was assembled in three steps:
1. **Product URLs:** The first step was to collect all the product URLs from the Migros Online website. This was done by scraping the category and subcategory pages. The corresponding dataset is called `product_categorization_and_urls.csv`.
2. **Product Specifics:** The second step was to scrape the product-specific pages to collect detailed information about each product. The corresponding dataset is called `product_specifics.csv`.
3. **Data Cleaning:** The final dataset was created by merging the two datasets and cleaning the data. The final dataset is called `final_dataset.csv`.

#### 📂 Project Structure

```
Project-SMO/
├── data/
│   └── final_dataset.csv
│   └── product_categorization_and_urls.csv
│   └── product_specifics.csv
├── scripts/
│   ├── scraper.ipynb 
│   └── EDA.ipynb
├── README.md
└── requirements.txt
```

## 🛠️ Tools

I use the following libraries and tools:
- **Web Scraping**: `selenium` and `beautifulsoup4` 
- **Data Processing**: `pandas` and `numpy`
- **Data Storage**: CSV 

## ⚠️ Limitations

- **Price per Unit Inaccuracy:** The price per unit may be incorrect due to inconsistencies on the Migros website.
- **Duplicate Products:** Some products appear in multiple subcategories, resulting in duplicates.
- **Nutritional Values:** Not all products have complete nutritional information.
- **Data Cleaning:** The data cleaning process may not catch all errors.
- **Website Changes:** The scraper will break if the website structure changes.
- **Up-to-Date Information:** Sold products change and change price frequently, so will be outdated quickly.

## 📈 Next Steps

- **Data Analysis:** Analyze the dataset to gain insights into consumer products.
- **Data Visualization:** Create visualizations to better understand the data.


## 📝 Disclaimer

This project is for educational purposes only. Please respect the website's terms of service and robots.txt file. The author is not responsible for any misuse of this code.
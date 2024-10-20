# 🛒 Scraping Migros.ch

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

The aim of this web scraping project is to collect useful information about all products offered on [Migros.ch](https://www.migros.ch/en). 

The data was collected on **2024-10-14**.

## 🎯 Motivation

The goals of this project are:
- **Generate a clean dataset** for others to use in their own projects.
- **Analyze** the food we buy and consume from both a price and nutritional perspective.

## 📊 Data Collected

The final dataset contains 16,845 rows with 79 attributes. 
Duplicates are due to products appearing in multiple subcategories.
The focus is on the nutritional content of the products. 
Other useful information that could have been collected includes "country of production", "rating", "climate impact", etc.

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
  - 🧊 **Of which saturates (g)**
  - 🍞 **Carbohydrate (g)**
  - 🍬 **Of which sugars (g)**
  - 🌾 **Fibre (g)**
  - 💪 **Protein (g)**
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
│   └── (hidden) product_categorization_and_urls.csv
│   └── (hidden) product_specifics.csv
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

- **Price per unit inaccuracy:** The price per unit may be incorrect due to inconsistencies on the Migros website.
- **Duplicate products:** Some products appear in multiple subcategories, resulting in duplicates.
- **Nutritional values:** Not all products have complete nutritional information.
- **Data cleaning:** The data cleaning process may not catch all errors.
- **Website changes:** The scraper will break if the website structure changes.
- **Up-to-Date information:** Sold products change and change price frequently, so will be outdated quickly.

## 📈 Next Steps

- **Data Analysis:** Analyze the dataset to gain insights into consumer products.
- **Data Visualization:** Create visualizations to better understand the data.


## 📝 Disclaimer

This project is for educational purposes only. Please respect the website's terms of service. Be a maverick the right way.
```
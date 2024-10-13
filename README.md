# 🛒 Project 3S: Scrape Swiss Supermarkets

## 📖 Overview

**Project 3S** aims to scrape the websites of major Swiss supermarkets (Migros, Coop, Denner, Lidl, and Aldi) to extract information food products consumed in Switzerland.

## 🎯 Motivation

The goals of this project are:

- **Analyze** the food we buy and consume from both a price and nutritional perspective.
- **Generate clean datasets** for others to use in their own projects.
- **Gather insights** to make informed dietary decisions.

## 📊 Data Collected

We extract the following information from each product:

- 🏪 **Store**
- 🗂️ **Category**
- 📂 **Subcategory**
- 🔗 **URL**
- 🏷️ **Product Name**
- ⚖️ **Weight**
- 💰 **Price**
- 💲 **Price per 100g**
- 🥦 **Nutritional Information**:
  - 🔥 **Calories**
  - 💪 **Proteins**
  - 🍞 **Carbohydrates**
  - 🧈 **Fats**
  - 🌾 **Fibers**

Current Data Collection Status:
- **Migros**: 9,002 products
- **Others**: Pending


## 🛠️ Tools

I use the following libraries and tools:

- **Web Scraping**: `selenium` and `beautifulsoup4` 
- **Data Processing**: `pandas`
- **Data Storage**: CSV 

## 🚧 Progress

The project is currently **in progress**. So far I've beein able to scrape the **Migros** website. The next step is to scrape **Coop**, and then start analyzing the data.

---
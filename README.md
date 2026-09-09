# 📊 Data Science Projects Portfolio

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-blue?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-red)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-blue)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-Web%20Scraping-orange)

## 👋 About This Repository

Welcome to my **Data Science Projects Portfolio**!

This repository contains two practical projects that demonstrate my skills in **Python, Data Collection, Data Cleaning, Exploratory Data Analysis (EDA), and Data Visualization**.

### 📂 Projects

1. ₿ **Cryptocurrency Data Analysis**
2. 📚 **Books Web Scraping & Data Analysis**

Both projects follow a practical data pipeline:

```text
Data Collection
      ↓
Data Cleaning
      ↓
Data Transformation
      ↓
Exploratory Data Analysis
      ↓
Data Visualization
      ↓
Insights
```

---

# ₿ 1. Cryptocurrency Data Analysis

## 📌 Project Overview

This project focuses on analyzing **cryptocurrency market data** collected through an API.

The project collects cryptocurrency information, performs data cleaning and preprocessing, and analyzes important market indicators such as **market capitalization, current price, trading volume, and 24-hour price changes**.

The project collects **500 cryptocurrency records** by retrieving 50 records across 10 pages.

---

## 🎯 Objectives

* Collect cryptocurrency data using an API
* Store API data in a structured dataset
* Clean and preprocess the data
* Handle missing values
* Analyze cryptocurrency market capitalization
* Compare cryptocurrency prices
* Analyze 24-hour price changes
* Analyze trading volume
* Create meaningful visualizations
* Identify important cryptocurrency market patterns

---

## 🔄 Cryptocurrency Data Pipeline

```text
Cryptocurrency API
        ↓
   API Requests
        ↓
    JSON Data
        ↓
   Pandas DataFrame
        ↓
   Data Cleaning
        ↓
 Data Transformation
        ↓
       EDA
        ↓
 Data Visualization
        ↓
  Market Insights
```

---

## 📊 Important Features

The dataset contains information such as:

| Feature                       | Description                   |
| ----------------------------- | ----------------------------- |
| `Id`                          | Cryptocurrency identifier     |
| `Symbol`                      | Cryptocurrency symbol         |
| `Name`                        | Cryptocurrency name           |
| `Current_Price`               | Current cryptocurrency price  |
| `Market_Cap`                  | Market capitalization         |
| `Market_Cap_Rank`             | Market capitalization ranking |
| `Total_Volume`                | Trading volume                |
| `High_24H`                    | 24-hour high                  |
| `Low_24H`                     | 24-hour low                   |
| `Price_Change_24H`            | 24-hour price change          |
| `Price_Change_Percentage_24H` | 24-hour percentage change     |
| `Circulating_Supply`          | Circulating supply            |
| `Total_Supply`                | Total supply                  |
| `Max_Supply`                  | Maximum supply                |
| `ATH`                         | All-time high                 |
| `ATL`                         | All-time low                  |
| `Last_Updated`                | Last updated information      |

---

## 🧹 Data Cleaning

The cleaning process includes:

* Checking missing values
* Handling missing values
* Checking data types
* Standardizing column names
* Preparing numerical columns
* Preparing the dataset for EDA

The project also handles missing values in the 24-hour percentage-change data using median-based filling.

---

## 📈 Cryptocurrency Analysis

The project analyzes:

### 🏆 Top 10 Cryptocurrencies by Market Cap

The analysis identifies the cryptocurrencies with the highest market capitalization.

```python
top10 = df.nlargest(10, "Market_Cap")
```

### 📈 Top 10 Cryptocurrencies by 24-Hour Price Change

The project also identifies cryptocurrencies with the highest positive 24-hour price changes.

```python
top_change = df.nlargest(
    10,
    "Price_Change_Percentage_24H"
)
```

### 📊 Other Analysis

* Current price comparison
* Market-cap analysis
* Trading-volume analysis
* 24-hour price movement
* Supply analysis
* ATH and ATL analysis

---

# 📚 2. Books Web Scraping & Data Analysis

## 📌 Project Overview

This project combines **Web Scraping and Data Analysis**.

Book information is collected from the **Books to Scrape** website using Python. The scraped HTML data is then converted into a structured Pandas DataFrame for cleaning, analysis, and visualization.

The scraping process works across multiple catalogue pages and collects book-related information.

---

## 🎯 Objectives

* Scrape book information from a website
* Collect data from multiple pages
* Parse HTML using BeautifulSoup
* Convert scraped information into a Pandas DataFrame
* Clean and transform the data
* Analyze book prices
* Analyze book ratings
* Explore the relationship between price and rating
* Create useful visualizations
* Generate insights from the dataset

---

## 🔄 Books Data Pipeline

```text
Books Website
      ↓
HTTP Request
      ↓
HTML Response
      ↓
BeautifulSoup
      ↓
Extract Book Information
      ↓
Pandas DataFrame
      ↓
Data Cleaning
      ↓
EDA
      ↓
Visualization
      ↓
Book Insights
```

---

## 📊 Book Dataset Features

The dataset contains fields such as:

| Column              | Description        |
| ------------------- | ------------------ |
| `Title`             | Book title         |
| `Price(£)`          | Book price         |
| `Rating`            | Book rating        |
| `Availability`      | Stock availability |
| `Book_Url`          | Book URL           |
| `Image_Url`         | Book image URL     |
| `Product_Type`      | Product type       |
| `Tax(£)`            | Tax amount         |
| `Number_Of_Reviews` | Number of reviews  |

The cleaned analysis dataset contains **980 rows and 7 columns**.

---

## 🧹 Data Cleaning

The project includes several preprocessing steps:

* Checking missing values
* Cleaning book prices
* Removing the `£` currency symbol
* Converting price into numerical format
* Converting text ratings such as `One`, `Two`, `Three`, `Four`, and `Five` into numerical ratings
* Renaming columns
* Removing unnecessary columns
* Preparing the dataset for analysis

---

## 📈 Books Analysis

### 💰 Price Distribution

The project analyzes how book prices are distributed across the dataset.

### ⭐ Rating Analysis

The project analyzes the distribution of book ratings.

### 📊 Price vs Rating

The project compares book prices across different rating levels.

For example:

```python
sns.boxplot(
    data=df,
    x="Rating",
    y="Price(£)"
)
```

The project also calculates and visualizes the **average book price by rating**.

---

# 📊 Data Visualization

Both projects use **Matplotlib and Seaborn** to communicate insights visually.

### Cryptocurrency visualizations

* Top 10 cryptocurrencies by market cap
* Top 10 cryptocurrencies by 24-hour price change
* Price-change analysis
* Market-data comparisons

### Books visualizations

* Book price distribution
* Rating distribution
* Price distribution by rating
* Average price by rating

---

# 🛠️ Technologies Used

## Programming

* 🐍 Python

## Data Collection

* Requests
* BeautifulSoup
* API

## Data Analysis

* Pandas
* NumPy

## Data Visualization

* Matplotlib
* Seaborn

## Development Environment

* Jupyter Notebook
* VS Code
* Git
* GitHub

---

# 💡 Skills Demonstrated

Through these projects, I have practiced:

* Python programming
* API data collection
* Web scraping
* HTML parsing
* JSON data handling
* Pandas
* NumPy
* Data cleaning
* Missing-value handling
* Data transformation
* Exploratory Data Analysis
* Data visualization
* Statistical analysis
* Data interpretation

---

# 📁 Repository Structure

```text
Data-Science-Projects/
│
├── Cryptocurrency-Data-Analysis/
│   ├── cryptocurrency_analysis.ipynb
│   ├── crypto_data.csv
│   └── clean_crypto_data.csv
│
├── Books-Web-Scraping-Analysis/
│   ├── books_scraping_analysis.ipynb
│   ├── books_data.csv
│   └── clean_books_data.csv
│
└── README.md
```

---

# 🚀 Future Improvements

## Cryptocurrency Project

* Add historical cryptocurrency data
* Analyze cryptocurrency volatility
* Create correlation analysis
* Build cryptocurrency clustering models
* Build price prediction models
* Create a real-time dashboard
* Deploy an interactive Streamlit application

## Books Project

* Analyze book categories in greater detail
* Analyze availability
* Build a book recommendation system
* Store scraped data in SQL
* Automate the scraping pipeline
* Create an interactive dashboard
* Deploy the project using Streamlit

---

# 🎯 My Data Science Journey

These projects are part of my journey toward becoming a **Data Scientist**.

My current learning path is:

```text
Python
   ↓
NumPy
   ↓
Pandas
   ↓
Matplotlib & Seaborn
   ↓
Statistics
   ↓
SQL
   ↓
Exploratory Data Analysis
   ↓
Machine Learning
   ↓
Real-World Projects
   ↓
Deployment
```

---

# 👨‍💻 About Me

### Gokul Chandra Swain

🎓 BCA Graduate | Berhampur University
📊 Aspiring Data Scientist
🐍 Python | Pandas | NumPy
📈 Matplotlib | Seaborn
🗄️ SQL
🤖 Machine Learning

I am passionate about **Data Science, Machine Learning, and using data to solve real-world problems**.

---

## ⭐ Thank You!

Thank you for visiting my repository!

If you find these projects useful or interesting, consider giving the repository a ⭐.

**Keep Learning. Keep Building. Keep Growing. 🚀**

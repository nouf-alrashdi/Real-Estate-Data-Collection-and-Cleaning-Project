# Real Estate Data Collection and Cleaning Project

In this project, I set out to replicate a real-world data science workflow by collecting and analyzing rental listings from two major real estate platforms — **Hilal Properties** and **Dubizzle**. The goal was to build a structured, cleaned, and enriched dataset to support predictive modeling around property pricing.

---

##  Table of Contents
1. [Project Overview](#project-overview)  
2. [Requirements](#requirements)  
3. [Setup Instructions](#setup-instructions)  
4. [Data Scraping](#data-scraping)  
5. [Data Cleaning & Integration](#data-cleaning--integration)  
6. [Feature Engineering](#feature-engineering)  

---

##  Project Overview

The primary objective of this project is to collect rental listings from two real estate platforms: **Hilal Properties** and **Dubizzle**.  
The data acquisition phase commenced with web scraping, focusing on essential property attributes such as:

- Titles  
- Locations  
- Pricing  
- Number of bedrooms and bathrooms  
- Listing categories  

This foundational data enables downstream tasks such as cleaning, integration, feature engineering, and predictive modeling for rental price estimation.

---

##  Requirements

- Python 3.8+
- Jupyter Notebook
- Dependencies (install via pip):
  pip install -r requirements.txt
`requirements.txt` includes:
- pandas
- numpy
- requests
- beautifulsoup4
- scikit-learn
- matplotlib

---

## Setup Instructions
1. Clone the repository:
git clone https://github.com/nouf-alrashdi/Real-Estate-Data-Collection-and-Cleaning-Project.git

---
2. Install dependencies (see Requirements).
3. Launch Jupyter.

---

## Data Scraping
- **Notebook**: `Scraping_Hilal_and_Dubizzle.ipynb`
- **Description**: Step-by-step scraping of Dubizzle rental listings and Hilal properties using requests and BeautifulSoup.
- **Output CSVs**: 
- `dubizzle_properties_for_rent.csv`
- `hilal_rental_data.csv`

---

## Data Cleaning & Integration
- **Notebook**: `Cleaning_and_Merging.ipynb`
- **Steps**:
- Renamed columns for consistency
- Converted prices, size, and room counts to numeric types
- Removed or filled missing values using group median or global median
- Cleaned inconsistent formatting (e.g., '300 SQM' → 300)
- Removed duplicates 
- Merged and deduped into `Merged_Cleaned_Dataset.csv`

---

## Feature Engineering
- **Notebook**: `Feature_Engineering.ipynb`
- **Derived Features**:
- Price per SQM: price / size
- Total rooms: bedrooms + bathrooms
- Location encoding: one-hot encoding for ML compatibility
- Feature scaling: using both MinMaxScaler and StandardScaler
- **Output**: `Final_Dataset.csv`

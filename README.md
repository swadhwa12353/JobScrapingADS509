# 📊 Job Description Text Mining and Classification

## Project Overview

This project explores text mining techniques on real-world job listings data. We collected raw job descriptions for three roles — **Software Engineer**, **Data Analyst**, and **Accountant** — using the [SerpAPI Google Jobs API](https://serpapi.com/google-jobs-api). The project applies cleaning, normalization, descriptive analysis, topic modeling, and classification to explore how language varies across roles and how well job roles can be predicted from text.

## Goals

✅ Collect and preprocess real-world job description data  
✅ Analyze language differences across roles  
✅ Build an unsupervised **topic model** and compare with known role labels  
✅ Build a supervised **classification model** to predict roles from text  
✅ Evaluate and visualize model performance

## Data Collection

We used a custom Python scraper with the SerpAPI to collect job postings from **California**, for the following roles:

- `Software Engineer`  
- `Data Analyst`  
- `Accountant`  

Each job listing included:

- Job Title  
- Company Name  
- Location  
- Job Description Text  
- Role Label (from search query)

## Text Processing Pipeline

- Text cleaning: line breaks, punctuation, numbers removed  
- Lowercasing  
- Stopword removal  
- Tokenization  
- Basic lemmatization  
- Descriptive statistics and visualization

## Topic Modeling

- Model: **Latent Dirichlet Allocation (LDA)** with 3 topics  
- Result: Topics did not align well with explicit roles (ARI ~ 0), suggesting that LDA captured latent themes other than job role.

## Classification Modeling

- **Model:** Logistic Regression with TF-IDF  
- **Accuracy:** 98.3% on hold-out test set  
- **Conclusion:** Roles can be predicted with high accuracy based on job description text.

## Key Insights

- Each role demonstrates distinct vocabulary and language patterns  
- Supervised classification models effectively recover job roles from text  
- Unsupervised topic modeling surfaces different latent structures, but does not directly align with explicit roles  
- The project pipeline can be reused for additional roles or job market analysis

## Tools

- Python (Pandas, Scikit-learn, Seaborn, Matplotlib, NLTK)  
- SerpAPI  
- Google Colab  

## Author
 Jason Tong, Sahil Wadhwa,  and Sadaf Sadegh Vaziri

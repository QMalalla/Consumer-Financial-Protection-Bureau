

# CFPB Consumer Complaints Analysis (2020–2024)

## 📊 Project Overview

This project analyzes over 500,000 consumer complaints filed with the **Consumer Financial Protection Bureau (CFPB)** between 2020 and 2024. Each complaint is more than a ticket—it's a story of unmet expectations within the U.S. financial system. This work aims to transform raw complaints into insights for reform, transparency, and improved customer protection.

## 🧩 Problem Statement

Although the CFPB collects vast amounts of complaint data, it remains underutilized for identifying systemic issues across the financial sector. The absence of timely analysis delays institutional improvements and policy reform.

## 🎯 Objectives

- Identify behavioral or systemic triggers from temporal trends (month, weekday, year).
- Reveal the most problematic financial products and issues.
- Benchmark company performance on response timeliness and resolution success.
- Provide actionable insights for regulators, companies, and the public.

## 👥 Target Audience

- Regulatory bodies (e.g., CFPB, financial watchdogs)
- Financial institutions and banks
- Consumer rights advocates
- Researchers in finance and public policy

## 🧾 Dataset Summary

- **Source:** [CFPB Complaint Database](https://catalog.data.gov/dataset/consumer-complaint-database)
- **Period:** 2020–2024
- **Size:** 500,000 complaints from 2,900+ companies
- **Scope:** U.S.-based, mostly submitted via Web
- **Key Columns:** Date received, Product, Issue, Narrative, Company, Timely response

## 🛠 Data Handling

- **Cleaning:** Removed nulls, standardized categories, extracted date components
- **Text Preprocessing:** Lowercasing, punctuation and stopword removal
- **Embedding:** Used `all-MiniLM-L6-v2` model for text vectorization
- **Clustering:** Grouped narratives to identify latent topics and themes
- **Missing Values:** Focused on ~174,000 valid complaint narratives

## 🔍 Key Insights

- **Q4 Spike:** Complaints increase notably from October to December
- **Product Issues:** Credit reporting dominates complaint categories
- **Top Offenders:** Equifax, TransUnion, and Experian have the highest volumes
- **Timeliness Matters:** Faster company responses often correlate with fewer repeat complaints
- **Submission Method:** Most complaints submitted online, reflecting digital consumer habits

## 💡 Recommendations

- Prepare better support infrastructure for Q4
- Build public-facing dashboards for error reporting and resolution tracking
- Modernize internal complaint systems using AI
- Establish national intelligence layers for early detection of systemic issues

## ⚠️ Limitations

- Only includes **published** complaints
- Potential demographic underrepresentation
- Some records lack outcome or resolution data

## 📚 References

- [CFPB Complaint Database](https://catalog.data.gov/dataset/consumer-complaint-database)
- [Sentence Transformers](https://www.sbert.net)
- U.S. Census Bureau (for population-normalized metrics)
- Annual reports of Equifax, Experian, and TransUnion

## 🧾 Data Dictionary

| Column Name                    | Description                                                                 |
|-------------------------------|-----------------------------------------------------------------------------|
| Date received                 | When the CFPB received the complaint                                        |
| Product                       | General financial product involved                                          |
| Sub-product                   | More specific subcategory of the product                                    |
| Issue                         | Type of issue the consumer experienced                                      |
| Sub-issue                     | More detailed classification of the issue                                   |
| Consumer complaint narrative  | Free-text complaint description by consumer                                 |
| Company public response       | Official company response published by the CFPB                             |
| Company                       | Company the complaint is about                                              |
| State                         | State where the consumer resides                                            |
| ZIP code                      | ZIP code of the consumer                                                    |
| Tags                          | Additional metadata like "Servicemember"                                    |
| Consumer consent provided?    | Whether the narrative can be published                                      |
| Submitted via                 | Channel of submission (e.g., Web, Phone)                                    |
| Date sent to company          | When the complaint was forwarded to the company                            |
| Company response to consumer  | The final response provided by the company                                  |
| Timely response?              | Whether the company responded in a timely manner                            |
| Complaint ID                  | Unique identifier                                                           |
| Year_received / Month / Day   | Date parts extracted from `Date received`                                   |
| CFPB to Company               | Days it took to forward the complaint to the company                        |
| has_narrative                 | Flag indicating presence of narrative (1 or 0)                              |
| clean_text                    | Preprocessed version of the narrative                                       |
| narrative_length              | Word count of cleaned narrative                                             |
| sentiment_score               | Sentiment polarity (-1 = negative, 1 = positive)                            |
| is_fraud_related              | Flag for presence of fraud-related keywords                                 |
| complaints_per_100k           | Normalized complaint rate by population                                     |

## 📈 Dashboard Preview

Power BI dashboard includes:

- Complaint trends over time
- Product-level breakdowns
- State and ZIP-code mapping
- Company-level benchmarks
- NLP-based complaint narrative clustering

> *“The numbers speak. Are we ready to listen?”*

---

## 👤 Author

**Qasim Malalla**  
Capstone Project — General Assembly Data Analytics Bootcamp  
March 7, 2025

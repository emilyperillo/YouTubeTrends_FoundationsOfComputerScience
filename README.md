![2ff5499e-0bf8-4ffc-b205-e496aca01204-5fe397b4e68ca](https://github.com/user-attachments/assets/cd7083a7-3c72-4a09-af5b-c2a33ce17ef2)

# YouTube Trends Analysis
### Foundations of Computer Science Project

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=flat&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)

---

## Project Overview

This repository contains a complete analysis of YouTube trending videos from **10 different countries**. The project leverages Python and the Pandas library to ingest, clean, and extract statistical insights from large datasets.

The primary objective was to process raw data to understand user engagement patterns, tag trends, and temporal distribution of video uploads.

---

## Key Features & Methodology

The project workflow is divided into three main stages:

### 1. Data Ingestion & Cleaning
* **Dataset Aggregation:** Concatenated multiple CSV files into a single dataframe, introducing a `country` column for geospatial distinction.
* **Handling Missing Values:** Identified and extracted videos containing no tags.
* **Filtering:** Created a separate `excluded` dataframe for videos with:
    * `comments_disabled`
    * `ratings_disabled`
    * `video_error_or_removed`
    * *Note: These records were removed from the primary analysis to ensure data quality.*

### 2. Feature Engineering
* **Engagement Metrics:** Calculated a `like_ratio` (Likes / Dislikes) for each video.
* **Temporal Parsing:** Split the `trending_date` into distinct `Year`, `Month`, and `Day` columns for granular time-series analysis.
* **Time Clustering:** Grouped video publish times into **10-minute intervals** (e.g., 02:20 - 02:30) to analyze upload patterns.

### 3. Statistical Analysis & Insights
* **Channel Performance:** Calculated total views per channel.
* **Tag Analysis:**
    * Counted total videos per tag.
    * Identified the most frequently used tags.
    * Computed the average *Like/Dislike ratio* for each `(tag, country)` pair.
* **Trend Identification:**
    * Identified the top-viewed video for each `(trending_date, country)` pair.
    * Identified the top-viewed video for each `(month, country)` pair.
* **Category Mapping:** Processed JSON files to map category IDs and quantified unassignable video categories per country.

---

## Technical Stack

* **Language:** Python (Jupyter Notebook) 
* **Libraries:**
    * `pandas`: For data manipulation and aggregation.
    * `numpy`: For numerical operations.
    * `json`: For parsing category metadata.
 * **Additional packages needed:**
    * `zstd`, in order to read zip files in the folders.

## Note on the use of AI tools
 * AI tools were only used as a means of support in case of code not running. AI languages did not write any code from scratch and the main support was the pandas documentation available online.
---
*Project developed for the Foundations of Computer Science course.*

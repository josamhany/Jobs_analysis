# Wuzzuf Job Listings Data Extraction and Analysis

This project is designed to scrape job listings from Wuzzuf, clean the data, perform analysis, visualize trends, and store the processed data in a MongoDB database for future use. It provides valuable insights into job market trends in Egypt, helping to identify job categories, workplace types, skills in demand, and more.

## Project Overview

The goal of this project is to gather and analyze job listings from Wuzzuf. We scrape the job data, clean it, and perform exploratory data analysis (EDA) to gain insights into various job-related aspects such as experience requirements, job categories, and company locations. The project also includes visualizations to highlight key trends in the job market.

### Key Steps

1. **Data Scraping**:
   - We scrape job data from multiple pages of Wuzzuf using Python and BeautifulSoup.
   - Data includes: Job Title, Company Name, Location, Job Type (Full-time/Part-time), Workplace Type (Remote/On-site/Hybrid), Career Level, Skills, and Job Link.

2. **Data Cleaning and Transformation**:
   - The data is cleaned to remove duplicates and missing values.
   - We process the "Years of Experience" field to handle variations in format and missing data.

3. **Data Analysis**:
   - We analyze key trends in job postings: most common job categories, job types, workplace types, and skills in demand.
   - We handle missing or incomplete experience data by assigning average experience values based on career level.

4. **Data Visualization**:
   - Various visualizations are created to showcase trends such as:
     - Job distribution by category and location.
     - Skills count per job category.
     - Prevalence of remote, hybrid, and on-site jobs.
     - Most in-demand skills and job categories.

5. **Data Storage**:
   - The cleaned and processed data is stored in a CSV file for offline analysis.
   - Additionally, the data is saved in a MongoDB database for easy querying and future analysis.

## Installation

### Prerequisites

Ensure you have the following dependencies installed:

- Python 3.x
- Libraries: `requests`, `BeautifulSoup4`, `pandas`, `matplotlib`, `seaborn`, `plotly`, `pymongo`
- MongoDB (for data storage)

You can install the required libraries by running:

```bash
pip install -r requirements.txt
```

### Setting Up MongoDB

Before using the MongoDB functionality, ensure you have a running MongoDB instance. If you don’t have MongoDB installed, follow the installation instructions from [MongoDB's official documentation](https://www.mongodb.com/docs/manual/installation/).

## Running the Project

### Step 1: Scrape Data

To start scraping job listings from Wuzzuf, run the `data_extraction.py` script:

```bash
python data_extraction.py
```

This script will fetch job listings from the first several pages of Wuzzuf and store the raw data in a CSV file.

### Step 2: Clean and Process Data

Once the data is scraped, run the `data_cleaning.py` script to clean and process the data:

```bash
python data_cleaning.py
```

This script will handle missing values, fix the experience range format, and prepare the data for analysis.

### Step 3: Analyze Data

Run the `data_analysis.py` script to analyze key trends in the data:

```bash
python data_analysis.py
```

This script will generate statistics and provide insights into the job market, including the most common job categories, workplace types, and more.

### Step 4: Visualize Data

Run the `data_visualization.py` script to visualize the results:

```bash
python data_visualization.py
```

This script generates various plots and charts, such as:
- Job distribution by category and location.
- Skills count per job category.
- Distribution of remote, hybrid, and on-site jobs.
- Most in-demand skills.

### Step 5: Store Data in MongoDB

Run the `data_storage.py` script to save the cleaned data into MongoDB:

```bash
python data_storage.py
```

This script ensures that the data is saved for easy querying in MongoDB, making it available for future analysis.

## Example Outputs

### Job Category Analysis

A bar chart visualizing the most frequent job categories:

```bash
Top 10 Most Frequent Job Categories
```

### Job Location Analysis

A bar plot showing the distribution of job postings by location:

```bash
Top 10 Locations by Job Postings
```

### Workplace Type Distribution

A pie chart representing the distribution of remote, hybrid, and on-site jobs:

```bash
Workplace Distribution (Remote, Hybrid, On-site)
```

### Most In-Demand Skills

A bar chart showcasing the top 10 most in-demand skills:

```bash
Top 10 Most In-Demand Skills
```

## Conclusion

This project provides a comprehensive analysis of the Egyptian job market by scraping, cleaning, and analyzing job listings from Wuzzuf. The insights derived from this project can help job seekers, recruiters, and businesses understand job trends, skill demands, and workplace preferences.

[linkedIn post](https://www.linkedin.com/posts/josam-hany-76b449301_python-datascience-webscraping-activity-7321942489945309185-Qm0O?utm_source=share&utm_medium=member_desktop&rcm=ACoAAE0hRQMBJwwXzE_2WIlbIlC2-W8nTypJdkU) 

[Wuzzuf](https://wuzzuf.net/jobs/egypt)

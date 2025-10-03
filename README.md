# arXiv-Scraper
Built a robust web scraper with Selenium to collect metadata from 19,000+ astrophysics papers on arXiv.org, handling CAPTCHA and complex pagination. Performed a comprehensive data analysis using pandas to identify and visualize trends in publication cycles, collaboration size, and subject popularity.

# arXiv Astrophysics Scraper and Data Analysis

## Project Summary

This project is an end-to-end data pipeline that scrapes, cleans, and analyzes research paper metadata from the arXiv.org e-print server. The goal was to collect a comprehensive dataset of all 2024 pre-prints in the field of Astrophysics (`astro-ph`) and its related disciplines to identify trends in research publication, collaboration, and revision cycles.

The script successfully navigates the site's anti-scraping measures (including intermittent CAPTCHAs) and complex pagination to gather detailed data on over 19,000 papers. The collected data was then cleaned and analyzed using the pandas library, and the key findings were presented using `matplotlib` and `seaborn`.

## Key Skills Demonstrated

* **Web Scraping:** Developed a robust, multi-stage scraper using **Selenium** to control a web browser, handle CAPTCHA challenges with **`WebDriverWait`**, and navigate complex, dynamic pagination logic. Used **BeautifulSoup** for precise HTML parsing.
* **Data Cleaning & Manipulation:** Utilized the **pandas** library to clean and transform raw scraped data. This included converting data types (strings to `datetime` objects), handling missing values, and structuring text data.
* **Exploratory Data Analysis (EDA):** Performed a multi-faceted analysis to uncover insights, including a time-series analysis of submission trends, a frequency analysis of research subjects, and correlation analyses between collaboration size and revision time.
* **Data Visualization:** Created clear and insightful visualizations using **`matplotlib`** and **`seaborn`**, including bar charts and faceted scatter plots to effectively communicate findings.
* **Professional Programming Practices:** Employed virtual environments (Conda) for dependency management, implemented robust error handling (`try...except`), and followed best practices like the DRY (Don't Repeat Yourself) principle.

## Key Findings

* The analysis revealed a potential link between submission volumes and the academic calendar, with notable peaks in activity during mid-summer and early autumn.
* A strong inverse correlation was found between the nature of a research subfield and its collaboration patterns. Theoretical fields (e.g., `hep-th`) were characterized by small team sizes and long revision times, while observational/applied fields (e.g., `astro-ph.IM`) showed the opposite trend.
* For theoretical fields, the revision timeline appears to be independent of collaboration size, suggesting it is driven by other factors like the inherent complexity of the research.
* **Scalability Note:** The scraper is currently semi-automated to handle CAPTCHAs via manual input. For a production environment, it could be upgraded to integrate with a third-party CAPTCHA-solving service.

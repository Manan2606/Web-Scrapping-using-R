# Automated Web Scraping and Analysis of Journal Articles

This project automates the process of scraping, analyzing, and visualizing data from journal articles published on [Mobile DNA Journal](https://mobilednajournal.biomedcentral.com). It uses R for data extraction, preprocessing, and visualization to derive insights such as publication trends, top authors, and keyword frequency.

## Features

- **Automated Data Scraping**: Extracts key details such as title, authors, abstract, publication date, keywords, and corresponding author information from journal articles.
- **Data Cleaning**: Ensures data integrity by removing duplicates, trimming whitespace, and handling missing values.
- **Visualizations**:
  - Publication trends over time.
  - Top 10 corresponding authors.
  - Keyword frequency analysis.

## Technologies Used

- **R Libraries**:
  - `rvest`: Web scraping
  - `dplyr`: Data manipulation
  - `xml2`: XML parsing
  - `httr`: HTTP requests
  - `stringr`: String manipulation
  - `ggplot2`: Data visualization
  - `viridis`: Color palettes
  - `tidyr`: Tidy data processing

## How to Use

### 1. Install Required Libraries
Ensure the required R libraries are installed:
```R
packages <- c("rvest", "dplyr", "xml2", "httr", "stringr", "ggplot2", "viridis", "tidyr")
install_if_missing <- function(p) {
  if (!requireNamespace(p, quietly = TRUE)) {
    install.packages(p)
  }
}
lapply(packages, install_if_missing)
```

2. Run the Script
Execute the R script to:

Scrape journal data by volume and year.
Analyze and visualize the results.
Save the cleaned data to final_scraped_data.csv.

3. Input Year
When prompted, input a year between 2010 and 2024 to fetch the corresponding volume's data:

```R
input_year <- as.integer(readline(prompt = "Enter the year (2010-2024): "))
```

4. View Visualizations
Publication Trends Over Time: Line plot of article count by month.
Top 10 Corresponding Authors: Horizontal bar chart of author contributions.
Top 10 Keywords: Horizontal bar chart of frequently used keywords.
5. Save Results
The final dataset is saved as a CSV file:

final_scraped_data.csv

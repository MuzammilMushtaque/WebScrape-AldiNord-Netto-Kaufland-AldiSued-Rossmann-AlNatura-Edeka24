Alnatura Product Scraper

Overview
This script scrapes product information from the Alnatura website. It collects data such as product ID, name, brand, ingredients, category, sub-category, allergens, labels, nutriments, image link, description, price, unit price, properties, and additional product information. The collected data is saved in both JSON and CSV formats.

Features
Scrapes product data from multiple categories
Handles pagination to gather all available products
Extracts detailed product information
Saves data in JSON and CSV formats

Requirements
Python 3.x
Libraries: requests, beautifulsoup4, pandas, json, tqdm, csv, re

Installation
Install the required libraries:
pip install requests beautifulsoup4 pandas tqdm

Usage
Ensure the required libraries are installed.
Run the script:

python alnatura_product_scraper.py
Code Explanation

Importing Libraries
requests: To make HTTP requests.
BeautifulSoup: To parse HTML content.
pandas: For data manipulation (not used in this snippet).
json: To handle JSON data.
tqdm: To display a progress bar.
csv: To handle CSV files.
re: For regular expressions.

Defining the URL and Categories
The base URL for scraping products.
A list of category IDs to iterate through.

Collecting Product Links
Iterate through each category and page to collect product links.
Break the loop if no links are found.

Scraping Product Information
Initialize an empty list to store product attributes.
Fetch each product page and parse the HTML.

Extracting Product Details
Extract various product details using try-except blocks to handle potential errors.

Handling Additional Information and Nutriments
Collect and format nutritional information.

Combining Attributes into Description
Transfer values from Artikelinformationen and Properties into description.

Saving Data to JSON and CSV
Save the collected data into JSON and CSV files.

Notes
The script includes sections for rating extraction (commented out) using Selenium, which can be activated if necessary.
Ensure the website structure has not changed before running the script, as it relies on specific HTML classes and IDs.
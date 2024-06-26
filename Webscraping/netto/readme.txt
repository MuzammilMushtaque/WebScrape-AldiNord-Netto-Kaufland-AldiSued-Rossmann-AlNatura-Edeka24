Netto Product Scraper

Overview
This script scrapes product data from the Netto online store, focusing on both food and cosmetic products. It collects various attributes such as product ID, name, brand, ingredients, category, sub-category, allergens, labels, image link, description, price, unit price, and rating. The scraped data is saved in JSON and CSV formats for further analysis.

Features
Scrapes product data from multiple pages.
Extracts and processes product attributes.
Handles food and cosmetic products separately.
Saves the data in JSON and CSV formats.

Requirements
Python 3.x
requests
pandas
beautifulsoup4
tqdm
re
json
csv
Setup
Install the required libraries using pip:

pip install requests pandas beautifulsoup4 tqdm
Save the script as netto_product_scraper.py.

Usage
Run the script:
python netto_product_scraper.py
The script will scrape the product data and save it in three files:
netto_food_products.json
netto_cosmetic_products.json
netto_products.json
netto_products.csv

Code Explanation

Headers
The script starts by defining the HTTP headers required for making requests to the Netto website.

Food Products

Scraping Links: It loops through the first 30 pages of the food category, extracting product links.
Extracting Attributes: For each product link, it extracts attributes like ID, name, brand, ingredients, category, sub-category, allergens, labels, image link, description, price, unit price, and rating.
Saving Data: The collected data is saved in a JSON file named netto_food_products.json.

Cosmetic Products

Scraping Links: It loops through the first 28 pages of the cosmetic category, extracting product links.
Extracting Attributes: For each product link, it extracts the same set of attributes as for food products.
Saving Data: The collected data is saved in a JSON file named netto_cosmetic_products.json.
Combining Data
The script combines the food and cosmetic product data into a single list and saves it in netto_products.json.

CSV Conversion
The combined product data is then saved in a CSV file named netto_products.csv, ensuring all possible keys are included.

Notes
The script uses regular expressions and BeautifulSoup for extracting and cleaning the data.
It handles different cases and potential errors using try-except blocks.
The script also ensures proper reordering of keys and appending additional information to descriptions.
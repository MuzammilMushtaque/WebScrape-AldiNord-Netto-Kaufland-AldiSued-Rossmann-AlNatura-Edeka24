Edeka24 Product Scraper
This Python script scrapes product information from the Edeka24 website, specifically from the food and cosmetic categories. It gathers product details such as names, prices, descriptions, and more, and then saves this data into JSON and CSV files.

Requirements
Python 3.x
requests
BeautifulSoup (part of bs4 package)
pandas
tqdm
You can install the required packages using pip:

"""pip install requests beautifulsoup4 pandas tqdm"""

Usage
Set up Headers

The script begins by setting up the HTTP headers to mimic a web browser's request. This is necessary to avoid being blocked by the website.

Extract Category Links

The script fetches the main category page and extracts links to all product subcategories.

Scrape Product Links

For each category, the script iterates through all pages and collects product links.

Extract Product Information

The script fetches each product page and extracts various attributes.

Save Data to JSON and CSV

The extracted data is saved in both JSON and CSV formats.

Notes

The script assumes a stable structure of the Edeka24 website. If the website structure changes, the script might need adjustments.
Some parts of the code (like fetching ratings using Selenium) are commented out and can be enabled if needed.
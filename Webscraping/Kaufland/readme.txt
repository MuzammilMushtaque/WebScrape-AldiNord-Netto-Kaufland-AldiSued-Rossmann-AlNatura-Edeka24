# Kaufland Product Scraper

This script scrapes product information from the Kaufland website. It navigates through various categories and subcategories to extract product details such as name, price, description, and images. The collected data is saved into a JSON file.

## Requirements

Ensure you have the following Python libraries installed:
- `requests`
- `beautifulsoup4`
- `pandas`
- `selenium`
- `json`
- `time`
- `re`

You can install these dependencies using pip:
```bash
pip install requests beautifulsoup4 pandas selenium
```

Additionally, ensure that you have the ChromeDriver installed for Selenium. Download it from [here](https://sites.google.com/a/chromium.org/chromedriver/downloads) and specify its path in the script.

## Script Overview

The script performs the following steps:
1. **Load Main Page**: Requests the main Kaufland page using the Requests library.
2. **Access Categories**: Accesses main categories and subcategories to drill down to the product level.
3. **Extract Product Information**: For each product, extracts details such as name, price, description, and images.
4. **Save Data to JSON**: Saves the extracted data into a JSON file.

### Functions

- **request_to_kaufland(url)**: Requests the given URL and returns the parsed HTML content using BeautifulSoup.
- **access_main_categories(categories_link)**: Iterates through the main category links and fetches subcategories.
- **access_sub_categories(subcategory_links)**: Iterates through the subcategory links to fetch sub-subcategories or products.
- **access_subsub_categories(Subsub_categories_links)**: Iterates through sub-subcategory links to fetch further subcategories or products.
- **access_subsubsub_categories(SubSubSub_cat)**: Iterates through sub-sub-subcategory links to fetch products.
- **first_page_products(ProductLists, PageNumber)**: Extracts product links from a category page and iterates through them to extract detailed product information.
- **Extract_Product_Info(product_soup, product_linkXX)**: Extracts detailed product information from a product page.
- **save_json(data)**: Saves the extracted data to a JSON file.

### Execution Flow

1. **Load Main Page**: The script starts by loading the main Kaufland page.
2. **Drill Down Through Categories**: It drills down through categories, subcategories, and further subcategories to reach product listings.
3. **Extract and Save Data**: The script then extracts product information and saves it into a JSON file.

### Usage

Run the script using Python:
```bash
python kaufland_scraper.py
```

The script will print out the progress as it navigates through categories and subcategories, and as it extracts product information.

## License

This script is provided as-is without any warranties. Use it at your own risk.
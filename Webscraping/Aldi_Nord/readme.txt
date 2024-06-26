# Aldi-Nord Scraping Script

This script is designed to scrape product information from the Aldi-Nord website. It navigates through different categories and subcategories to extract detailed information about products, including descriptions, publication dates, categories, and images. The extracted data is saved into a JSON file.

## Requirements

Ensure you have the following Python libraries installed:
- `requests`
- `beautifulsoup4`
- `pandas`
- `selenium`
- `json`
- `re`

You can install these dependencies using pip:
```bash
pip install requests beautifulsoup4 pandas selenium
```

## Script Overview

The script performs the following steps:
1. **Request the Main Page**: Access the main page of Aldi-Nord.
2. **Navigate to Products Section**: Find and navigate to the 'Produkte' section.
3. **Access Categories**: Navigate through the first and subsequent levels of categories.
4. **Extract Product Information**: For each product, extract relevant data and save it in JSON format.

### Functions

- **request_to_aldiNord(url)**: Makes a request to the given URL and returns the BeautifulSoup object.
- **access_main_page(soup)**: Extracts the link to the 'Produkte' section from the main page.
- **access_category_1(soup)**: Accesses the first level of categories.
- **access_cateogry_2(anchor_elements)**: Accesses the second level of categories.
- **access_category_n(anchor_elements)**: Accesses the nth level of categories.
- **access_category_3(product_list_soup2)**: Accesses the third level of categories and extracts product information.
- **product_extraction(final_soup)**: Extracts product information from the final soup object.
- **save_json(data)**: Saves the extracted data to a JSON file, appending new data to existing content.

### Execution Flow

1. **Request the Main Page**: Initiates a request to the Aldi-Nord main page and parses the HTML content.
2. **Access the 'Produkte' Section**: Finds the link to the 'Produkte' section and modifies the URL for subsequent requests.
3. **Request the 'Produkte' Page**: Initiates a request to the 'Produkte' page and parses the HTML content.
4. **Access Categories and Extract Products**: Navigates through categories, subcategories, and products to extract information.

### Data Extraction

The `product_extraction` function extracts various pieces of information, including:
- Description
- Publication date
- Categories
- Product name, ID, brand, price
- Product image
- Certification images

### Saving Data

Extracted data is saved into a JSON file named `scraped_data_3.json` using the `save_json` function.

### Usage

Run the script using Python:
```bash
python aldi_nord_scraper.py
```

Make sure to customize any part of the script according to your specific requirements or website changes.

## License

This script is provided as-is without any warranties. Use it at your own risk.
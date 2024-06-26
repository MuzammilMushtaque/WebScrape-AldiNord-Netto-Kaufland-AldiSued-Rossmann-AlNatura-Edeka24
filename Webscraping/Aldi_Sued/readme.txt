# Aldi-Sued Product Scraper

This script scrapes product information from the Aldi-Sued website. It navigates through various categories and extracts product details such as name, price, description, and images. The data is then saved into a JSON file.

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

Additionally, you will need the ChromeDriver to use Selenium. Download it from [here](https://sites.google.com/a/chromium.org/chromedriver/downloads) and specify the path to `chromedriver.exe` in the script.

## Script Overview

The script performs the following steps:
1. **Load the Category Page**: Uses Selenium to load a category page from the Aldi-Sued website.
2. **Click 'Show More' Button**: Dynamically clicks the 'Show More' button to load more products.
3. **Extract Product Information**: For each product, extract details such as name, price, description, and images.
4. **Save Data to JSON**: Saves the extracted data into a JSON file.

### Functions

- **request_to_AldiSued(url)**: Initializes the Selenium WebDriver and loads the given URL.
- **showMore_dynamic(driver)**: Clicks the 'Show More' button until no more products are loaded and returns the page source.
- **request_product_link(url)**: Makes a request to a product URL and returns the BeautifulSoup object.
- **extract_information(product_soup)**: Extracts product details such as name, price, description, and images.
- **beautifulsoup(html_string)**: Parses the page source, extracts product links and images, and iterates over each product to extract information.
- **save_json(data)**: Saves the extracted data to a JSON file.

### Execution Flow

1. **Load Category Page**: The script starts by loading a category page and initializing the Selenium WebDriver.
2. **Handle Dynamic Content**: It dynamically clicks the 'Show More' button to ensure all products are loaded.
3. **Extract and Save Data**: The script then extracts product information and saves it into a JSON file.

### Usage

Run the script using Python:
```bash
python aldi_sued_scraper.py
```

You will need to manually accept cookies and close any pop-up elements on the website before the script continues. 

## License

This script is provided as-is without any warranties. Use it at your own risk.
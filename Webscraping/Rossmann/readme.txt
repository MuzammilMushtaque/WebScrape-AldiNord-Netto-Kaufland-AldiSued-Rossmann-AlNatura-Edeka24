# Rossmann Product Scraper

This script scrapes product information from the Rossmann website. It navigates through the product listings, extracts details such as product name, brand, category, price, images, and other relevant information, and saves the data into a JSON file.

## Requirements

Ensure you have the following Python libraries installed:
- `requests`
- `beautifulsoup4`
- `pandas`
- `tqdm`
- `json`
- `time`

You can install these dependencies using pip:
```bash
pip install requests beautifulsoup4 pandas tqdm
```

## Script Overview

The script performs the following steps:
1. **Load Product Listing Pages**: Requests multiple pages of the product listings from the Rossmann website.
2. **Extract Product Links**: Collects links to individual product pages from the listing pages.
3. **Extract Product Information**: For each product, extracts details such as name, brand, category, price, images, and other relevant information.
4. **Save Data to JSON**: Saves the extracted data into a JSON file.

### Functions

- **save_attrs_to_json(attrs, filename='Priceonly_makeup_product_data.json')**: Saves the extracted product attributes to a JSON file.
- **Main Loop**: Iterates through the listing pages, extracts product links, and then iterates through the product links to extract and save detailed product information.

### Execution Flow

1. **Load Product Listing Pages**: The script starts by loading multiple pages of the product listings from the Rossmann website.
2. **Extract Product Links**: It collects links to individual product pages from each listing page.
3. **Extract Product Information**: For each product, it extracts detailed information such as name, brand, category, price, images, and other relevant information.
4. **Save Data to JSON**: The script then saves the extracted data into a JSON file.

### Usage

Run the script using Python:
```bash
python rossmann_scraper.py
```

The script will print out the progress as it navigates through the listing pages, extracts product links, and extracts product information. The extracted data will be saved into a JSON file named `Priceonly_makeup_product_data.json`.

### Notes

- The script uses a delay (`time.sleep(0.25)`) between requests to avoid overloading the server.
- If an error occurs during data extraction, the script will continue to the next product link.

## License

This script is provided as-is without any warranties. Use it at your own risk.
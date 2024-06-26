# WebScraping the Top German Stores

This repository contains scripts for web scraping data from the top German stores using Selenium and BeautifulSoup libraries in Python. The primary focus is on extracting data related to food and cosmetics from seven different supermarket websites.

## Repository Structure

The main folder is dedicated to web scraping and contains subfolders for each individual supermarket website. Each subfolder includes a Jupyter notebook with the web scraping script and a corresponding README file.

### Subfolders for Each Supermarket

1. **Aldi Nord**
2. **Aldi Sued**
3. **Kaufland**
4. **Edeka24**
5. **Netto**
6. **Rossmann**
7. **AlNatura**

### Data Extraction Goals

The primary goal of these scripts is to extract the following essential information from each supermarket website:

- Product names
- Brands
- Prices
- Offers
- Sales
- Descriptions
- Ingredients
- And more

## Requirements

To run the scripts in this repository, you need the following Python libraries:

- Selenium
- BeautifulSoup
- Pandas
- Jupyter Notebook

You can install these libraries using pip:

```bash
pip install selenium beautifulsoup4 pandas notebook


### Notes


- Ensure that you have the correct WebDriver for Selenium corresponding to your browser. For example, if you are using Chrome, you need to download the ChromeDriver and place it in your system's PATH.
- Each script is tailored to the specific layout and structure of the supermarket website it targets. Modifications may be necessary if the website structure changes.

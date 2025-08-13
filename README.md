## Phone Prices Web Scraping

This project is designed to extract and compare smartphone prices (e.g., Samsung S24 Ultra) from popular Nigerian e-commerce websites such as [Jumia](https://www.jumia.com.ng) and [Slot](https://www.slot.ng).
It uses Python's web scraping tools to collect product names and price data, clean and store the data, and prepare it for further analysis or price monitoring.

### Features

* Scrapes real-time product data from multiple e-commerce platforms.
* Handles multiple product links in a scalable and reusable manner.
* Extracts both product names and prices.
* Supports polite scraping using time delays.
* Cleans and formats price data (e.g., removes currency symbols, handles special characters).
* Outputs data into a pandas DataFrame for analysis or export.

### Technologies Used

* `requests` – for sending HTTP requests.
* `BeautifulSoup` – for parsing HTML content.
* `pandas` – for data manipulation and tabular storage.
* `time` – for implementing delays between requests to avoid overloading websites.

### How It Works

1. **Define Headers and Target URLs**: URLs of product pages from Jumia and Slot are defined and looped through.

2. **Scraping Logic**:

   * A function (`scrape_product_data`) is written to encapsulate the scraping logic.
   * It uses conditional logic to detect the structure of the webpage and select the appropriate HTML elements.

3. **Cleaning and Transformation**:

   * Scraped prices are cleaned to remove currency symbols (`₦`, `NGN`, `#`) and commas.
   * Converted to numeric values for analysis.

4. **Storage**:

   * Data is stored in a pandas DataFrame.
   * Can be easily exported to Excel or CSV.

### Getting Started

To run the project locally:

1. Clone the repository or download the notebook.
2. Install dependencies (preferably in a virtual environment):
   ```bash
     pip install requests beautifulsoup4 pandas
   ```
3. Open and run the Jupyter Notebook:
   ```bash
     phone_prices_web_scrape.ipynb
   ```

### Notes

* Ensure your internet connection is active when running the scraper.
* Some sites may change their HTML structure frequently. You might need to update the tag selectors accordingly.
* Always scrape responsibly – include delays and avoid sending too many requests in a short time.

### Potential Improvements

* Add exception handling and logging for failed scrapes.
* Expand support to other e-commerce platforms.
* Schedule periodic scrapes using CRON or a cloud service.
* Build a dashboard to visualize price trends.

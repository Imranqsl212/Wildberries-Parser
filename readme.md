# Wildberries Parser

This Python script is a simple web scraper designed to extract product information from the Wildberries online store and save it to a CSV file. The script utilizes the `requests` and `pandas` libraries for making HTTP requests and handling data, respectively.

## Installation

Before running the script, make sure to install the required Python packages by running the following command:

```bash
pip install requests pandas
```

## Usage

1. Clone project
   ```bash
   git clone https://github.com/Imranqsl212/Wildberries-Parser.git
   ```

2. Run project:
   ```bash
   python wildberries_parser.py
   ```


## Dependencies
- `requests`: Used for making HTTP requests to the Wildberries website.
- `pandas`: Utilized for organizing and saving the extracted data in a CSV file.

## Configuration
- `proxies`: A dictionary containing proxy settings. Modify the proxy address and port as needed.

## Functions
1. **`get_category():`**
   - Sends an HTTP GET request to the Wildberries catalog URL with specified headers and proxies.
   - Returns the JSON response.

2. **`prepare_items(response):`**
   - Extracts relevant product information from the JSON response.
   - Converts price values to a readable format.
   - Returns a list of dictionaries, each representing a product.

3. **`main():`**
   - Orchestrates the main workflow by calling `get_category()` to retrieve data and `prepare_items()` to process it.
   - Creates a pandas DataFrame from the processed data and saves it to a CSV file (`products.csv`).

## Important Notes
- The script is designed to work with the specific Wildberries URL and may need adjustments if the structure of the website changes.
- Ensure that you have the necessary permissions to scrape data from the Wildberries website.
- Consider the legality and terms of service regarding web scraping for the targeted website.
- Feel free to customize and enhance the script based on your specific needs and requirements.

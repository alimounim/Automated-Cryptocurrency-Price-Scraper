# Automated Cryptocurrency Price Scraper

## Description
This project automates the process of scraping real-time Bitcoin price data from CoinMarketCap. It stores the cryptocurrency name, price, and timestamp in a CSV file, updating the data hourly. The project leverages Python libraries like BeautifulSoup and pandas for web scraping and data handling, providing a simple yet effective way to monitor market trends over time.

## Features
- **Real-Time Data Scraping**: Fetches Bitcoin prices directly from CoinMarketCap.
- **Automated Updates**: Runs every hour to collect the latest data.
- **Data Storage**: Saves data in a CSV file for easy tracking and analysis.
- **Scalable**: Easily extendable to include multiple cryptocurrencies or integrate with APIs.

## Technologies Used
- **Python**
  - `BeautifulSoup` for HTML parsing.
  - `requests` for sending HTTP requests.
  - `pandas` for data manipulation and CSV handling.
  - `datetime` for timestamps.
  - `os` for file management.
  - `time` for automation delays.

## How It Works
1. The script sends an HTTP request to CoinMarketCap to fetch the Bitcoin page.
2. It uses BeautifulSoup to parse the page and extract the cryptocurrency name and price.
3. The data is formatted and stored in a dictionary, which is then converted to a pandas DataFrame.
4. The DataFrame is saved to a CSV file, appending new data if the file already exists.
5. The script runs in an infinite loop, updating the data every hour.

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   ```
2. **Install Dependencies**:
   Ensure you have Python installed, then run:
   ```bash
   pip install beautifulsoup4 pandas requests
   ```
3. **Run the Script**:
   ```bash
   python crypto_scraper.py
   ```

## File Structure
- **`crypto_scraper.py`**: Main script for scraping and saving data.
- **`requirements.txt`**: List of required Python libraries.
- **Output CSV File**: `Crypto_Automated_Web_Scraper_Pull.csv` (created upon first run).

## Example Output
| Crypto Name | Price   | Timestamp           |
|-------------|---------|---------------------|
| Bitcoin     | 27000.5 | 2025-01-05 14:00:00 |

## Future Enhancements
- Add support for multiple cryptocurrencies.
- Use APIs for more reliable data retrieval.
- Integrate real-time data visualization tools.
- Create a web dashboard for easier monitoring.


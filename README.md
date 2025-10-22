##Amazon Price Tracker 🛒


Track the price, ratings, and reviews of any Amazon product automatically using Python. This project scrapes product information and saves it into a CSV for analysis or personal monitoring.

Features

Scrapes product title, price, ratings, and total reviews from Amazon.

Handles data cleaning and formatting (e.g., removes ₹ and commas from price).

Supports daily tracking with automated CSV updates.

Graceful error handling for unavailable pages or network issues.

Ready for extension: email alerts, multiple products, dashboards, or visualization.

Installation

Clone this repository:

git clone https://github.com/yourusername/Amazon-Price-Tracker.git


Install required Python packages:

pip install pandas requests beautifulsoup4

Usage

Single fetch example:

from price_tracker import fetch_amazon_product, save_to_csv

url = "https://www.amazon.in/Nothing-Phone-Black-256-RAM/dp/B0B8TBNGBG/"
data = fetch_amazon_product(url)
save_to_csv(data)


Daily tracking (run continuously):

from price_tracker import track_amazon_price

product_url = "https://www.amazon.in/Nothing-Phone-Black-256-RAM/dp/B0B8TBNGBG/"
track_amazon_price(product_url, interval_seconds=86400)  # 86400 seconds = 1 day

CSV Output

The data is saved to AmazonPriceTracker.csv with the following columns:

Date	Product	Price	Total_Reviews	Rating
2025-10-22	Nothing Phone (1) 5G (Black, 256 GB)	33989	39 ratings	4.0 out of 5 stars

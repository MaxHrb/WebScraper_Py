# WebScraper_Py

## This Python code defines several functions that extract various pieces of information about a product from a webpage's HTML using the BeautifulSoup library.
The get_title function finds the span tag with the id 'productTitle' and extracts the text within the tag as the product title. If it cannot find the tag, it returns an empty string.
The get_price function finds the span tag with the id 'price' and extracts the text within the tag as the product price. If it cannot find the tag, it tries to find the span tag with the id 'dealprice' and extracts the text within the tag as the product price. If it cannot find either tag, it returns an empty string.
The get_rating function finds the i tag with the class 'a-icon a-icon-star a-star-4-5' and extracts the text within the tag as the product rating. If it cannot find the tag, it tries to find the span tag with the class 'a-icon-alt' and extracts the text within the tag as the product rating. If it cannot find either tag, it returns an empty string.
The get_review_count function finds the span tag with the id 'acrCustomerReviewText' and extracts the text within the tag as the number of user reviews for the product. If it cannot find the tag, it returns an empty string.
The get_availability function finds the div tag with the id 'availability', then finds the span tag within that div and extracts the text within the tag as the product availability status. If it cannot find the tag, it returns the string "Not Available".

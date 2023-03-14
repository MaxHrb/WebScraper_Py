# WebScraper_Py

## This Python code defines several functions that extract various pieces of information about a product from a webpage's HTML using the BeautifulSoup library.
The get_title function finds the span tag with the id 'productTitle' and extracts the text within the tag as the product title. If it cannot find the tag, it returns an empty string.
### Summary of exectution window 28 and 29
### 28
The get_price function finds the span tag with the id 'price' and extracts the text within the tag as the product price. If it cannot find the tag, it tries to find the span tag with the id 'dealprice' and extracts the text within the tag as the product price. If it cannot find either tag, it returns an empty string.
The get_rating function finds the i tag with the class 'a-icon a-icon-star a-star-4-5' and extracts the text within the tag as the product rating. If it cannot find the tag, it tries to find the span tag with the class 'a-icon-alt' and extracts the text within the tag as the product rating. If it cannot find either tag, it returns an empty string.
The get_review_count function finds the span tag with the id 'acrCustomerReviewText' and extracts the text within the tag as the number of user reviews for the product. If it cannot find the tag, it returns an empty string.
The get_availability function finds the div tag with the id 'availability', then finds the span tag within that div and extracts the text within the tag as the product availability status. If it cannot find the tag, it returns the string "Not Available".
###29

The if __name__ == '__main__': statement indicates that the code below it should only be executed when the script is run directly, as opposed to being imported as a module into another script.

When the script is run directly, the program sends an HTTP request to an Amazon search results page using the requests library with a custom User-Agent header defined in the HEADERS dictionary. The page is then parsed using the BeautifulSoup library to create a soup object that contains all of the data from the page. The program then extracts all of the links on the page that lead to individual product pages and stores them in a list called links_list.

Next, the program creates an empty dictionary called d to store the product details for each product on each page. It then loops through each link in links_list, sends an HTTP request to the individual product page, parses the page using BeautifulSoup, and extracts the product details using four different functions: get_title, get_price, get_rating, and get_review_count. The details for each product are then added to the d dictionary.

Finally, a pandas dataframe is created by using the pd.DataFrame.from_dict method with d as the input. The program then replaces any empty strings in the 'title' column with NaN and drops any rows in the dataframe where the 'title' column is NaN. The resulting dataframe is then saved as a CSV file called "amazon_data.csv".

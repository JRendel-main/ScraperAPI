# Amazon Web Scraper README

This is a simple Amazon web scraper built using Node.js and Express, designed to extract product details and reviews from Amazon.com. It utilizes the [Scraper API](http://scraperapi.com) to bypass restrictions imposed by Amazon. You can use this scraper to collect information from Amazon product pages for various purposes, such as market research, price tracking, or data analysis.


## Prerequisites

Before using this Amazon web scraper, make sure you have the following prerequisites installed on your machine:

- [Node.js](https://nodejs.org): This project is built using Node.js. You will need it to run the server.
- [npm](https://www.npmjs.com/): Node Package Manager is required to install project dependencies.

## Getting Started

Follow these steps to set up and use the Amazon web scraper:

1. Clone this repository to your local machine:
   - `git clone https://github.com/your-username/amazon-web-scraper.git`

2. Navigate to the project directory:
   - `cd amazon-web-scraper`

3. Install project dependencies:
   - `npm install`

4. Obtain a Scraper API Key:
   - You need an API Key from [Scraper API](http://scraperapi.com) to make requests to Amazon. Sign up for an account and obtain your API key. You can set your API key by updating the `APIKey` variable in `app.js`.

5. Run the server:
   - `node app.js`

The server will start running on the default port 5000 or the port specified in your environment variables.

## Usage

### Base URL

The scraper server listens on `http://localhost:5000` by default. You can access the following endpoints to scrape data:

1. `GET /`

   This is the root endpoint and can be used to check if the server is running.

2. `GET /products/:productId`

   Use this endpoint to get details of a specific Amazon product. Replace `:productId` with the Amazon product's unique identifier found in its URL. For example, if the product's URL is `https://www.amazon.com/dp/B08H7Y1YJ3`, the `:productId` would be `B08H7Y1YJ3`.

3. `GET /products/:productId/reviews`

   This endpoint allows you to retrieve product reviews for a specific Amazon product. Replace `:productId` with the product's unique identifier as mentioned above.

The server will respond with JSON data containing the scraped information.

## Example

To get product details, you can make a GET request like this:

`curl http://localhost:5000/products/B08H7Y1YJ3`

This will return a JSON response containing details about the specified product.

## Legal Considerations

When using this scraper, be sure to comply with Amazon's Terms of Service and the applicable laws and regulations governing web scraping in your jurisdiction. This scraper is intended for educational and research purposes.

## Disclaimer

This repository is provided for educational and informational purposes only. The authors are not responsible for any misuse or violation of terms and conditions by users of this software.

Happy scraping!

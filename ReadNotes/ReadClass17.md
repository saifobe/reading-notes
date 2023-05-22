# Web Scraping 
## What is web scraping?

Web scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort. 

## What is web scraping used for?

Web scraping is used to collect large information from websites. But why does someone have to collect such large data from websites? To know about this, let’s look at the applications of web scraping:

- Price Comparison: Services such as ParseHub use web scraping to collect data from online shopping websites and use it to compare the prices of products.
- Email address gathering: Many companies that use email as a medium for marketing, use web scraping to collect email ID and then send bulk emails.
- Social Media Scraping: Web scraping is used to collect data from Social Media websites such as Twitter to find out what’s trending.
- Research and Development: Web scraping is used to collect a large set of data (Statistics, General Information, Temperature, etc.) from websites, which are analyzed and used to carry out Surveys or for R&D.
- Job listings: Details regarding job openings, interviews are collected from different websites and then listed in one place so that it is easily accessible to the user.

## Is web scraping legal?

Web scraping itself isn’t illegal, but there are some important rules governing it.

Before scraping a website, you should always check its terms and conditions. Some websites may not want you to crawl and extract their data, and may block your IP address and/or take legal action.

To be on the safe side, you should always check a website’s Terms of Use to make sure you’re not doing anything wrong.

## How does web scraping work?

To extract data using web scraping with python, you need to follow these basic steps:

- Find the URL that you want to scrape
- Inspecting the Page
- Find the data you want to extract
- Write the code
- Run the code and extract the data
- Store the data in the required format

## Libraries used for Web Scraping

- **Requests** - Requests is a simple and elegant Python HTTP library. It provides methods for accessing Web resources via HTTP.

- **Beautiful Soup** - Beautiful Soup is a Python library for pulling data out of HTML and XML files.

- **Selenium** - Selenium is a portable framework for testing web applications. Selenium provides a playback tool for authoring functional tests without the need to learn a test scripting language.

- **Scrapy** - Scrapy is a free and open-source web-crawling framework written in Python. Originally designed for web scraping, it can also be used to extract data using APIs or as a general-purpose web crawler.

## How to scrape a website that requires login with Python

- **Step 1: Import Libraries** - Import all the libraries that you’ll need for web scraping. You’ll need requests and BeautifulSoup.

- **Step 2: Send a GET request to the URL of the webpage that you want to scrape** - The server responds to the request by returning the HTML content of the webpage. For this task, you’ll use Python’s requests library. The get() method issues a GET request; it fetches documents identified by the given URL.

- **Step 3: Create a BeautifulSoup object** - A BeautifulSoup object is created from the HTML, which is the markup of the website. The BeautifulSoup package is used to parse the html, that is, take the raw html text and break it into Python objects. It is called BeautifulSoup because it is like turning over the cooked html with a spatula to get at the soft, yummy goodness underneath.

- **Step 4: Find the data you want to extract** - Inspect the page to see where your data is located. To do this, right-click on the element and click “Inspect”. When you find the tag that contains the data you want to extract, it’s time to create a dataset with that information.

- **Step 5: Extract the data** - After identifying the right tag, you can extract the text within the tag using the BeautifulSoup object. If you want to extract an attribute from a tag, you can do so by treating the tag like a dictionary.

- **Step 6: Store the data in a required format** - Print the results to the screen or write to a file.


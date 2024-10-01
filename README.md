# Web Scraping with Python

## Overview
This repository contains Python scripts for web scraping using the `BeautifulSoup` library. The examples demonstrate how to scrape data from websites like [Hacker News](https://news.ycombinator.com/). Additionally, there is a script to scrape Wikipedia and preprocess the content using `NLTK`.

## Getting Started

### Prerequisites
To get started with web scraping using `BeautifulSoup`, you will need to install the necessary library:
  ```bash
  pip install bs4
  ```

### Steps
1. Install BeautifulSoup
  Use pip to install the BeautifulSoup library, which allows you to scrape and parse HTML and XML content.

2. Import the Required Libraries
  Start by importing BeautifulSoup and requests to fetch and parse data:
  from bs4 import BeautifulSoup
  import requests

3. Load Site Data Using XML Parser
  After importing the libraries, load the website data and use the XML or HTML parser to read it:
  page = requests.get("https://news.ycombinator.com/")
  soup = BeautifulSoup(page.content, 'html.parser')

4. Scrape Data of Interest
  Identify the relevant HTML elements you want to extract, like titles, links, or other data:
  titles = soup.find_all('a', class_='storylink')
  for title in titles:
    print(title.text)

You can refer to BeautifulSoup documentation here https://www.crummy.com/software/BeautifulSoup/bs4/doc/

### Scraping Wikipedia
In the script Scraping_wikipedia.py, the example demonstrates how to scrape Wikipedia articles and preprocess the data to extract sentences using NLTK.

### Example Process:
- Fetch Wikipedia page content.
- Clean and preprocess the data.
- Use NLTK to split the article text into sentences for analysis.

## Additional Resources
For detailed documentation and guidance on how to use BeautifulSoup, visit the BeautifulSoup Documentation.

For Assignment 3, I was asked to scrape a website to extract information. To practise this, I used the website BooksToScrape. This functions as a mock online bookshop with all kinds of information about several hundreds of books. My goal was to extract information specifically from books with a 5-star rating, collect their cover image URLs, and store them together with metadata.

## **Corpus**
CSV File containing:

| Content (image URL) | Metadata (title of the book) |
|--------------------|-----------------|

## **Cleaning Process**
Some book titles contained encoding issues (e.g. â instead of ').
These were cleaned using Unicode normalization + regex to remove/replace bad characters.
Whitespace was stripped and URLs were standardized.
Cleaning snippet used in code:

`title = title.encode('latin1', 'replace').decode('utf-8', 'replace')`\
`title = re.sub(r'[^\x00-\x7F]+', "'", title)`

##**Terms and Conditions**
The [robots.txt](http://books.toscrape.com/index.html/robots.txt) is empty, meaning that scraping is permitted.
They also state the following in their title:
_Books to Scrape, We love being scraped!_

http://books.toscrape.com


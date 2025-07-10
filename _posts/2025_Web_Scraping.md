---
layout: single
title: "Web Scraping Report – Denis Ndemwa"
date: 2025-05-14
author_profile: true
---

# 🕸️ Web Scraping Report

**Author:** Denis Ndemwa (CS-DA01-25056)  
**Date:** May 14, 2025


DENIS NDEMWA (CS-DA01-25056)					          Date: May 14, 2025
Web Scraping Report from	     	                                       
DENIS NDEMWA'S COLAB   

Objectives
1.	To do a brief description of what web scraping is about and its relevant tasks
2.	With satisfactory reasons, choose a website to web scrape and save it for analysis
3.	To explain what I will be doing in web scraping
INTRODUCTION 
Here I will be web scraping the website above and save it to Google Colab which using python programming language. I will be basically extracting data, rearranging it and saving it again.
What is web scraping?
Web scraping is a technique used to automatically extract data from websites using software applications. These programs are designed to visit websites, identify relevant pages, and extract specific information, like text or images, for various purposes like data mining, archiving, or research. 
Key aspects of web scraping: 
1.	Automation - Web scraping relies on automated tools (scrapers) to perform the data extraction process, making it much faster and more efficient than manual methods. 
2.	Data Extraction - Scraping involves extracting data from a website's underlying HTML code, rather than just copying visible content. 
3.	Various Applications - It's used for a wide range of applications, including: 
a)	Data mining: Gathering large datasets for analysis and research. 
b)	Information processing: Automating tasks like extracting product details from e-commerce sites. 
c)	Archiving historical content: Preserving online content for future use. 
d)	Competitor monitoring: Tracking competitor pricing and product information. 
e)	Price intelligence: Gathering and analysing pricing data from various online retailers. 

4.	Legality and Ethics: While generally legal when accessing publicly available data, it's important to be aware of a website's terms of service and any specific prohibitions against scraping. Violating these terms can lead to legal issues. 
5.	Tools and Technologies: Web scraping often utilizes programming languages like Python, libraries like BeautifulSoup, and frameworks like Scrapy for efficient data extraction and manipulation. 
Challenges:
Scraping can be challenging due to websites' dynamic content, bot detection mechanisms, and the need to handle varying website structures. 

The website I am web scraping is Web Scraping Report from
The reason why I need it is because:
a)	It has data which is open to the public.
b)	The web scraping tool that I will be using, uses the website's HTML code to extract the data you're looking for. This data might include product prices, article content, user data, or any other publicly visible information. 
c)	It has data which in a table which will help use different commands in python
HOW TO SCRAPE FOR THE WEBSITE ABOVE AND SAVE IT FOR ANALYSIS
 
These libraries are often used together in web scraping tasks. The requests library retrieves the HTML content of a web page, BeautifulSoup parses the HTML, and pandas is used to organize the extracted data into a structured format for further analysis or storage.
i.	BeautifulSoup - This library is used for parsing HTML and XML documents. It creates a parse tree that can be used to extract data from the documents.
ii.	Requests - This library is used for making HTTP requests to fetch the content of web pages. It allows Python programs to interact with web servers.
iii.	Pandas - This library provides data structures and functions for working with structured data, particularly tabular data. It introduces the concept of a DataFrame, which is similar to a table in a relational database or a spreadsheet.

 
This part of the code is basically for storing the website URL in a variable is essential for several reasons, primarily for flexibility, readability, and maintainability of the code. By using a variable, you can easily change the URL you are scraping without having to modify your code multiple times. This also makes your code more readable and easier to understand, as the URL is clearly defined. 
i.	Flexibility - If you need to scrape multiple URLs, or if the URL of the target website changes, you can simply change the variable value without altering the rest of your code.
ii.	Readability - Using a descriptive variable name (e.g., target_url) makes it clear what the variable represents, enhancing code readability.
iii.	Maintainability - Variables make your code easier to maintain. If you need to update the target URL, you only need to modify the variable value, rather than searching through your code for the URL in multiple places.
iv.	Modularity - By storing the URL in a variable, you can easily create functions or modules that accept the URL as an argument, making your code more modular and reusable.
 
1. soup = BeautifulSoup(page.text, 'html'), is used to initialize a BeautifulSoup object, named soup, by parsing the HTML content stored in the page.text variable. The 'html' argument specifies that the content should be parsed as HTML. Printing soup will display the parsed HTML content. 
2.	page.text:
This assumes that page is a variable that holds the raw HTML content retrieved from a website or a file.
soup = BeautifulSoup(page.text, 'html') - This line creates a BeautifulSoup object. The first argument is the HTML content to be parsed, and the second argument 'html' tells BeautifulSoup to use the built-in HTML parser. 
3.	print(soup):
This line displays the parsed HTML content, which is now represented as a BeautifulSoup object. 
In summary, the code parses HTML and then prints the parsed HTML content for display or further processing.
For a more helpful explanation to a user, consider adding information about how to use the soup object to extract specific parts of the HTML, for example by finding specific tags using .find() or .find_all()

 
The part of the code snippet attempts to find and print all HTML tables with the class "table" within a BeautifulSoup object named soup. The soup.find_all('table', class_='table') method is used to locate these tables, and the print(hockey_table) statement displays the results. If multiple tables with the specified class exist, the hockey_table variable will contain a list of those tables; if only one table or none are found, it will be a list containing either the single table or an empty list, respectively. 
Elaboration:
1. BeautifulSoup: The code assumes that soup is a BeautifulSoup object, which is used for parsing HTML documents.
2. find_all():  This method searches for all elements that match the specified criteria. Here, it searches for <table> elements with the class "table."
3. class_:  The class_ argument in find_all() is used to match the class attribute of HTML elements.
4. hockey_table: This variable will store the results of the search. If multiple tables are found, it will be a list containing each table as a BeautifulSoup element.
5. print():  The print() statement displays the contents of hockey_table. If there are multiple tables, it will print a list of BeautifulSoup objects. If there are no tables or only one, it will print a list containing either an empty list or the single table object. 
 
This code snippet extracts the column headings (<th>) from an HTML table using BeautifulSoup. Specifically, it finds all <th> tags, extracts their text, removes leading/trailing whitespace, and stores the resulting list of titles in the hockey_table_title variable. Finally, it prints the extracted titles. 
Here's a breakdown: 
1.	table_titles = soup.find_all('th'): This line uses BeautifulSoup's find_all() method to locate all HTML elements with the tag name th, which are typically used for table headers. The results are stored in the table_titles variable as a list of BeautifulSoup Tag objects.
2.	hockey_table_title = [title.text.strip() for title in table_titles]: This line uses a list comprehension to process each <th> tag in the table_titles list.
o	title.text: This extracts the text content of the current <th> tag.
o	.strip(): This removes any leading or trailing whitespace (spaces, tabs, newlines) from the extracted text.
o	The entire list comprehension creates a new list named hockey_table_title containing only the extracted and cleaned column header text.
3.	print(hockey_table_title): This line prints the extracted column headings to the console.
 
This code snippet uses BeautifulSoup to extract data from the first table on a webpage, specifically the first 25 rows after skipping the header row. It finds the table, retrieves all rows, and then iterates through them, extracting the text from each cell (including both <td> and <th> tags) and prints it. 
Here's a breakdown of the code:
1. soup.find('table'): This line uses BeautifulSoup's find() method to locate the first table element on the page. The find() method stops after finding the first match. 
2. table.find_all('tr'):  This line uses find_all() to retrieve all <tr> (table row) elements within the identified table. The find_all() method finds all occurrences of a tag, in this case, all <tr> elements. 
3. enumerate(rows[0:26], start=1):   This loop iterates through the first 25 rows (skipping the header, which would be the first row, at index 0). enumerate() provides both the index and the row itself. The start=1 argument ensures that row numbering starts from 1, not 0. 
4. cells = row.find_all(['td', 'th']):  This line finds all cells (both <td> and <th> elements) within the current row. It uses find_all() with a list of tags to search for either <td> or <th>. 
5. row_data = [cell.get_text(strip=True) for cell in cells]:   This list comprehension extracts the text from each cell and stores it in a list called row_data. get_text(strip=True) retrieves the text content of the cell, removing leading/trailing whitespace. 
6. print(f"Row {i}:", row_data):  This line prints the row number and the extracted data for each row. 

 
This part of the code is used to save column headings into a Pandas DataFrame, then the column names stored in a list. After saving the column headings in a DataFrame, it creates an empty DataFrame and assigns a list to the columns attribute.
 
This part of the code is used to inspect a DataFrame (df) resulting from web scraping in Python. It prints the first few rows using df.head(), or displays all rows and columns using print(df). 
 
The code df.to_csv(r'./Hockey.csv') saves a Pandas DataFrame, named df, to a CSV file named "Hockey.csv" within the current directory. The r prefix before the string path ensures that backslashes are treated literally, preventing potential issues with escape sequences. The . indicates the current directory. 
Explanation:
•	df: This refers to the Pandas DataFrame object that you want to save. 
•	.to_csv(): This is a Pandas method that exports a DataFrame to a CSV file. 
•	r'./Hockey.csv': This specifies the file path. r is a raw string literal, which prevents backslashes from being interpreted as escape characters. ./ means the current directory. Hockey.csv is the name of the CSV file. 
Conclusion
I was able to do a successful web scraping and everything played out well as expected meaning there were no errors at all. I was able to explain what web scraping is,  briefly describing what web scraping is or rather what it entails as well as web scraping a website and saved the results for analysis on a future date.

# Web Scrape


Web scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort



**The web scraping software may directly access the World Wide Web using the Hypertext Transfer Protocol or a web browser , It is a form of copying in which specific data is gathered and copied from the web, typically into a central local database or spreadsheet, for later retrieval or analysis**

## Important notes about web scraping:


1-understand how you can legally use the data

2-  not downloading data at too rapid a rate because this may break the website.


## Inspecting the Website

 figure out where we can locate the links to the files we want to download inside the multiple levels of HTML tags

## python code 

library used 

```
import requests
import urllib.request
import time
from bs4 import BeautifulSoup
```

1- download the libraryes
2- set the url to the website and access the site with our requests library.

3- parse the html with BeautifulSoup so that we can work with a nicer, nested BeautifulSoup data structure. 


## Techniques

+ Human copy-and-paste

The simplest form of web scraping is manually copying and pasting data from a web page into a text file or spreadsheet.

+ Text pattern matching

powerful approach to extract information from web pages can be based on the UNIX grep command or regular expression-matching facilities 

+ HTTP programming

Static and dynamic web pages can be retrieved by posting HTTP requests to the remote web server using socket programming.


+ HTML parsing

Many websites have large collections of pages generated dynamically from an underlying structured source like a database


+ DOM parsing


+ Vertical aggregation

he preparation involves establishing the knowledge base for the entire vertical and then the platform creates the bots automatically

+ Semantic annotation recognizing

can be used to locate specific data snippets

+ Computer vision web-page analysis

 using machine learning and computer vision that attempt to identify and extract information from web pages by interpreting pages visually as a human being might.




 ## Web Scraping best practices 

 ### + Respect Robots.txt

+ Scraping too fast and too many pages, faster than a human ever can
+ Following the same pattern while crawling. For example – go through all pages of search results, and go to each result only after grabbing links to them. No human ever does that.
+ Too many requests from the same IP address in a very short time
+ Not identifying as a popular browser. You can do this by specifying a ‘User-Agent’.
+ using a user agent string of a very old browser

What if you need some data that is forbidden by Robots.txt. You could still scrape it. Most anti-scraping tools block web scraping when you are scraping pages that are not allowed by Robots.txt.


### Make the crawling slower, do not slam the server, treat websites nicely

Use auto throttling mechanisms which will automatically throttle the crawling speed based on the load on both the spider and the website that you are crawling. Adjust the spider to an optimum crawling speed after a few trial runs. Do this periodically because the environment does change over time.



## Do not follow the same crawling pattern

Humans generally will not perform repetitive tasks as they browse through a site with random actions


## Make requests through Proxies and rotate them as needed

There are several methods that can change your outgoing IP.

+ TOR
+ VPNs
+ Free Proxies
+ Shared Proxies


## Beware of Honey Pot Traps

Honeypots are systems set up to lure hackers and detect any hacking attempts that try to gain information. 


## Avoid scraping data behind a login

Login is basically permission to get access to web pages. Some websites like Indeed do not allow permission.

They could take away your credentials or block your account which can, in turn, lead to your web scraping efforts being blocked.





# How can websites detect and block web scraping?


+ Unusual traffic/high download rate especially from a single client/or IP address within a short time span.

+ Repetitive tasks performed on the website in the same browsing pattern – based on an assumption that a human user won’t perform the same repetitive tasks all the time.
+ Checking if you are real browser – A simple check is to try and execute javascript. Smarter tools can go a lot more and check your Graphic cards and CPUs 😉 to make sure you are coming from real browser.
+ Detection through honeypots – these honeypots are usually links which aren’t visible to a normal user but only to a spider. When a scraper/spider tries to access the link, the alarms are tripped.




## How do you find out if a website has blocked or banned you?


+ CAPTCHA pages
+ Unusual content delivery delays
+ Frequent response with HTTP 404, 301 or 50x errors

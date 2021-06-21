# local storage :

the operating system typically provides an abstraction layer for storing as key/value pairs.


If your native client application needs local storage beyond key/value pairs you can embed your own database, invent your own file format.

in the past cookies were ussed to store data but it has some issues :

1-Cookies are included with every HTTP request : **slowing down your web application ,sending data unencrypted over the internet**

2-Cookies are limited to about 4 KB of data


## HTML5 STORAGE :
 refer to it as “Local Storage” or “DOM Storage.”

 ** it’s a way for web pages to store named key/value pairs locally, within the client web browser,his data persists even after you navigate away from the web site, close your browser tab, exit your browser,this data is never transmitted to the remote web server (unlike cookies)** unless you send the data manually



 ## how to access it :
 it is implemented natively in web browsers.

 access HTML5 Storage through the localStorage object on the global window object.  (if the browser suppori it)
 ```
 function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
}
```


 **The data stored can be any type supported by JavaScript**
 the data is actually stored as a string. If you are storing and retrieving anything other than strings, you will need to use functions.


 ## TRACKING CHANGES TO THE HTML5 STORAGE AREA :
   

   to make changes use : 
    ```
    setItem() 
    removeItem()
     clear()
## LIMITATIONS IN CURRENT BROWSERS:


“5 megabytes” is how much storage space each origin gets by default.


## database product :
  new API has been standardized and implemented across all major browsers
     


 

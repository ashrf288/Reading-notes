


## 
100’s = These are informational status codes

200’s = These are the success codes

300’s = These are redirection codes.

400’s =These are the client error codes. 

500’s =These are the server error codes. 

## What is a status code 202? 
202 Accepted - Often used for asynchronous processing. This code tells the client that the request was valid, but its processing will finish sometime in the future.

## What is a status code 308?
Permanent Redirect - This tells the client to use another URL to access the resource and not use the current URL anymore. It’s helpful when we have multiple endpoints for one resource, but don’t want to implement reading from all of them.

## What code would you use if an update didn’t return data to a client?
204 No Content 

## What code would you use if a resource used to exist but no longer does?
308 Permanent Redirect

## What is the ‘Forbidden’ status code?
403 Forbidden


# MONGO DB

## Why do we need to pull our MongoDB database string out of our server and put it into our .env?

to have access to the databes in the server

## What is middleware?
 functions that have access to the request object (req), the response object (res)

 ## What does app.use(express.json()) do?
 recognize the incoming Request Object as a JSON Object

 ## What does the /:id mean in a route?
 its a params 

 ## What is the difference beween PUT and PATCH?
 PUT method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource whereas the PATCH method supplies a set of instructions to modify the resource. 

 ## How do you make a defalut value in a schema?
 using mongoose command 

 ## What does a 500 error status code mean?
  Internal Server Error 

  ## What is the difference between a status 200 and a status 201?
  the 200 request was received and understood and is being processed. 201 - Created A 201 status code indicates that a request was successful and as a result, a resource has been created 



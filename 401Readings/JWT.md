##  JSON Web Token

(JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object


## When should you use JSON Web Tokens

+ Authorization
+ Information Exchange


## JSON Web Token structure

In its compact form, JSON Web Tokens consist of three parts separated by dots (.), which are:

+ Header

the header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.

+ Payload

The second part of the token is the payload, which contains the claims. Claims are statements about an entity (typically, the user) and additional data. There are three types of claims: registered, public, and private claims.


+ Signature

To create the signature part you have to take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.


## How do JSON Web Tokens work?

![](https://cdn2.auth0.com/docs/media/articles/api-auth/client-credentials-grant.png)


## JWT Authentication with Django REST

1- Obtain Token
First step is to authenticate and obtain the token. The endpoint is /api/token/ and it only accepts POST requests.

`http post http://127.0.0.1:8000/api/token/ username=vitor password=123`


2- Refresh Token
To get a new access token, you should use the refresh token endpoint /api/token/refresh/ posting the refresh token


```
http post http://127.0.0.1:8000/api/token/refresh/ refresh=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsImV4cCI6MTU0NTMwODIyMiwianRpIjoiNzAyOGFlNjc0ZTdjNDZlMDlmMzUwYjg3MjU1NGUxODQiLCJ1c2VyX2lkIjoxfQ.Md8AO3dDrQBvWYWeZsd_A1J39z6b6HEwWIUZ7ilOiPE

```



## A Production Stack

You want to only use tech in production, which is reliable, well tested and has been around for a while.


A production setup usually consists of multiple components, each designed and built to be really good at one specific thing. They are fast, reliable and very focused.

If you want to run Django in production, be sure to use a production-ready web server like Nginx, and let your app be handled by a WSGI application server like Gunicorn.

If you plan on running on Heroku, a web server is provided implicitly. You don’t have to take care of it. You just need to specify a command to run your application server (again, Gunicorn is fine) in the Procfile.


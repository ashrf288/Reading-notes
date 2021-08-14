

## What is OAuth?

OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential


## Give an example of what using OAuth would look like.
 to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon

 ## How does OAuth work? What are the steps that it takes to authenticate the user?
 two unrelated sites or services trying to accomplish something on behalf of users or their software

 steps are : 
 1- The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.

2- The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.

3- The first site gives this token and secret to the initiating user’s client software.

4- The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).

5- If not already authenticated to the authorization provider, the client may be asked to authenticate.
6-  After authentication, the client is asked to approve the authorization transaction to the second website.

7- The user approves (or their software silently approves) a particular transaction type at the first website.

8-The user is given an approved access token (notice it’s no longer a request token).

9- The user gives the approved access token to the first website.
The first website gives the access token to the second website as proof of authentication on behalf of the user.

10- The second website lets the first website access their site on behalf of the user.
11- The user sees a successfully completed transaction occurring.

12-OAuth is not the first authentication/authorization system to work this way on behalf of the end-user.
 In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).

 ## What is OpenID?
 OpenID is for humans logging into machines, OAuth is for machines logging into machines on behalf of humans."


 # Authentication and Authorization Flows


 ## What is the difference between authorization and authentication?
 Authentication means confirming your own identity, while authorization means granting access to the system.

 ## What is Authorization Code Flow? 
 exchanges an Authorization Code for a token

 ## What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
 OAuth 2.0 provides a version of the Authorization Code Flow which makes use of a Proof Key for Code Exchange (PKCE).

 ## What is Implicit Flow with Form Post?
 As an alternative to the Authorization Code Flow, OAuth 2.0 provides the Implicit Flow, which is intended for Public Clients

 ## What is Client Credentials Flow?
M2M apps use the Client Credentials Flow With machine-to-machine (M2M) applications, such as CLIs, daemons, or services running on your back-end, the system authenticates and authorizes the app rather than a user

## What is Device Authorization Flow?
 the device asks the user to go to a link on their computer or smartphone and authorize the device.

 ## What is Resource Owner Password Flow?
 highly-trusted applications can use the Resource Owner Password Flow, which requests that users provide credentials (username and password).

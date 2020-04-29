# Reading 12 - OAuth 2.0

## OAuth 2.0
* an open standard for access delegation.
* serves as a way to give users the ablity to grant application access to services without giving the application their password.

## How does it work?
* application developers needs to register the application on Github OAuth and get client_id and client_secret etc.
* application developers use client_id and client_secret and designated github url and other information to make an url that redirect the users to github sign in page.
* when user sign in with their github credential, there are several handshake happens:
  1. github authenticates user's credential, upon successful it would send application with one-time-use code.
  2. application server acts as client and use this one-time-use code to make post request with required information to github.
  3. github responds with a token that give access to user's certain github information to the application server.
  4. application server acts as client and use this token to make get request to github to get user's certain github information.
  5. github responds with requested user's github information to the application server.
  6. application server grabs username and generates hashed password for this username and save those credential to the database. Then server generates an application token based on user credential and send it to user for future authentication.

## Access Code
* `response_type=code`: your server wants an auth code.
* `client_id=<your client id>`: tells the auth server which app the user is granting access to
* `redirect_url=<your redirect url>`: tells the auth server which endpoint to redirect to upon successful authentication
* `scope=<list of scopes>`: what user's information can server get
* `state=<more stuff>`: place to store information

## Access Token
When application server uses access code to make post request to auth server, auth server will respond with access token that gives acess to user's certain information.
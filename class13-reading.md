# Reading 13 - Bearer Authorization - 4/29/2020

## Bearer Authentication
* Basic Authentication generates a token for users based on username and password they provided when they sign in or sign up. This token will be used later for subsequent request.
* OAuth uses third party services such as github, google etc to autenticate users and grant application access without giving application their password. At the end of this process, applicationn will generate token for users and this token will be used later for subsequent request.
* Both basic authentication and OAuth generate token. And Bearer Authentication uses this token to authenticate users for their requests. In this way, users don't have to send their credentials every time they make a request or go through OAuth process every time they make a request.
* A token has enough information inside to look up a user and confirm access before continuing the work.

## JSON Web Tokens (JWT)
* An open standard self-contained to securely transmit between servers and clients as a JSON object.
* This information can be verified and trusted because it is digitally signed.
* Signed tokens can verify the integrity of the claims contained within it.
* Encrypted tokens hide claims.

## When to use JWT
* Authorization: a good example is Single Sign On (SSO)
* Information Exchange: a good way of securely transimitting information between parties.
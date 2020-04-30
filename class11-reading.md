# Reading 11 - Authentication - 4/27/2020

## User Modeling
* Emails, user names, and addresses can be stored in plain text, as long as the database is password protected and/or behind a firewall.
* Password should be encrypted using a hashing algorithm before it is ever stored.
* Never send sensitive date to client application.
* Using a second model will ensure that no users will accidentally/maliciously get access to sensitive information.

## Cryptography
* Studies methods for encoding messages so that they can be read only by a person who knows the key.
* Cryptanalysis - the science of decoding encrypted messages without processing the perper key.

## Hash Algorithms
* Hash algorithms generates unique and unbreakable password and stores it to database.
* Hash algorithms is one way, it is impossible to generate original password from hashed password.
* When the user sign in to the application, the Hash algorithm will compare original password with hashed password for authentication. If authentication is successful, server will generate a token and send it to client.

## Cypher Algorithms
* Cypher algoriths take data and a key and makes encrypted data.
* Tokens can be made similarly and passed back and forth from back-end to front-end.
* It is much safter and easier to transimit token rather than plain text password for authentication when the client make a subsequent request.

## Basic Authorization
* A common method used to send user credential (username and password) in an HTTP request.
* The username and password are encoded and added to request Authorization header and send it to server for authentication.
* Be aware that base64 encoding is not a form of encryption. The client and server must use HTTPS to protect the username and password as it travels across the network.
# Securing Passwords with Bcrypt Hashing Function

Hashing is the greatest way for protecting passwords and considered to be pretty safe for ensuring the integrity of data or password.

problems :

1-Brute Force attack

2-Hash Collision attack

3-BCrypt, IT's SLOW AND STRONG AS HEL

# Basic access authentication

method for an HTTP user agent  to provide a user name and password when making a request

In basic HTTP authentication, a request contains a header field in the form of Authorization: Basic credentials

## Features

HTTP Basic authentication (BA) implementation is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages

## Security

basic authentication is typically used in conjunction with HTTPS to provide confidentiality.

 JavaScript method to clear cached credentials

 script>  document.execCommand('ClearAuthenticationCache');</script

 ## Protocol

 *Server side*

 The WWW-Authenticate header field for basic authentication is constructed as following:

**WWW-Authenticate: Basic realm="User Visible Realm"**

The server may choose to include the charset parameter from RFC 7617

**WWW-Authenticate: Basic realm="User Visible Realm", charset="UTF-8"**

*Client side*

The Authorization header field is constructed as follows:

1-The username and password are combined with a single colon (:)

2-he resulting string is encoded into an octet sequence

3-The resulting string is encoded using a variant of Base64 (+/ and with padding).

4-The authorization method and a space (e.g. "Basic ") is then prepended to the encoded string

# OWASP auth cheatsheet

**Authentication** is the process of verifying that an individual, entity or website is whom it claims to be. Authentication in the context of web applications is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know

**Session Management** is a process by which a server maintains the state of an entity interacting with it

## Authentication General Guidelines
1-User IDs

2-Email address as a User ID

## Authentication Solution and Sensitive Accounts

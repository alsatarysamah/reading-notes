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

Do NOT allow login with sensitive accounts

Do NOT use the same authentication solution

## Implement Proper Password Strength Controls

1- Minimum length of the passwords should be enforced by the application. Passwords shorter than 8 characters are considered to be weak (NIST SP800-63B).

2-Maximum password length should not be set too low, as it will prevent users from creating passphrases. A common maximum length is 64 characters due to limitations in certain hashing algorithms

### Implement Secure Password Recovery Mechanism

It is common for an application to have a mechanism that provides a means for a user to gain access to their account in the event they forget their password

### Store Passwords in a Secure Fashion

It is critical for an application to store a password using the right cryptographic technique.

### Compare Password Hashes Using Safe Functions

 comparison function:

 1-Has a maximum input length, 

 2-Explicitly sets the type of both variable

 3-Returns in constant time

 ### Authentication Responses

First implementation using the "quick exit" approach

IF USER_EXISTS(username) THEN

    password_hash=HASH(password)

    IS_VALID=LOOKUP_CREDENTIALS_IN_STORE(username, password_hash)
    
    IF NOT IS_VALID THEN

       
     RETURN Error("Invalid Username or Password!")
    
    ENDIF
    ELSE
    RETURN Error("Invalid Username or Password!")
    ENDIF

# bcrypt docs

Version Compatibility:

Node Version	Bcrypt Version

0.4	<= 0.4

0.6, 0.8, 0.10	>= 0.5

0.11	>= 0.8

4	<= 2.1.0

8	>= 1.0.3 < 4.0.0

10, 11	>= 3

12 onwards	>= 3.0.6

 error that starts with:

 gyp ERR! stack Error: "pre" versions of node cannot be installed, use the --nodedir flag instead

 ### Dependencies

NodeJS

node-gyp


Windows users will need the options for c# and c++ installed with their visual studio instance.

Python 2.x

OpenSSL

### Install via NPM

npm install bcrypt

### Usage


const bcrypt = require('bcrypt');

const saltRounds = 10;

const myPlaintextPassword = 's0/\/\P4$$w0rD';

const someOtherPlaintextPassword = 'not_bacon';

### To hash a password:

    bcrypt.genSalt(saltRounds, function(err, salt) {

    bcrypt.hash(myPlaintextPassword, salt, function(err, hash) {
        // Store hash in your password DB.
    });
     });

### To check a password:

    // Load hash from your password DB.
    .compare(myPlaintextPassword, hash, function(err, result) {
    // result == true
    });
       bcrypt.compare(someOtherPlaintextPassword, hash, function(err, result) {
    // result == false
    });
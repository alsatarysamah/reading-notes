# What is JSON Web Token?
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object.


# When should you use JSON Web Tokens?

1-Authorization

2-Information Exchange

# What is the JSON Web Token structure?

In its compact form, JSON Web Tokens consist of three parts separated by dots (.), which are:

**Header**

ex:

{

  "alg": "HS256",

  "typ": "JWT"

}

**Payload**
There are three types of claims: registered, public, and private claims.

1-Registered claims:iss (issuer), exp (expiration time), sub (subject), aud (audience).

2-Public claims:

3-Private claims

ex:

{

  "sub": "1234567890",

  "name": "John Doe",

  "admin": true

}

**Signature**

ex:

HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  secret)

 *jwt.io Debugger to decode, verify, and generate JWTs.*


 # How do JSON Web Tokens work?

 Authorization: Bearer <token

 The following diagram shows how a JWT is obtained and used to access APIs or resources:

 ![](./image/Screenshot%20(199).png)

 # Why should we use JSON Web Tokens?

 1-As JSON is less verbose than XML

 2-JSON parsers are common in most programming languages because they map directly to objects



# Are JWTs Secure?

JWTs can be either signed, encrypted or both. If a token is signed, but not encrypted, everyone can read its contents, but when you don't know the private key, you can't change it. Otherwise, the receiver will notice that the signature won't match anymore.
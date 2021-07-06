# ![GA Logo](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Auth Research Lab

---

Authentication is a complex and exciting topic that involves using many of the concepts we've already studied as well as several new ideas. 

An authentication system allows the registration / signup of new users and allows those users to sign in. It has to be able to identify each user and keep their information private and secure.

Being able to develop secure user login systems is in fact a whole career and life path in and of itself, but understanding the broad concepts of **Auth** is critically import for all developers. 

Describing auth flow and understanding key terms are very common **interview questions** for junior developers, so lets take some time to research and understand auth and the related concepts.

## Setup

Fork and clone this repository and answer the questions as you research directly in the README. You do not have to pull request and submit this lab, but you will want to have it on hand for reference in the future. 

## Auth Concepts Worksheet

#### Define the following

1. *Authentication*

Authentication is checking whether or not a user is valid i.e. checking their username and password against what is stored in the database. Every time someone logs into a website their credentials (email, username, password etc.) need to be authenticated. Another example is an API that uses an API key would need to authenticate the key that you provide before sending back any data.

2. *Authorization*

Authorization is deciding what resources an authenticated user can assess. For example on social media you are only authorized to access your own profile to edit but not anyone elses.

3. Explain how *authentication* and *authorization* are related but distinct concepts.

Users must first be authenticated by checking that their log in credentials are correct (username and password match the database) -- afterwards the user's authorization is checked to see what resources they have access to.

Links to read:

https://dev.to/lschultebraucks/introduction-to-authentication-and-authorization-1bio

https://en.wikipedia.org/wiki/Authentication

https://aboutssl.org/authentication-vs-authorization/

https://en.wikipedia.org/wiki/Authorization

5. *Sessions vs Token based auth*

Session based login is 'stateful' ie whether or not the user is logged in is stored in 'state', usually either a cookie or local storage.

Token based login is 'stateless' meaning a token in stored as a cookie or local storage and is verified by the server on each request.

link to read:

https://sherryhsu.medium.com/session-vs-token-based-authentication-11a6c5ac45e4

6. *json web token (also know as a jwt)*

Is a standard for encoding and transmitting json data payloads over http requests. It is frequently used in token based auth, where jwts are 'signed' by a server so it can verify that they originated from the same server (or a trusted origin).

jwts ARE NOT hashed or encrypted and anyone can see the information inside of them.

link:

https://jwt.io/introduction

7. *Encoding, encryption and hashing* along with the uses for and differences between the three. 

Encoding is not used for hiding data securely and can be decoded by anyone. Encoding is useful to ensure that data is not corrupted after it has been transmitted from one destination to another. Encoding is also useful when zipping data to make it a smaller size for transmission/storage. The encoding algorithm must be known by the encoder and decoder.

Encryption is a special type of encoding used to hide sensitive/secret data. Once data has been encrypted by an algorithm, the same algorithm must be used to decrypt it and typically encryption algorithms use a cypher that scrambles the data so that the same cypher must be used along with the correct algorithm to decrypt the data. Think of a cypher as a password for encryption.

Hashing data uses special algorithms called a 'hashing functions'. When data is hashed the output is mapped to the same size regardless of the input. Once hashed, data cannot be unhashed. It is impossible to decrypt hashing which is why it is used for password storage. The only way to crack a hashed password is by matching the original unhashed string to it using the hashing function. 

8. *oAuth* (pronounced oh-Auth)

#### Explore and then describe the following npm packages:

1. [bcrypt](https://www.npmjs.com/package/bcrypt)

An npm package that can be used for hashing passwords. We can use it to safely store passwords in our database.

2. [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken)

An npm package that is used for encoding jwts, signing jwts and decoding jwts. We will use it to create and sign jwts on our backend and decode jwts on our fronted.

3. [passport](https://www.npmjs.com/package/passport)
    * also describe what a *strategy* is in the context of this npm package

Passport is the industry standard for auth middleware in express. It comes with a wide variety of strategies that refer to how the auth flow works, for example 'local strategy' and 'oAuth strategy'. Passport is great because more that one strategy can be used on a server making for a smooth user experience.


---

## Licensing
1. All content is licensed under a CC-BY-NC-SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact legal@ga.co.
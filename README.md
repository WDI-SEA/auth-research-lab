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
    - verifying a user's identity (asking for privilaged credentials -- checking those against known credentials)
2. *Authorization*
    - what you are allowed to do, what you have access to after logging in, or after authenticating
3. Explain how *authentication* and *authorization* are related but distinct concepts.
    - work in conjunction with each other, authentication is a visiable process to the user, where as authorization is not. 
5. *Sessions vs Token based auth*
    - session - stores the auth details on the server(information crudded in the db when the user logs in)
    - token based auth - server checks 'tokens' on each request
6. *json web token (also know as a jwt)*
    - a way of transmitting information as json in a small size, three parts (header, payload, signature)
    - used with mobile apps or desktop (web standard draft)
    - header -- tells you how to read the information in the payload (describes the endocing standard)
    - payload -- is readable by anyone
    - signature lets us verify the origin of a jwt
7. *Encoding, encryption and hashing* along with the uses for and differences between the three
    - encoding - transformation of data, easy to check if data is complete (does not hide information)
    - encrpytion - secure encoding of data (uses password like keys) to secure information so that only parties with the keys can see it
    - hashing - irreversiable transformation of data that is fed throught a 'hashing function' 
8. *oAuth* (pronounced oh-Auth)
    - open authorization - lets a thrid party handle the authentication transaction 

#### Explore and then describe the following npm packages:

1. [bcrypt](https://www.npmjs.com/package/bcrypt)
    - industry standard package in node for handiling hashing
2. [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken)
    - implements full jwt standard
3. [passport](https://www.npmjs.com/package/passport)
    * also describe what a *strategy* is in the context of this npm package
    - passport middleware authentication package for node 
    - strategy - one specific middle providied by passport that authenticates in one way

---

## Licensing
1. All content is licensed under a CC-BY-NC-SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact legal@ga.co.
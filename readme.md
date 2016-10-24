# Security and Authentication

## Core Competencies

Students will be able to:

* Explain the main Security responsibilities of a web application
* Define the terms `authentication` and `authorization`
* Explain how a password can be stored *securely* in a database using a digest.
* Use Rails to create a simple web application with support for:
  - user registration
  - login and logout
  - "remember me" feature to keep a user signed in
  - preventing access to specific routes until a valid session is established
  - changing a password
  - some password complexity rules

## Introduction

There are *many* security responsibilities of a mature software application.

## Class Exercise

List all of the Security responsibilities of a Software Application:

* AuthN - access to system is guarded
* AuthZ - users can only access specific data and functions
* Privacy - sensitive data is kept private
* Non-repudiation - audit trails

In order to implement the above, we must define the following:

### Registration

How will users register for our web site?

* Registration page with form for name, email, password, password_confirmation
* EMail confirmation

### Authentication

* How to verify a user's identity?
* Multi-factor authentication
  - Something you know: simple login and password, pin
  - Something you have: credit card, key (safety deposit box key),
                        security token, access card, key fob
  - Something you are: DNA sample, fingerprint or retina scan

### Authorization

* How to determine and control what a user is allowed to see and do?
* Protect RESTful endpoints / routes
* Protect RESTful resources

### Password Policies

* Complexity - passwords should have a minimum complexity
* Resets - how can a user can reset their lost password?
* Password Expiration?
* Password protection - how can we ensure that passwords cannot be stolen?

### Account Management

* Can a User account be disabled or deleted?
* How can users update their profiles?

### Session Management

* Users should be able to login and logout
* User sessions should be persisted (remember me)
* User sessions can be terminated (system downtime)

### Privacy

* A user's sensitive data should be kept private
  - Access control
  - Encryption

## Building a Simple TODO App (then adding User Sessions and Security)

* For Rails see [Rails TODO App](https://github.com/ATL-WDI-Exercises/rails_todo_app)
* For Express / NodeJS see [Express Security with Passport](https://github.com/ATL-WDI-Curriculum/express-security-with-passport)

## Summary

Discuss / Review:

* HTTPS
* browser cookies
* OAuth
* encryption: 1-way (hashing, fingerprinting) and 2-way (secure communication)
* digital certs, public-key cryptography
* password digest algorithms - salt


### Quiz

* What is the difference between Authentication and Authorization?
* Why do we store the password_digest in the database instead of the password itself?
* What is the reason for storing a remember_token in the database?
* What role do browser cookies play in session management?
* What is SHA (feel free to do a Google search)?

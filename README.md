# Visual EST 
![CI](https://github.com/visual-est/visual-est-public/workflows/Java%20CI/badge.svg)

Visual EST is an [EST](https://tools.ietf.org/html/rfc7030) client with graphical interface. It uses the EST library from [Bouncy Castle](https://www.bouncycastle.org/) and [JavaFX](https://openjfx.io/).

## Main Features
*	Certificate enrollment and re-enrolment via Enrollment over Secure Transport protocol.
*	Client authentication using certificate client and/or username & password (HTTP Basic and Digest).
*	Support of TLS channel binding (Linking Identity and Proof-of-Possession information).
*	Keypair generation using EC, RSA and DSA algorithms.
*	Supported EST operations
    *	Distribution of CA certificates (getcacerts)
    *	CSR attributes (csrattrs)
    *	Client certificate request for initial enrollment (simpleenroll) 
    *	Client certificate request for re-enrollment  (simplereenroll)

## Out of the scope
*	Certificate-less TLS mutual authentication.
*	EST operations
    *	Full CMC (fullcmc)
    *	Server-Side Key Generation (serverkeygen)

**Note:** Both applications (Windows and macOS) are not code-signed, so you will see warning about this.


## Changelog

All notable changes to this project will be documented here.

### [Release 1.0.21](https://github.com/visual-est/visual-est-public/releases/tag/1.0.21) (2020-02-29)


#### Features

* Refactoring the validation logic of the client authentication certificate. How it includes expiration, chain, and revocation (CRL & OCSP) validations.



#### Bug Fixes

* The Serial Number of the issued certificate is wrong
* The Subject DN dialog does not set the correct Serial Number

# Visual EST ![CI](https://github.com/visual-est/visual-est-public/workflows/Java%20CI/badge.svg)



# Changelog

All notable changes to this project will be documented here.

## [Release 1.0.21](https://github.com/visual-est/visual-est-public/releases/tag/1.0.21) (2020-02-29)


### Features

* Refactoring the validation logic of the client authentication certificate. How it includes expiration, chain, and revocation (CRL & OCSP) validations.



### Bug Fixes

* The Serial Number of the issued certificate is wrong
* The Subject DN dialog does not set the correct Serial Number

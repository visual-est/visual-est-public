# Visual EST 

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

## Screenshots
![alt text](https://github.com/visual-est/visual-est-public/blob/master/Main%20Window.png "Main Window")


## Changelog

All notable changes to this project will be documented here.

### [Release 1.1.88](https://github.com/visual-est/visual-est-public/releases/tag/1.1.88) (2026-05-19)

#### Bug Fixes
- Fixed issue where `NOT_SPECIFIED` trust mode incorrectly returned empty trust anchors instead of the system trust store, causing EST client to fall back to insecure 'trust all' mode

### [Release 1.1.87](https://github.com/visual-est/visual-est-public/releases/tag/1.1.87) (2026-04-21)

#### Bug Fixes

**Previously**, when the trust anchor mode was set to _"Add Additional From"_, the additional certificates from the selected file were added on top of the EST CA certificates only. The JRE built-in trust store was silently ignored, causing TLS connections to servers with certificates issued by well-known public CAs to fail unexpectedly.

**Now**, selecting _"Add Additional From"_ correctly merges all three sources:
1. The JRE built-in trust store
2. The EST CA certificates retrieved via _Get CA Certificates_
3. The additional trust anchors loaded from the specified file


### [Release 1.1.84](https://github.com/visual-est/visual-est-public/releases/tag/1.1.84) (2026-04-21)

#### Bug Fixes

- **Java 25 LTS** — The application now ships with a bundled Java 25 LTS runtime, bringing improved performance, security updates, and long-term support.
- **Updated dependencies** — All third-party libraries have been updated to their latest versions.
- **Updated copyright** — Copyright notice updated to 2020–2026.

### Known Issues

> ⚠️ **Dark theme glitches** — The Dark theme may display visual artifacts or rendering glitches in certain UI areas. We are aware of the issue and it will be addressed in an upcoming release.  
> **Workaround:** Switch to the Light theme to avoid the problem.

### [Release 1.0.115](https://github.com/visual-est/visual-est-public/releases/tag/1.0.115) (2021-10-06)
#### Features
* Now Visual EST uses Bouncy Castle 1.69, Java 17, and JavaFX 14.

#### Bug Fixes
* Now on macOS Visual EST has the right icon.

### [Release 1.0.28](https://github.com/visual-est/visual-est-public/releases/tag/1.0.28) (2020-03-24)
#### Bug Fixes
* Fix an issue that prevents some private key formats to be used for CSR generation.

### [Release 1.0.27](https://github.com/visual-est/visual-est-public/releases/tag/1.0.27) (2020-03-09)
#### Bug Fixes
* Fix the eye icon on the password fields

### [Release 1.0.26](https://github.com/visual-est/visual-est-public/releases/tag/1.0.26) (2020-03-08)
#### Features
* Tabs are now detachable, so users are able to see General and Log tab at the same time.

### [Release 1.0.25](https://github.com/visual-est/visual-est-public/releases/tag/1.0.25) (2020-03-08)
#### Features
* The sections for Certificate and Username & Password authentication has been merged into one. In addition, the Additional Settings section has been moved as separate tab.

### [Release 1.0.24](https://github.com/visual-est/visual-est-public/releases/tag/1.0.24) (2020-03-05) 
#### Features
* A new way to select client authentication certificate. Users can now drag & drop, paste, or browse certificate.

### [Release 1.0.23](https://github.com/visual-est/visual-est-public/releases/tag/1.0.23) (2020-03-03)
#### Features
* Double click on a log event will open it in a new dialog.

### [Release 1.0.22](https://github.com/visual-est/visual-est-public/releases/tag/1.0.22) (2020-03-02)
#### Bug Fixes
* Certificate details are now showing UnstructuredName and UnstructuredAddress
* Certificate details window displays KU and EKU
* The attributes of the summary panel of the enrollend are now selectable
* Certificate details now shows the Serial Number in HEX

### [Release 1.0.21](https://github.com/visual-est/visual-est-public/releases/tag/1.0.21) (2020-02-29)
#### Features
* Refactoring the validation logic of the client authentication certificate. How it includes expiration, chain, and revocation (CRL & OCSP) validations.
]
#### Bug Fixes

* The Serial Number of the issued certificate is wrong
* The Subject DN dialog does not set the correct Serial Number

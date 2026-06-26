# OpenSSL Certificate Generation and Validation

## Overview

This project demonstrates the complete process of generating, inspecting, validating, and deploying a self-signed X.509 digital certificate using OpenSSL on Kali Linux.

The objective was to gain hands-on experience with Public Key Infrastructure (PKI), certificate management, and HTTPS security while understanding how digital certificates establish trust between systems.

## Objectives

* Generate a 2048-bit RSA private key
* Create a Certificate Signing Request (CSR)
* Generate a self-signed X.509 certificate
* Inspect certificate attributes
* Validate the certificate using OpenSSL
* Deploy the certificate to a local HTTPS server
* Understand browser trust and certificate validation


## Technologies Used

* Kali Linux
* OpenSSL
* HTTPS
* X.509 Certificates
* Public Key Infrastructure (PKI)

---

## Skills Demonstrated

* Public Key Infrastructure (PKI)
* Digital Certificate Management
* RSA Key Generation
* Certificate Signing Requests (CSR)
* Certificate Validation
* HTTPS Configuration
* Browser Trust Verification
* Cryptography Fundamentals

---

## Key Commands

```bash
openssl genrsa -out itskillcentre.key 2048

openssl req -new -key itskillcentre.key -out itskillcentre.csr

openssl x509 -req -days 365 -in itskillcentre.csr -signkey itskillcentre.key -out itskillcentre.crt

openssl x509 -in itskillcentre.crt -text -noout

openssl verify -CAfile itskillcentre.crt itskillcentre.crt

openssl s_server -key itskillcentre.key -cert itskillcentre.crt -accept 8443 -www

**What I Learned**

One of the biggest lessons from this project was understanding the difference between a **valid certificate** and a **trusted certificate**.

Although the certificate was cryptographically valid, browsers displayed a warning because it was self-signed rather than issued by a trusted Certificate Authority (CA). This demonstrated how browsers protect users from potential Man-in-the-Middle (MITM) attacks through certificate trust verification.

**
The complete technical report for this project is included in this repository.

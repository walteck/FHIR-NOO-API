---
title: Security Guidance
keywords: development
tags: [development]
sidebar: overview_sidebar
permalink: development_api_security_guidance.html
summary: "Details of the API security model and supported protocols."
---

## Transport Layer Security (TLS) Protocol ##

After consultation with the Infrastructure Security, Operational Security and Spine DDC teams the following SSL protocols SHALL be supported.

{% include important.html content="The list of supported ciphers is ordered in order of preference (i.e. the first item being the most preferred)." %}

- `TLSv1.2`
- `TLSv1.1`
- `TLSv1`

## Supported Ciphers ##

After consultation with the Infrastructure Security, Operational Security and Spine DDC teams the following SSL ciphers SHALL be supported.

{% include important.html content="The list of supported ciphers is ordered in order of preference (i.e. the first item being the most preferred)." %}

- `AESGCM+EECDH`
- `AESGCM+EDH`
- `AES256+EECDH`
- `AES256+EDH`

{% include note.html content="GCM (Galois Counter Mode) suites are preferred as these are resistant to timing attacks<sup>1</sup>." %}

{% include important.html content="A Java 8 (or above) Runtime Environment and/or an upto date version of OpenSSL is required to support the GCM cipher suites." %}

<sup>1</sup>[Digitcert - SSL Support Enabling Perfect Forward Secrecy](https://www.digicert.com/ssl-support/ssl-enabling-perfect-forward-secrecy.htm)

## Tomcat OpenSSL Support Using The APR/Native Provider ##

- SSLCipherSuite = `AESGCM+EECDH,AESGCM+EDH,AES256+EECDH,AES256+EDH`
- SSLHonorCipherOrder = `true`
- SSLProtocol = `TLSv1+TLSv1.1+TLSv1.2`
- SSLVerifyClient = `require`

Please see the [Tomcat Config HTTP SSL Support](https://tomcat.apache.org/tomcat-8.0-doc/config/http.html#SSL_Support) webpage for more details.

## External Documents / Policy Documents ##

| Name | Author | Version | Updated |
| Approved Cryptographic Algorithms Good Practice Guidelines | NHS Digital | v4.0 | 13/07/2016 |
| Warranted Environment Specification (WES) | NHS Digital | v1.0 | June 2015 |
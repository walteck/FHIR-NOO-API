---
title: Cross Organisation Audit & Provenance using JWT
keywords: spine, ssp, integration, audit, jwt, provenance
tags: [Security]
sidebar: overview_sidebar
permalink: development_security_jwt.html
summary: "Overview of how audit and provenance data is expected to be transported over the National Opt-Out FHIR interfaces using JWT."
---

## Cross Organisation Audit & Provenance using JWT ##

Consumer systems SHALL provided audit and provenance details in the HTTP authorization header as an oAuth bearer token (as outlined in [RFC 6749](https://tools.ietf.org/html/rfc6749){:target="_blank"}) in the form of a JSON Web Token (JWT) as defined in [RFC 7519](https://tools.ietf.org/html/rfc7519){:target="_blank"}.

### JSON Web Tokens (JWT) ###

Consumer system SHALL generate a new JWT for each API request.

| Claim | Priority | Description | Fixed Value | Dynamic Value | Specification / Example |
|-------|----------|-------------|-------------|---------------|-------------------------|


## JWT Example ##

```json

```

{% include important.html content="Whilst the use of a JWT and the claims naming is inspired by the [SMART on FHIR](https://github.com/smart-on-fhir/smart-on-fhir.github.io/wiki/cross-organizational-auth) NHS Digital hasn't commited to using the SMART on FHIR specification." %}

### Example Code ###

TODO...what language will be used ? .NET, c#, Java ???




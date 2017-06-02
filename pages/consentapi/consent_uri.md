---
title: uri Element
keywords: uri, consent
tags: [profile,element,uri]
sidebar: overview_sidebar
permalink: consent_uri.html
summary: "low level details for the National Opt-Out 'uri' element"
---

## id Implementation Guide ##

### Use case ###

This specification describes a single use case.

### Element Usage ###

authority uses the Consent.authority element TODO...........

### status ###

|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|uri|uri  | TODO|


Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`uri`| TODO| Enter text here|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`uri`| TODO|Enter text here|


On the wire XML example

```xml
TODO
```

On the wire example in JSON

```json
TODO
```

*Error Handling*

The provider system SHALL return an error if:

- the `uri` is invalid (i.e. fails NHS Number format and check digit tests).
- the `uri` is not associated with a NHS Number Status Indicator Code





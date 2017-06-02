---
title: purpose Element
keywords: purpose, consent
tags: [profile,element,purpose]
sidebar: overview_sidebar
permalink: consent_purpose.html
summary: "low level details for the National Opt-Out 'purpose' element"
---

## id Implementation Guide ##

### Use case ###

This specification describes a single use case.

### Element Usage ###

purpose uses the Consent.purpose element TODO...........

### status ###

|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|purpose|Coding  | TODO|


Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`purpose`| TODO| Enter text here|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`purpose`| TODO|Enter text here|


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

- the `purpose` is invalid (i.e. fails NHS Number format and check digit tests).
- the `purpose` is not associated with a NHS Number Status Indicator Code





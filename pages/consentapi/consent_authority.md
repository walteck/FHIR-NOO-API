---
title: authority Element
keywords: policy, consent
tags: [profile,element,policy]
sidebar: overview_sidebar
permalink: consent_authority.html
summary: "low level details for the National Opt-Out 'authority' element"
---

## id Implementation Guide ##

### Use case ###

This specification describes a single use case.

### Element Usage ###

authority uses the Consent.authority element TODO...........

### status ###

|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|authority|uri  | TODO|


Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`authority`| TODO| Enter text here|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`authority`| TODO|Enter text here|


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

- the `authority` is invalid (i.e. fails NHS Number format and check digit tests).
- the `authority` is not associated with a NHS Number Status Indicator Code





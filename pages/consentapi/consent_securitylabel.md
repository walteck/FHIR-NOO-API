---
title: securityLabel Element
keywords: securityLabel, consent
tags: [profile,element,securityLabel]
sidebar: overview_sidebar
permalink: consent_securitylabel.html
summary: "low level details for the National Opt-Out 'securityLabel' element"
---

## id Implementation Guide ##

### Use case ###

This specification describes a single use case.

### Element Usage ###

securityLabel uses the Consent.securityLabel element TODO...........

### status ###

|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|securityLabel|Coding  | TODO|


Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`securityLabel`| TODO| Enter text here|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`securityLabel`| TODO|Enter text here|


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

- the `securityLabel` is invalid (i.e. fails NHS Number format and check digit tests).
- the `securityLabel` is not associated with a NHS Number Status Indicator Code





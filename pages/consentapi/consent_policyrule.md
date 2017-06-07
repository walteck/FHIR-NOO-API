---
title: policyRule Element
keywords: policyRule, consent
tags: [profile,element,policyRule]
sidebar: overview_sidebar
permalink: consent_policyrule.html
summary: "low level details for the National Opt-Out 'policyRule' element"
---

## id Implementation Guide ##

### Use case ###

This specification describes a single use case.

### Element Usage ###

policyRule uses the Consent.policyRule element TODO...........

### status ###

|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|policyRule|uri  | TODO|


Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`policyRule`| TODO| Enter text here|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`policyRule`| TODO|Enter text here|


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

- the `policyRule` is invalid (i.e. fails NHS Number format and check digit tests).
- the `policyRule` is not associated with a NHS Number Status Indicator Code





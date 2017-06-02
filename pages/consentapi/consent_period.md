---
title: period Element
keywords: period, consent
tags: [profile,element,patient]
sidebar: overview_sidebar
permalink: consent_period.html
summary: "low level details for the National Opt-Out 'period' element"
---
{% include important.html content="The period element described is used to TO DO........." %}

## id Implementation Guide ##

### Use case ###

This specification describes a single use case.

### Element Usage ###

Category uses the Consent.period element TODO...........

### status ###

|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|period| Period | Period of time that consent is in place for. |

Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`period`| TODO| Enter text here|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`period`| TODO|Enter text here|


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

- the `period` is invalid (i.e. fails NHS Number format and check digit tests).
- the `period` is not associated with a NHS Number Status Indicator Code





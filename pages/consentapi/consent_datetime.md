---
title: dateTime Element
keywords: date, time, consent
tags: [profile,element,patient]
sidebar: overview_sidebar
permalink: consent_datetime.html
summary: "low level details for the National Opt-Out 'period' element"
---
{% include important.html content="The dateTime element described is used to TO DO........." %}

## id Implementation Guide ##

### Use case ###

This specification describes a single use case.

### Element Usage ###

dateTime uses the Consent.dateTime element TODO...........

### status ###

|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|dateTime| dateTime | Date stamp added to the consent record. |

Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`dateTime`| TODO| Enter text here|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`dateTime`| TODO|Enter text here|

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

- the `dateTime` is invalid (i.e. fails NHS Number format and check digit tests).
- the `dateTime` is not associated with a NHS Number Status Indicator Code





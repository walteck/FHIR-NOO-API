---
title: consentingParty Element
keywords: party, consent
tags: [profile,element,patient]
sidebar: overview_sidebar
permalink: consent_consenting_party.html
summary: "low level details for the National Opt-Out 'consentingParty' element"
---
{% include important.html content="The consentingParty element described is used to TO DO........." %}

## id Implementation Guide ##

### Use case ###

This specification describes a single use case.

### Element Usage ###

Category uses the Consent.period element TODO...........

### status ###

|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|consentingParty| Reference | Captures the details of the orgnaization or person who has granted consent to share the data. |

Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`consentingParty`| TODO| Enter text here|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`consentingParty`| TODO|Enter text here|


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

- the `consentingParty` is invalid (i.e. fails NHS Number format and check digit tests).
- the `consentingParty` is not associated with a NHS Number Status Indicator Code





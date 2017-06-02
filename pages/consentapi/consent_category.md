---
title: category Element
keywords: category, consent
tags: [profile,element,category]
sidebar: overview_sidebar
permalink: consent_category.html
summary: "low level details for the National Opt-Out 'category' element"
---
{% include important.html content="The category element described is used to TO DO........." %}

## id Implementation Guide ##

### Use case ###

This specification describes a single use case.

### Element Usage ###

Category uses the Consent.category element TODO...........

### status ###

|Type|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
| Slice| identifier| Identifier | A unique national and/or local identifier for a patient |
|Complex| identifier#1 [nhsNumber]|Identifier| The patient NHS Number.|
|Extension|nhsNumberVerificationStatus|CodeableConcept| An extension with a required valueset that determines the status of the NHS number allocated to the patient.|

Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`category`| TODO| Enter text here|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`category`| TODO|Enter text here|


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

- the `category` is invalid (i.e. fails NHS Number format and check digit tests).
- the `category` is not associated with a NHS Number Status Indicator Code





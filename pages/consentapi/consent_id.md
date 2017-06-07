---
title: id Element
keywords: id, consent
tags: [profile,element,id,NHS Number,design]
sidebar: profiles_sidebar
permalink: consent_id.html
summary: "low level details for the care connect patient 'id' element"
---
{% include important.html content="The identifier element described is  used to provide a unique method to identify a NHS patient. It is not the identifier for the FHIR message" %}

## Identifier Implementation Guide ##

### Use case ###

This specification describes a single use case.

### Element Usage ###

National Opt-Out uses the Consent.id element to allocate a unique identification code to each consent record that is created.

### Logical id ###

|Name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|id| Identifier | A unique logical identifier allocated by the National Opt-Out model.|

- 'id' **MUST** be used to identify a consent record. This is the primary identifier for a patients consent preferences.

**Example of correct usage**

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`id`| 347|Logical id stored as a string value.|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`id`| 402 556 1234|NHS number must not be used as the logical id| **To CONFIRM**

RESTful API example

{% include custom/search.token1.html para="2.1." base="https://fhir.nhs.uk/StructureDefinition/" resource="consent" content="id" text1="347" %}

*Error Handling*

The provider system SHALL return an error if:

- the `id` is invalid








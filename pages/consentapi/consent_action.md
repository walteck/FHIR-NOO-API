---
title: action Element
keywords: action, consent
tags: [profile,element,action]
sidebar: overview_sidebar
permalink: consent_action.html
summary: "low level details for the National Opt-Out 'action' element"
---
## id Implementation Guide ##

### Use case ###

This specification describes a single use case.

### Element Usage ###

actor uses the Consent.actor element TODO...........

### status ###

|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|action|CondeablConcept  | TODO|

Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`action`| TODO| Enter text here|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`action`| TODO|Enter text here|


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

- the `action` is invalid (i.e. fails NHS Number format and check digit tests).
- the `action` is not associated with a NHS Number Status Indicator Code





---
title: source Element
keywords: source, consent
tags: [profile,element,patient]
sidebar: overview_sidebar
permalink: consent_source.html
summary: "low level details for the National Opt-Out 'source' element"
---

### Element Usage ###

source uses the Consent.source element to record how which mechanism was used to capture the consent information e.g Online, GP practice, Patient App.

### source ###

|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|source|  | Backbone (parent) element to capture details about source system/method.|
|attachment| Attachment | |
|reference| Reference | |  **TODO** could be a questionnaireResponse required or doc ref

Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`source`| TODO| Enter text here|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`source`| TODO|Enter text here|


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

- the `source` is invalid (i.e. fails NHS Number format and check digit tests).
- the `source` is not associated with a NHS Number Status Indicator Code





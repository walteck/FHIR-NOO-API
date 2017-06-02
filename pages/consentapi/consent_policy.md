---
title: policy Element
keywords: policy, consent
tags: [profile,element,policy]
sidebar: overview_sidebar
permalink: consent_policy.html
summary: "low level details for the National Opt-Out 'policy' element"
---
{% include important.html content="The source element described is used to TO DO........." %}

## id Implementation Guide ##

### Use case ###

This specification describes a single use case.

### Element Usage ###

actor uses the Consent.actor element TODO...........

### status ###

|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|source|  | Backbone (parent) element to capture details about source system/method.|
|attachment| Attachment | |
|reference| Reference | |

Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`policy`| TODO| Enter text here|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`policy`| TODO|Enter text here|


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

- the `policy` is invalid (i.e. fails NHS Number format and check digit tests).
- the `policy` is not associated with a NHS Number Status Indicator Code





---
title: action Element
keywords: action, consent
tags: [profile,element,action]
sidebar: overview_sidebar
permalink: consent_action.html
summary: "low level details for the National Opt-Out 'action' element"
---

### Element Usage ###

action uses the Consent.action element to indicate what actions are controlled by the national opt-out policy.

### status ###

|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|action|CondeablConcept  | TODO|

Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`action`| disclose|Only a value of 'disclose' is permitted in this element|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`action`| collect|Invalid code. Element has a fixed value to 'disclose'|


On the wire XML example

```xml
<action>
	<coding>
		<system value="http://hl7.org/fhir/ValueSet/consent-action"/>
		<code value="disclose"/>
	</coding>
</action>
```

On the wire example in JSON

```json
{
  "action": {
    "coding": {
      "system": { "-value": "http://hl7.org/fhir/ValueSet/consent-action" },
      "code": { "-value": "disclose" }
    }
  }
}
```

*Error Handling*

The provider system SHALL return an error if:

- the `action` does not have a value of 'disclose'






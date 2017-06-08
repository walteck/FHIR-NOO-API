---
title: category Element
keywords: category, consent
tags: [profile,element,category]
sidebar: overview_sidebar
permalink: consent_category.html
summary: "low level details for the National Opt-Out 'category' element"
---

### Element Usage ###

Category uses the Consent.category element to distinguish the national opt-out consent instances from any other consent instance.

### category ###

|Element Type|Data Type|Description|
| ------------- | ------------- | ------------- |
|CodeableConcept | N/A| A unique national and/or local identifier for a patient |

Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`category`| NOOM| A valid category code to identify consent instance as a NOOM type.

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`category`| ICOL|Code taken from http://hl7.org/fhir/v3/ActCode. Not use by NOOM.|


XML Example

```xml
<category>
	<coding>
		<system value="https://fhir.nhs.uk/ValueSet/noom-category-type-1"/>
		<code value="NOOM"/>
	</coding>
</category>
```

JSON Example

```json
{
  "category": {
    "coding": {
      "system": { "-value": "https://fhir.nhs.uk/ValueSet/noom-category-type-1" },
      "code": { "-value": "NOOM" }
    }
  }
}
```

*Error Handling*

The provider system SHALL return an error if:

- the `category` code is not "NOOM"
- the category valueset is not https://fhir.nhs.uk/ValueSet/noom-category-type-1





---
title: patient Element
keywords: patient, consent
tags: [profile,element,patient]
sidebar: overview_sidebar
permalink: consent_patient.html
summary: "low level details for the National Opt-Out 'patient' element"
---
### Element Usage ###

patient uses the Consent.patient element to store the patients 10 digit NHS number which has been allocated to the record via a a trace using the patient demographics service (PDS). 

### patient ###

|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|patient| Reference |Reference to the patients 10 digit NHS number|

Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`patient`| 4505577104| A valid NHS number with no spaces|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`patient`| 450-557-7104|Incorrect format. Hyphens should not be used|
|![Cross](images/cross.png)|`patient`| 450 557 7104|Incorrect format. Spacing should not be used|

*Error Handling*

The provider system SHALL return an error if:

- the `patient` is invalid (i.e. fails NHS Number format and check digit tests).
- the `patient` is not associated with a NHS Number Status Indicator Code





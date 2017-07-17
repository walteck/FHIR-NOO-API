---
title: status Element
keywords: status, consent
tags: [profile,element,status]
sidebar: overview_sidebar
permalink: consent_status.html
summary: "low level details for the National Data Opt-out 'status' element"
---
### Element Usage ###

Consent uses the Consent.status element to indicate whether the patient has agreed to data sharing or has opted out of one or both types defined within the national opt-out policy.

{% include important.html content="Where a consent instance does not exist, it is implied that the patient has agreed to national opt-out data sharing." %}

### id ###

|Element Type| Data Type| Description|
| ------------- | ------------- | ------------- |
| code| string | The current status of the consent instance.|


- `active` **MAY** be used to indicate that the patient has agreed to national opt-out data sharing.
- `inactive` **MUST** be used to indicate that the patient has requested to Opt-Out. 
- No other code is permitted to be used as a status of a consent instance.
- Where a patient updates one or both of their preferences, the status code **MUST** be updated accordingly.

Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`status`| active|Patients data for research and/or planning and commissioning will be shared|

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`status`|proposed |Although status is a valid FHIR code, it is an invalid NDOP code.|

### Examples ###

XML Body

```xml
<status value="active"/>
```
JSON Body

```json
{
    "status": { "-value": "active" }
}
```

### Code Snippets

```javascript
TODO
```

```python
TODO
```

```C#
TODO
```

```java
TODO
```


*Error Handling*

HTTP response codes will determine the success or failure of the POST operation. No element specific codes will be generated upon failure to POST.









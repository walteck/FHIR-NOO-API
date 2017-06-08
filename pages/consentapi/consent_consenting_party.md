---
title: consentingParty Element
keywords: party, consent
tags: [profile,element,patient]
sidebar: overview_sidebar
permalink: consent_consenting_party.html
summary: "low level details for the National Opt-Out 'consentingParty' element"
---
### Element Usage ###

consenting party uses the Consent.consentingParty element to capture the consenter. This would typically be the patient themselves.  

### consenting party ###

|name|Data Type|Description|
| ------------- | ------------- | ------------- | ------------- |
|consentingParty| Reference | Captures the details of the organization or person who has granted consent to share the data. |

Example of correct usage

|Usage| Element| examples| Comments|
|![Tick](images/tick.png)|`consentingParty`|https://nww.spine.nhs.uk/4505577104 |

Examples of incorrect usage

|Usage| Element| examples| Comments|
|![Cross](images/cross.png)|`consentingParty`| https://nww.spine.nhs.uk/450-557-7104|

XML example

```xml
    <consentingParty>
    	<reference value="https://nww.spine.nhs.uk/4505577104"/>
    </consentingParty>
```

JSON example

```json
{
  "consentingParty": {
    "reference": { "-value": "https://nww.spine.nhs.uk/4505577104" }
  }
}
```

*Error Handling*

The provider system SHALL return an error if:

- the `consentingParty` is invalid (i.e. fails NHS Number format and check digit tests).
- the `consentingParty` is not associated with a NHS Number Status Indicator Code





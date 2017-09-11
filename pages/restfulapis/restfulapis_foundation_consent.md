---
title: Foundation | Consent
keywords: structured, restful, consent, policy
tags: [fhir, security, restful, consent]
sidebar: accessrecord_rest_sidebar
permalink: restfulapis_foundation_consent.html
summary: A record of a healthcare consumer’s policy choices, which permits or denies identified recipient(s) or recipient role(s) to perform one or more actions within a given policy context, for specific purposes and periods of time.
---
{% include custom/search.warnbanner.html %}
{% include custom/profile.html content="[Consent](https://fhir.nhs.uk/StructureDefinition/NationalOptOut-Consent-1.html)" %}

## 1. Create ##

New National Data Opt-out records are captured using the FHIR `Consent` resource.

<div markdown="span" class="alert alert-success" role="alert">
POST https://fhir.nhs.uk/structureDefinition/Consent</div>


## 2. Read ##

<div markdown="span" class="alert alert-success" role="alert">
GET https://fhir.nhs.uk/structureDefinition/Consent/[id]</div>

Return a single `Consent` record for the specified logical ID (Not the NHS Number). 

## 3. Search Parameters ##

<div markdown="span" class="alert alert-success" role="alert">
GET /Consent/[searchParameters]</div>
Consent contains the patients opt-out preferences for the National Data Opt-out Programme. Returns a bundle or single `Consent` resource for the specified patient or search criteria.

{% include custom/moscow.html content="[Consent](https://www.hl7.org/fhir/consent.html#search)" %}

| Name | Type | Description | Conformance | Path |
|------|------|-------------|-------|------|
| `id` | `identifier` | Logical ID assigned to the consent record. |  | Consent.id |
| `status` | `code` | Current consent status |  | Consent.status |
| `patient` | `Reference` | Reference used to identify the patient, typically an NHS number |  | Consent.patient |


## 4. History ##

<div markdown="span" class="alert alert-success" role="alert">
GET /Consent/_history/[searchParameters]</div>

***Update when decision on history has been made***

## 3. Example ##

Place a consent record onto the National Data Opt-out register (Spine Clinical Database)

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Consent xmlns="http://hl7.org/fhir">
	<id value="783ffeef-538e-4a17-bed2-983a382ccdd7"/>
	<status value="active"/>
    <patient>
    	<reference value="https://nww.spine.nhs.uk/4505577104"/> 
    </patient>
    <dateTime value="2017-02-01T11:15:33+00:00"/>
    <consentingParty>
    	<reference value="https://nww.spine.nhs.uk/4505577104"/>
    </consentingParty>
    <actor>
        <role>
            <coding>
                <system value="http://hl7.org/fhir/v3/ParticipationType"/>
                <code value="INF"/> 
            </coding>
        </role>
        <reference>
            <reference value="Practitioner/5679"/>
        </reference>
    </actor>
    <policyRule value="http://hl7.org/fhir/ConsentPolicy/opt-out"/>
    <purpose> 
        <system value="http://hl7.org/fhir/v3/ActReason"/> 
        <code value="HRESCH"/>
        <display value="healthcare research"/>
    </purpose>
    <purpose> 
        <system value="http://hl7.org/fhir/v3/ActReason"/> 
        <code value="HOPERAT"/> 
        <display value="healthcare operations"/>
    </purpose>
</Consent>
```

### 3.1 Request Query ###
Return all Patient resources with a NHS Number 9876543210, the format of the response body will be xml. Replace 'baseUrl' with the actual base Url of the FHIR Server.

#### 3.1.1. cURL ####

{% include custom/embedcurl.html title="Search Patient" command="curl -X GET  'http://[baseUrl]/Patient?identifier=https://fhir.nhs.uk/Id/nhs-number|9876543210&_format=xml'" %}

### 3.2 Response Headers ###

| Status Code |
|----------------|
|201 | Created

| Header | Value |
|-----------------|---------|
| Content-Type  | application/xml+fhir;charset=UTF-8 |



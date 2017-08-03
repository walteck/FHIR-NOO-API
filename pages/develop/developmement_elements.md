---
title: Profile Elements
keywords: elements, consent
tags: [profile,elements,usage]
sidebar: overview_sidebar
permalink: development_elements.html
summary: "Implentation guide on the characteristics and usage of the profiles elements"
---

## Consent Profile Elements ##

|Name|Data Type|Card|Description|Value|
|----|---------|----|-----------|-----|
|[`id`](consent_id.html)|token|1..1|Logical id assigned by the FHIR server|Any UUID|
|[`status`](consent_status.html)|string|1..1|The current status of the consent instance|active,inactive|
|[`category`](consent_category.html)|string|1..1|Category uses the Consent.category element to distinguish the national opt-out consent instances from any other consent instance|NDOP|
|[`patient`](consent_patient.html)|Reference|1..1|Spine reference to the patients NHS number traced from PDS|
|`period`|dateTime|1..1|Period consent commences|
|`dateTime`|dateTime|1..1|Date and time instance was last updated|Date+Time+TimeZone|
|[`consentingParty`](consentingparty.html)|Reference|1..1|Reference to the patient NHS number traced from PDS|
|[`actor`](consent_actor.html)|backbone|1..*|Captures the patient or healthcare professional who controls the consent|N/A|
|`actor.role`|CodeableConcept|1..1|Valueset for the role|INF=informant|
|`actor.reference`|Reference|1..1|URL for the actor|
|`actor.actorperson`|extension|0..1|String value to capture person|Mother of patient|
|[`action`](consent_action.html)|CodeableConcept|1..1|to indicate what actions are controlled by the national opt-out policy|disclose|
|[`organization`](consent_organization.html)|Reference|1..1|ODS code for the organization.|MUST be a URL|
|[`source`](consent_source.html)|Reference|1..1|Capture mechanism used to set the patients preferences|
|[`purpose`](consent_purpose.html)|Coding|1..1|Contains Opt-Out for Research or Commissioning & Planning|HRESCH, HOPERAT|

## Consent Extensions ##

National Data Opt-out Source of Opt-Out extension

`https://fhir.nhs.uk/STU3/StructureDefinition/extension-optoutsource-1`


|Name|Data Type|Card|Description|
|----|---------|----|-----------|
|[`OptoutSource`](consent_extension_sourceofoptout.html)|extension|1..1|Extension to capture the source that defined the national opt-out preferences e.g NHS Choice, GP System|


## FHIR&reg; RESTful API Examples ##

**XML Example 1**

The example below demonstrates the structure of a constructed XML body that can be submitted to the National Data Opt-out service via a HTTP POST. This will set the preferences for HRESCH only.

<script src="https://gist.github.com/dxh73/199ddd4005e1759effb23ee8ed902f9f.js"></script>

{% include custom/post.consent.html base="https://fhir.nhs.uk/STU3/StructureDefinition/" resource="Consent" content1="POST" text1="https://nww.spine.nhs.uk/4505577104"%}

{% include custom/get.consent.html base="https://fhir.nhs.uk/STU3/StructureDefinition/" resource="Consent" content2="GET" id="133552f9-7aaf-485f-a91a-bdfc0a367409" nhsno="https://nww.spine.nhs.uk/4505577104" text2="NDOP" text3="HRESCH"%}

{% include custom/put.consent.html base="https://fhir.nhs.uk/StructureDefinition/" resource="Consent" content2="PUT" id="133552f9-7aaf-485f-a91a-bdfc0a367409"%}

## Searching National Data Opt-out History ##

{% include custom/history.consent.html base="https://fhir.nhs.uk/STU3/StructureDefinition/" resource="Consent" content2="GET" id="785f7cc6-f63b-41fc-9bd4-2d09df5606f9" text1="https://nww.spine.nhs.uk/4505577104" text2="HRESCH" histid="6ed33184-56ab-450f-98c5-8f86d7310766"%}


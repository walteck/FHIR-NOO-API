---
title: Profile Elements
keywords: elements, consent
tags: [profile,elements,usage]
sidebar: overview_sidebar
permalink: development_elements.html
summary: "Implentation guide on the characteristics and usage of the profiles elements"
---

## Consent Profile Elements ##

|Name|Data Type|Card|Description|
|----|---------|----|-----------|
|[`id`](consent_id.html)|token|1..1|Logical id assigned by the FHIR server|Any UUID|
|[`status`](consent_status.html)|string|1..1|The current status of the consent instance|active,inactive|
|[`category`](consent_category.html)|string|1..1|Category uses the Consent.category element to distinguish the national opt-out consent instances from any other consent instance|NDOP|
|[`patient`](consent_patient.html)|Reference|1..1|Spine reference to the patients NHS number traced from PDS|
|`period`|dateTime|1..1|Period consent commences|
|`dateTime`|dateTime|1..1|Date and time instance was last updated|Date+Time+TimeZone|
|[`consentingParty`](consentingparty.html)|Reference|1..1|Reference to the patient NHS number traced from PDS|
|[`actor`](consent_actor.html)|backbone|0..1|Captures the patient or healthcare professional who controls the consent|N/A|
|`actor.role`|CodeableConcept|1..1|Valueset for the role|INF|
|`actor.reference`|Reference|1..1|URL for the actor|
|[`action`](consent_action.html)|CodeableConcept|1..1|to indicate what actions are controlled by the national opt-out policy|disclose|
|[`organization`](consent_organization.html)|Reference|1..1|ODS code for the organization.|MUST be a URL|
|[`source`](consent_source.html)|Reference|1..1|Capture mechanism used to set the patients preferences|
|[`purpose`](consent_purpose.html)|Coding|1..1|Contains Opt-Out for Research or Commissioning & Planning|HRESCH, HOPERAT|

## Consent Extensions ##

National Data Opt-out Source of Opt-Out extension

`https://fhir.nhs.uk/StructureDefinition/extension-SourceOfOptOut-1`


|Name|Data Type|Card|Description|
|----|---------|----|-----------|
|[`sourceofoptout`](consent_extension_sourceofoptout.html)|extension|1..1|Extension to capture the source that defined the national opt-out preferences e.g NHS Choice, GP System|


## FHIR&reg; RESTful API Examples ##

**XML Example 1**

The example below demonstrates the structure of a constructed XML body that can be submitted to the National Data Opt-out service via a HTTP POST. This will set the preferences for HRESCH only.

{% include custom/post.consent.html base="https://fhir.nhs.uk/StructureDefinition/" resource="consent" content1="POST" text1="https://nww.spine.nhs.uk/4505577104" %}

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Consent xmlns="http://hl7.org/fhir" xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://hl7.org/fhir ../Schemas/consent.xsd">
	<id value="783ffeef-538e-4a17-bed2-983a382ccdd7"/>
	<meta>
		<profile value="https://fhir.nhs.uk/StructureDefinition/noom-consent-1"/>
	</meta>
	<status value="inactive"/>
	<category>
		<coding>
			<system value="https://fhir.nhs.uk/ValueSet/noom-category-type-1"/>
			<code value="NDOP"/>
		</coding>
	</category>
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
            <reference value="https://nww.spine.nhs.uk/4505577104"/>
        </reference>
    </actor>
    <policyRule value="http://hl7.org/fhir/ConsentPolicy/opt-out"/>
    <purpose> 
        <system value="http://hl7.org/fhir/v3/ActReason"/> 
        <code value="HOPERAT"/>
        <display value="healthcare operations"/>
    </purpose>
</Consent>
```

{% include custom/get.consent.html base="https://fhir.nhs.uk/StructureDefinition/" resource="consent" content2="GET" text1="https://nww.spine.nhs.uk/4505577104" text2="NDOP" text3="HRESCH"%}

{% include custom/put.consent.html base="https://fhir.nhs.uk/StructureDefinition/" resource="consent" content2="PUT" text2="https://nww.spine.nhs.uk/4505577104" %}

## Searching National Data Opt-out History ##

{% include custom/history.consent.html base="https://fhir.nhs.uk/StructureDefinition/" resource="consent" content2="GET" id="785f7cc6-f63b-41fc-9bd4-2d09df5606f9" text1="https://nww.spine.nhs.uk/4505577104" text2="HRESCH" %}




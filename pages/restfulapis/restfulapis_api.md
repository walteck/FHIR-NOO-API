---
title: RESTful API
keywords: getcarerecord, structured, rest, resource
tags:
- structured
- getcarerecord
sidebar: overview_sidebar
permalink: restfulapis_api.html
summary: Overview
---

## FHIR&reg; RESTful API ##


**XML Example 1**

The example below demonstrates the structure of a constructed XML body that can be submitted to the National Data Opt-out service via a HTTP POST RESTful command where both opt-out questions are stored in one XML body.

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Consent xmlns="http://hl7.org/fhir" xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://hl7.org/fhir ../Schemas/consent.xsd">
	<id value="783ffeef-538e-4a17-bed2-983a382ccdd7"/>
	<meta>
		<!--Identifies the profile being used-->
		<profile value="https://fhir.nhs.uk/StructureDefinition/noom-consent-1"/>
	</meta>
	<identifier>
		<value value="311fcae7-32a7-4a8e-a15c-eebae3a246b9"/>
	</identifier>
	<status value="active"/>
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
        <code value="HRESCH"/>
        <display value="healthcare research"/>
    </purpose>
</Consent>
```

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
{% include custom/post.consent.html base="https://fhir.nhs.uk/StructureDefinition/" resource="consent" content2="POST" %}

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Consent xmlns="http://hl7.org/fhir" xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://hl7.org/fhir ../Schemas/consent.xsd">
	<id value="57449861-1dab-42ce-870a-3540dc2890d3"/>
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
{% include custom/post.op.consent.html base="https://fhir.nhs.uk/StructureDefinition/" resource="consent" content2="POST" %}


{% include custom/get.consent.html base="https://fhir.nhs.uk/StructureDefinition/" resource="consent" content2="GET" text1="783ffeef-538e-4a17-bed2-983a382ccdd7" text2="NDOP" %}

{% include custom/put.consent.html base="https://fhir.nhs.uk/StructureDefinition/" resource="consent" content2="PUT" text1="783ffeef-538e-4a17-bed2-983a382ccdd7" %}

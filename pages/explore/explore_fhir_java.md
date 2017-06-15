---
title: FHIR Java Client
keywords: client, C#
tags: [profile,elements,usage]
sidebar: overview_sidebar
permalink: explore_fhir_java.html
summary: "FHIR Java client using HAPI NET"
---

{% include tip.html content="Java code snippets utilise James Agnew's Open Source HAPI FHIR Client [HAPI FHIR](https://github.com/jamesagnew/hapi-fhir)" %}

## Creating Consent Instance ##


```java
//Create the consent instance
//
Consent consent = new Consent();
consent.addstatus()
	.setValue("active");
consent.addCategory()
	.setSystem("https://fhir.nhs.uk/ValueSet/noom-category-type-1")
	.setCode("NOOM");
consent.addPatient()
	.setReference("https://nww.spine.nhs.uk/4505577104");
consent.addconcentingParty()
	.setReference("https://nww.spine.nhs.uk/4505577104");
consent.addActor()
	.setcoding()
		.setSystem("http://hl7.org/fhir/v3/ParticipationType")
		.setCode("INF");
	.setReference("https://nww.spine.nhs.uk/4505577104");
consent.addpolicyRule()
	.setValue=(""http://hl7.org/fhir/ConsentPolicy/opt-out");
consent.addPurpose()
	.setSystem("http://hl7.org/fhir/v3/ActReason")
	.setCode("HRESCH")
	.setDisplay("healthcare research");
```
## Establish a connection to a FHIR Server ##

```java
//Connect to NHS FHIR server (STU3)
//
FhirContext ctx = FhirContext.stu3();
String serverBase = "http://fhir.nhs.uk"
IGenericClient client = ctx.newRestfulGenericClient(serverBase);
```

## Submit to instance to FHIR server ##

```java 
//Perform a create (POST)
MethodOutcome outcome = client.create()
	.resource(consent)
	.execute();
```


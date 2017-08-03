---
title: National Data Opt-out | Reference
keywords: development Reference
tags: [development]
sidebar: overview_sidebar
permalink: development_deliverables.html
summary: "Developer Cheat Sheet shortcuts for the <br/>technical build of National Data Opt-out API."
---

{% include information.html content="Simplifier.net is used to as a temporary solution to provide rendered profiles until developer network is updated to support STU3 profiles"%}

# National Data Opt-out Profiles:

| Profile | ValueSets |
| :--------- |:-------- |
| [NDOP-Consent-1](https://simplifier.net/TestNationalOptOutPr/NDOP-Consent-1xml) | 
| [OperationOutcome-1](https://simplifier.net/TestNationalOptOutPr/NDOP-Consent-1xml) | 

# National Data Opt-out Extensions
|Extension|
|---------|
| [Extension-ActorPerson-1](https://simplifier.net/NOOM/extension-actorperson-1)|
| [Extension-Extension-Opt-out-Source-1](https://simplifier.net/NOOM/extension-optoutsource-1)

# Identifiers #

| identifier | URI | Comment |
|--------------------------------------------|----------|----|
| `Logical ID` | https://fhir.nhs.uk/Consent/[id] | Consent record identifier |
| `Patient` | https://proxy.pds.nhs.uk | Patient |
| `consentingParty` | https://proxy.sds.nhs.uk | Patient |
|`actor`|https://proxy.sds.nhs.uk or https://proxy.pds.nhs.uk | Patient or Practitioner|
|`organization`|https://proxy.sds.nhs.uk |NHS Digital|



{% include warning.html content="The URI's for PDS and SDS are not confirmed and are subject to change." %}
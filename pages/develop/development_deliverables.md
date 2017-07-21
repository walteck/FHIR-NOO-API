---
title: National Data Opt-out | Reference
keywords: development Reference
tags: [development]
sidebar: overview_sidebar
permalink: development_deliverables.html
summary: "Developer Cheat Sheet shortcuts for the <br/>technical build of National Data Opt-out API."
---

# National Data Opt-out Profiles:

| Profile | ValueSets |
| :--------- |:-------- |
| [NDOP-Consent-1](https://simplifier.net/TestNationalOptOutPr/NDOP-Consent-1xml) | 

# Identifiers #

| identifier | URI | Comment |
|--------------------------------------------|----------|----|
| `Logical ID` | https://fhir.nhs.uk/Consent/[id] | Consent record identifier |
| `Patient` | https://proxy.pds.nhs.uk | Patient |
| `consentingParty` | https://proxy.sds.nhs.uk | Patient |
|`actor`|https://proxy.sds.nhs.uk or https://proxy.pds.nhs.uk | Patient or Practitioner|
|`organization`|https://proxy.sds.nhs.uk |NHS Digital|



{% include warning.html content="The URI's for PDS and SDS are not confirmed and are subject to change." %}
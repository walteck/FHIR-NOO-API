---
title: Interactions
keywords: interaction, consent
tags: [interaction]
sidebar: overview_sidebar
permalink: development_interactions.html
summary: "National Opt-Out Spine Interactions"
---

## NOOM API Overview ##

This section provides National Opt-Out (NOOM) implementers with an overview of the NOOM API messaging interface also known as the ‘National Opt-Out Service’.

The NOOM API supports the following functionality:

POST patient NOOM preferences
GET existing patient NOOM preferences
PUT patient updated NOOM preferences

The NOOM API is based on the HL7 FHIR STU3 3.0.1 Messaging Implementation (April 2017).

## National Opt-Out Spine RESTful Interaction Diagram ##

<img src="images/NOOMInteractions.png">


## Register Patients National Opt-Out Preferences Interaction ##

The client system will construct a XML body containing NOOM preferences and submit this to the ACS via Spine services using a RESTful create interaction.

- ***Sender:*** Any NOOM client
- ***Receiver:*** Spine 2
- ***RESTful API Interaction:*** POST [base]/consent

**Responses**

Assuming successful URL submission, there are several possible responses to the NOOM request:
- 
- HTTP 201-Record Created: The entry has been successfully created and the NOOM returns an HTTP Location header containing the 'server' assigned logical Id of the created resource.
- HTTP 400-Bad Request: Resource could not be parsed or failed basic FHIR validation rules
- HTTP 404-Not Found: Resource type not supported, or not a FHIR end-point
- HTTP 422-Unprocessable Entity: The proposed resource violated applicable FHIR profiles or server business rules.

## Retrieve Patients National Opt-Out Preferences Interaction ##

The client system will perform a RESTful search interaction for current patient preferences located on the National Opt-Out service.

- ***Sender:***Any NOOM Client
- ***Receiver:***Spine 2
- ***RESTful API Interaction:***GET [base]/consent[parameters] 

**Responses**

The search results **shall** return one or two instances of the patients National Opt-Out preferences, depending on search parameters utilized. Instances **shall** be one of the following preferences:

- HRESCH - Research Opt-Out
- HOPERAT - Planning and Commissioning Opt-Out

Assuming successful URL submission, there is one possible outcome to a search request:

- HTTP 200-Request was successfully executed

The NOOM FHIR server determines which of the set of resources it serves meet the specific criteria, and returns the results of the search in the HTTP response as a 'searchset' bundle.

Note: Although an HTTP response 200 OK indicates the request was successful, the bundle could return a 0 (zero) total value indicating no record was found. This is an XML example of the Bundle with a 0 (zero) total value indicating no record was found.

## Update Patients National Opt-Out Preferences Interaction ##

The client system will perform a RESTful update interaction to amend the patients National Opt-Out preferences and submit a revised body to to the NOOM service.

- ***Sender:***Any NOOM Client
- ***Receiver:***Spine 2
- ***RESTful API Interaction:***GET [base]/consent[parameters] 

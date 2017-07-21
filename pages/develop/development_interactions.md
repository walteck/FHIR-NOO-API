---
title: Interactions
keywords: interaction, consent, NDOP
tags: [interaction]
sidebar: overview_sidebar
permalink: development_interactions.html
summary: "National Data Opt-out Spine Interactions"
---

## National Data Opt-out Spine RESTful Interaction Diagram ##

<img src="images/NDOPInteractions2.png">


## Register Patients National Data Opt-out Preferences Interaction ##

The client system will construct a XML body containing NDOP preferences and submit this to the ACS via Spine services using a RESTful create interaction.

- ***Sender:*** Any NDOP client
- ***Receiver:*** Spine 2
- ***RESTful API Interaction:*** POST https://[baseurl]/Consent

{% include note.html content="The baseurl is typically a fully qualified domain name (FQDN) but may on occasion consist of other path elements to uniquely identify the endpoint." %}

{% include note.html content="Details on the FHIR RESTful specification for creating a new instance can be found here [RESTful Create](https://www.hl7.org/fhir/http.html#create)" %}

---
**Responses**

Assuming successful URL submission, there are several possible responses to the NDOP request:

- HTTP 201-Record Created: The entry has been successfully created and the NDOP returns an HTTP Location header containing the 'server' assigned logical Id of the created resource.
- HTTP 400-Bad Request: Resource could not be parsed or failed basic FHIR validation rules
- HTTP 422-Unprocessable Entity: The proposed resource violated applicable FHIR profiles or server business rules.

## Retrieve Patients National Data Opt-out Preferences Interaction ##

The client system will perform a RESTful search interaction for current patient preferences located on the National Data Opt-out service.

- ***Sender:***Any NDOP Client
- ***Receiver:***Spine 2
- ***RESTful API Interaction:***GET https://[baseurl]/Consent[parameters] 


{% include note.html content="Details on the FHIR RESTful specification for reading an instance can be found here [RESTful Read](https://www.hl7.org/fhir/http.html#read)" %}
---
**Responses**

The search results **shall** return one or two instances of the patients National Data Opt-out preferences, depending on search parameters utilized. Each instance **shall** have one of the following preferences:

- HRESCH - Research Opt-Out
- HOPERAT - Planning and Commissioning Opt-Out

Assuming successful URL submission, there is one possible outcome to a search request:

- HTTP 200-Request was successfully executed

The NDOP FHIR server determines which of the set of resources it serves meet the specific criteria, and returns the results of the search in the HTTP response as a 'searchset' bundle or where a specific logical ID forms the only search parameter, as single consent resource.

Note: Although an HTTP response 200 OK indicates the request was successful, the bundle could return a 0 (zero) total value indicating no record was found. Below is an XML example of a Bundle with a 0 (zero) total value indicating no record was found. 

```xml
<?xml version="1.0" encoding="UTF-8"?>
<Bundle xmlns="http://hl7.org/fhir">
    <id value="cb176b22-5b78-4b88-8c6a-adca33ebc3"/>
    <meta>
    <lastUpdated value="2017-07-17T12:39:43Z"/>
    </meta>
    <type value="searchset"/>
    <total value="0"/>
    <link>
    <relation value="self"/>
    <url value="http://test.fhir.org/r3/Consent?search-id=08da8bc9-689a-40fc-b414-c63acf1056&amp;&amp;patient=https%3A//nww.spine.nhs.uk/4505577104&amp;category=NOOM&amp;_sort=_id"/>
    </link>
</Bundle>
```

## Update Patients National Data Opt-out Preferences Interaction ##

The client system will perform a RESTful update interaction to amend the patients National Data Opt-out preferences and submit a revised body to the NDOP service.

- ***Sender:***Any NDOP Client
- ***Receiver:***Spine 2
- ***RESTful API Interaction:***PUT https://[baseurl]/Consent[parameters] 

{% include note.html content="Details on the FHIR RESTful specification for creating a new instance can be found here [RESTful Update](https://www.hl7.org/fhir/http.html#update)" %}

**Responses**

Assuming success, there are several possible responses to the NDOP request:

- HTTP 200-OK: The entry has been successfully updated and the NDOP returns an HTTP Location header containing the 'server' assigned logical Id of the updated resource.
- HTTP 400-Bad Request: Resource could not be parsed or failed basic FHIR validation rules
- HTTP 422-Unprocessable Entity: The proposed resource violated applicable FHIR profiles or server business rules.

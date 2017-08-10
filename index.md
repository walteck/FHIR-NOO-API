---
title: Introduction to National Data Opt-out Programme
keywords: ndop, opt-out
tags: [getting_started]
sidebar: overview_sidebar
permalink: index.html
toc: true
summary: A brief introduction to getting started with the National Data Opt-out Programme FHIR&reg; API
---

{% include important.html content="This site is under active development by the interoperability messaging team and is intended to provide all the technical resources you need to successfully deploy a National Data Opt-out Programme Profile. Some areas are being formulated and iterative updates to content will be added on a regular basis." %}

{% include warning.html content="This site is provided for information only and is intended for those engaged with NHS Digital in the development of the National Data Opt-out Programme FHIR&reg; API. It is advised not to develop against these specifications until a formal announcement has been made." %}

# Background #

The National Data Opt-out Programme (NDOP) is a product of the National Data Guardian (NDG) review on data security and how individuals data is used and shared by healthcare organizations.  NDOP has been created to provide a model that will allow each individual citizen to have control over specific data, being able to choose the type of data that can be shared.

The current incarnation of NDOP will provide a mechanism to citizens registered with a GP in England to choose if they wish to share the following data:

- Data for use within Planning and Commissioning
- Data for use within research


The initial phase will provide an online portal which citizens can access via a web browser to set their data sharing preferences. Additional mechanisms will be introduced at a later date, including updating GP Systems, mobile devices and off-line systems. It is anticipated that the online portal will be available in September 2017.

## National Data Opt-out Programme API ##

The National Data Opt-out Programme requires an API to capture the preferences chosen via the online portal and transfer these preferences to a centralized data store located on Spine. The API messaging will use the HL7 FHIR&reg; messaging standard to enable preferences to be created, retrieved and updated via it's own RESTful API. FHIR RESTful API performs transactions using HTTP request/response, allowing rapid development of applications using the NDOP API.

The NDOP API is relatively lightweight in its design, made up of limited limited components, making it easy to maintain and deploy.


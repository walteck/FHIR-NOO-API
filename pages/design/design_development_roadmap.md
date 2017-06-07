---
title: Development Roadmap
keywords: development,
tags: [engage,development,fhir]
sidebar: overview_sidebar
permalink: design_development_roadmap.html
summary: National Opt-Out API roadmap outlines the development schedule for the RESTful APIs.

---

[<i class="fa fa-arrow-left" aria-hidden="true"/> Back to Care Connect API - Introduction.](index.html)

{% include important.html content="All development phases outlined below are indicative and subject to on-going review." %}

## Exploration ##

### Proposed High Level Design ###

<img src="images/noom_high_level_design.png" style="width:100%;max-width: 100%;">

1. NHS.uk will be the patient facing opt-out solution with GP on-line systems to follow.
2. 3rd party route provides patients an assisted service for setting opt-out preferences either via GP practice staff or via a national back office solution. 
3. NHS Number will be used to match a user identity to a user transaction.
4. NHS Digital systems that stored Type 2 preferences, will be upgraded to interface with the National Opt-Out Model. 
5. Opt-Out preferences will be stored on Spine ACS.
6. Bloom filter used to extract dissented patients from Spine ACS into a flat file which will be encrypted and compressed. This will then be made available over MESH.
7. Local and central solutions that already incorporate the Bloom filter.

{% include important.html content="This diagram and its associated descriptions are subject to change as the National Opt-Out Model solution evolves." %}
---
title: FHIR Python Client
keywords: client, C#
tags: [profile,elements,usage]
sidebar: overview_sidebar
permalink: explore_fhir_python.html
summary: "FHIR Python client using Smart on FHIR"
---

## Establish connection to FHIR Server ##

```python
from fhirclient import client
settings = {
    'app_id': 'NDOP',
    'api_base': 'https://fhir.nhs.uk'
}
smart = client.FHIRClient(settings=settings)
```


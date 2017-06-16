---
title: FHIR JavaScript Client
keywords: client, javascript
tags: [JavaScript,client,usage]
sidebar: overview_sidebar
permalink: explore_fhir_js.html
summary: "FHIR JavaScript client using Smart on FHIR"
---

## Initialize the client ##

```javascript
FHIR.oauth2.ready(function(smart){
    // add code
});
```

```javascript
var entry = {
  category: [{term: 'TAG term', schema: 'TAG schema', label: 'TAG label'}, ...]
  resource: {
    resourceType: 'Consent',
    //...
  }
}

myClient.create(entry,
 function(entry){
    console.log(entry.id)
 },
 function(error){
   console.error(error)
 }
)
```

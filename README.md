## Background

### What is the Zynx Health API and FHIR?
The Zynx Health API provides access to Zynx Content in the FHIR standard format.
[FHIR (Fast Healthcare Interoperability Resources)](http://hl7.org/fhir/summary.html) is a specification for exchanging healthcare data in a modern and developer-friendly way.
<br>
<br>
## Table of Contents

1. [What's New](#new)
2. [Clinical  Decision Support Content](#CDS)
3. [Getting Started](#start)
   1. [Get your API Key](#getkey)
   2. [Make API Calls](#makecalls)
   3. [Stay Updated](#stayupdated)
<br><br>

## What's New<a id="new"></a>

| Date       | Description     |
| :--------- | :-------------- |
| 06.14.2017 | Initial release |
| 07.06.2017 | Added search examples page |
| 07.17.2017 | Updated Clinical Decision Support Content Schedule |
| 08.01.2017 | Added Clinical Glossary |
| 09.07.2017 | Updated for Beta.1 Status* |

<br>* **We will contact you if you who were previously issued API keys prior to 09.07.2017. The previously issued API keys will continue to work according to the [prior instructions](./archive/20170907/README.md) for a limited time. They will no longer be valid after 9/15/2017.**
<br>

## Clinical Decision Support Content<a id="CDS"></a>
### Early Access
**Content**|**Type**|**Status**|**Pricing**|**ID**
:-----:|:-----:|:-----:|:-----:|:---:
Asthma - Admission to ICU|Order Set|Available Now|Free for approved developers. See developer license agreement for terms.|c1d06f95-c9f4-436d-ae8b-4de9c141867b
Transition of Care - General|Plan of Care|Available Now|Free for approved developers. See developer license agreement for terms.|6d1b044e-17ae-4b72-9e26-f62e187e4e4b

For a glossary of clinical terms and Zynx product offerings, [click here](./clinical-glossary.md).

### Premium
**Product**|**Type**|**Status**|**Pricing**
:-----:|:-----:|:-----:|:-----:
ZynxOrder<br/>[400+]|Order Set|Estimated September 2017|Requires paid license.
ZynxCare<br/>[300+]|Plan of Care|Estimated October 2017|Requires paid license.

For a glossary of clinical terms and Zynx product offerings, [click here](./clinical-glossary.md).
<br><br>

## Getting Started<a id="start"></a>

### 1. Get your API Key<a id="getkey"></a>
Each organization will need their own API key. If you haven't done so already, [apply for a key](http://www.zynxhealth.com/news-resources/developer/#apply).
> Wherever `API_KEY` is referenced below, replace it with the unique key that was emailed to you.
<br>

### 2. Make API Calls<a id="makecalls"></a>

#### A. Use [RESTful API](http://hl7.org/fhir/http.html)

| Field | Description                              | Acceptable Value(s)                      |
| :---- | :--------------------------------------- | :--------------------------------------- |
| base  | Zynx Health API [Service Base URL](http://hl7.org/fhir/http.html#general) | `https://api-gw-beta1.cb.zynx.com/t/zynx.com/connect/1.0.0/` |
| type  | Resource type                 | `PlanDefinition` [`order-sets`, `plans-of-care`]   |
| id    | Logical identity of the resource         | `c1d06f95-c9f4-436d-ae8b-4de9c141867b`                             |

<br>

Presently one resource type will be exposed with Zynx content via the RESTful API of the FHIR workflow module/clinical process:
 - [`PlanDefinition`](http://hl7.org/fhir/plandefinition.html): This resource allows for the definition of various types of plans as a sharable, consumable, and executable artifact. The resource is general enough to support the description of a broad range of clinical artifacts such as clinical decision support rules, order sets and protocols.

##### Example Requests

> Wherever `API_KEY` is referenced below, replace it with the unique key that was emailed to you.
> 
> Examples for provide for both JSON and XML.  Just update the Accept header.

###### Order Sets
```
curl --request GET \
--header 'Authorization: Bearer API_KEY' \
--header 'Accept: application/json' \
--header 'cache-control: no-cache' \
https://api-gw-beta1.cb.zynx.com/t/zynx.com/connect/1.0.0/order-sets/c1d06f95-c9f4-436d-ae8b-4de9c141867b

curl --request GET \
--header 'Authorization: Bearer API_KEY' \
--header 'Accept: application/xml' \
--header 'cache-control: no-cache' \
https://api-gw-beta1.cb.zynx.com/t/zynx.com/connect/1.0.0/order-sets/c1d06f95-c9f4-436d-ae8b-4de9c141867b
```
###### Plans of Care
```
curl --request GET \
--header 'Authorization: Bearer API_KEY' \
--header 'Accept: application/json' \
--header 'cache-control: no-cache' \
https://api-gw-beta1.cb.zynx.com/t/zynx.com/connect/1.0.0/plans-of-care/6d1b044e-17ae-4b72-9e26-f62e187e4e4b

curl --request GET \
--header 'Authorization: Bearer API_KEY' \
--header 'Accept: application/xml' \
--header 'cache-control: no-cache' \
https://api-gw-beta1.cb.zynx.com/t/zynx.com/connect/1.0.0/plans-of-care/6d1b044e-17ae-4b72-9e26-f62e187e4e4b
```

###### Postman GUI REST API tool
For instructions about using the Postman GUI REST API tool, [click here](./gui-api-request.md).


#### C. More Information
| Resource Type      |             Resource Content             |                XML Schema                |               JSON Schema                |              Search Params               |
| :----------------- | :--------------------------------------: | :--------------------------------------: | :--------------------------------------: | :--------------------------------------: |
| PlanDefinition     | [RC](http://hl7.org/fhir/plandefinition.html#resource) | [XML](http://hl7.org/fhir/plandefinition.xsd) | [JSON](http://hl7.org/fhir/PlanDefinition.schema.json) | [Search](http://hl7.org/fhir/plandefinition.html#search) |
<br>

### 3. Stay Updated<a id="stayupdated"></a>
Since the Zynx Health API is actively being developed, follow this page to keep up-to-date with the changes.

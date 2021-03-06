## Background

### What is the Zynx Health API and FHIR?
The Zynx Health API provides access to Zynx Content in the FHIR standard format.
[FHIR (Fast Healthcare Interoperability Resources)](http://hl7.org/fhir/summary.html) is a specification for exchanging healthcare data in a modern and developer-friendly way.
<br>
<br>
## Table of Contents

1. [What's New](#new)
2. [Beta 2 Release Notes](#beta2)
3. [Clinical  Decision Support Content](#CDS)
   1. [Clinical Glossary](./clinical-glossary.md)
4. [Getting Started](#start)
   1. [Get your API Key](#getkey)
   2. [Make API Calls](#makecalls)
   3. [Stay Updated](#stayupdated)
<br><br>

## <a id="new"></a>What's New

| Date       | Description     |
| :--------- | :-------------- |
| 10.25.2017 | Added information for Zynx's Value Set|
| 10.27.2017 | Beta 2 Release* |

<br>* **You will be contacted if you who were previously issued API keys for beta 1. The previously issued API keys will continue to work according to the [prior instructions](./archive/20171027/README.md) for a limited time. Beta 1 will no longer be available after 11/3/2017.**
<br>

## <a id="beta2"></a>Beta 2 Release Notes

API Additions and Changes:

* The API now implements the PlanDefinition resource (previously there were separate order-sets and plans-of-care resources)
	* The type is specified within the PlanDefinition as documented [here](http://build.fhir.org/plandefinition-definitions.html#PlanDefinition.type)
* Limited [search on focus and venue](./search.md) have been added. Currently requires the usage of the Ids for the [focus](focus_id.md) and [venue](venue_id.md).

PlanDefinition Content Additions:

* The PlanDefinitions now contain performance measure information associated to actions.

Known Minor Issues:

* Copyright symbol is not encoded properly, however it is in the copyright element so it is still clear that it is a copyright.
* Paging URL in Bundle not currently correct, it excludes PlanDefinition resource name. Paging not functional.

Future Work NOT in Beta 2

* Expect continued implementation of additional search features in FHIR. Including Paging.
* Implementation of "metadata" endpoint with CapabilityStatement.
* Specification of profile for search on focus and venue.
* We are committed to implementing the applicable portions of the FHIR standard as it relates to our Clinical Content.

## <a id="CDS"></a>Clinical Decision Support Content
### Early Access
**Content**|**Type**|**Status**|**Pricing**|**ID**
:-----:|:-----:|:-----:|:-----:|:---:
Asthma - Admission to ICU|Order Set|Available Now|Free for approved developers. See developer license agreement for terms.|c1d06f95-c9f4-436d-ae8b-4de9c141867b
Transition of Care - General|Plan of Care|Available Now|Free for approved developers. See developer license agreement for terms.|6d1b044e-17ae-4b72-9e26-f62e187e4e4b

For a glossary of clinical terms and Zynx product offerings, [click here](./clinical-glossary.md).

### Premium
**Product**|**Type**|**Status**|**Pricing**
:-----:|:-----:|:-----:|:-----:
ZynxOrder<br/>[400+]|Order Set|Available Now|Requires paid license.
ZynxCare<br/>[300+]|Plan of Care|Available Now|Requires paid license.

For a glossary of clinical terms and Zynx product offerings, [click here](./clinical-glossary.md).
<br><br>

## <a id="start"></a>Getting Started

### <a id="getkey"></a>1. Get your API Key
Each organization will need their own API key. If you haven't done so already, [apply for a key](http://www.zynxhealth.com/news-resources/developer/#apply).
> Wherever `API_KEY` is referenced below, replace it with the unique key that was emailed to you.

### 2. SMART on FHIR demonstration app using Zynx API.

[Get the code](https://github.com/zynxhealth/api-demo) for the demonstration app.
<br>

### <a id="makecalls"></a>3. Make API Calls

#### A. Use [RESTful API](http://hl7.org/fhir/http.html)

| Field | Description                              | Acceptable Value(s)                      |
| :---- | :--------------------------------------- | :--------------------------------------- |
| base  | Zynx Health API [Service Base URL](http://hl7.org/fhir/http.html#general) | `https://api-gw-beta2.cb.zynx.com/t/zynx.com/connect/1.0.0/` |
| type  | Resource type                 | `PlanDefinition`    |
| id    | Logical identity of the resource         | `c1d06f95-c9f4-436d-ae8b-4de9c141867b`                             |

<br>

Presently one resource type will be exposed with Zynx content via the RESTful API of the FHIR workflow module/clinical process:
 - [`PlanDefinition`](http://hl7.org/fhir/plandefinition.html): This resource allows for the definition of various types of plans as a sharable, consumable, and executable artifact. The resource is general enough to support the description of a broad range of clinical artifacts such as clinical decision support rules, order sets and protocols.

##### Example Requests

> Wherever `API_KEY` is referenced below, replace it with the unique key that was emailed to you.
> 
> Examples are provided for both JSON and XML.  Just update the Accept header.

###### Order Sets
```
curl --request GET \
--header 'Authorization: Bearer API_KEY' \
--header 'Accept: application/json' \
--header 'cache-control: no-cache' \
https://api-gw-beta2.cb.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition/c1d06f95-c9f4-436d-ae8b-4de9c141867b

curl --request GET \
--header 'Authorization: Bearer API_KEY' \
--header 'Accept: application/xml' \
--header 'cache-control: no-cache' \
https://api-gw-beta2.cb.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition/c1d06f95-c9f4-436d-ae8b-4de9c141867b
```
###### Plans of Care
```
curl --request GET \
--header 'Authorization: Bearer API_KEY' \
--header 'Accept: application/json' \
--header 'cache-control: no-cache' \
https://api-gw-beta2.cb.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition/6d1b044e-17ae-4b72-9e26-f62e187e4e4b

curl --request GET \
--header 'Authorization: Bearer API_KEY' \
--header 'Accept: application/xml' \
--header 'cache-control: no-cache' \
https://api-gw-beta2.cb.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition/6d1b044e-17ae-4b72-9e26-f62e187e4e4b
```

###### Postman GUI REST API tool
For instructions about using the Postman GUI REST API tool, [click here](./gui-api-request.md).


#### C. More Information
| Resource Type      |             Resource Content             |                XML Schema                |               JSON Schema                |              Search Params               |
| :----------------- | :--------------------------------------: | :--------------------------------------: | :--------------------------------------: | :--------------------------------------: |
| PlanDefinition     | [RC](http://hl7.org/fhir/plandefinition.html#resource) | [XML](http://hl7.org/fhir/plandefinition.xsd) | [JSON](http://hl7.org/fhir/PlanDefinition.schema.json) | [Search](http://hl7.org/fhir/plandefinition.html#search) |

###### Zynx's Value Set for Content Item Types
| Text or Display Value   | Code Value    |   Explanation |
| :---------------- | :-----------: | :---------- |
| Section       | 2             | A category used to organize order items ([view full explanation](https://github.com/zynxhealth/documentation/blob/master/clinical-glossary.md#section))|
| Orderable (Med)  | 3          | Drug names that can be expressed as medication names or dispensable products ([view full explanation](https://github.com/zynxhealth/documentation/blob/master/clinical-glossary.md#medication))|
| Reminder | 4          | An evidence-based note to the clinician at the point of care ([view full explanation](https://github.com/zynxhealth/documentation/blob/master/clinical-glossary.md#reminder))|
|Orderable | 5| Non-medication items that can be ordered by a clinician (e.g. nursing orders, laboratory tests, radiology, etc) ([view full explanation](https://github.com/zynxhealth/documentation/blob/master/clinical-glossary.md#orderable))|
|Problem|8| A condition experienced by a patient that can be treated in a clinical care setting ([view full explanation](https://github.com/zynxhealth/documentation/blob/master/clinical-glossary.md#problem))|
|Outcome|10| Measurable patient-centered conditions/states, behaviors, or perceptions in response to interdisciplinary interventions ([view full explanation](https://github.com/zynxhealth/documentation/blob/master/clinical-glossary.md#outcome))|
|Activity|12|A specific action that the interdisciplinary care team carries out to address a patient problem ([view full explanation](https://github.com/zynxhealth/documentation/blob/master/clinical-glossary.md#activity))|
|Activitylet|15|Further description or clarification of key concepts for an activity in a plan of care.


### <a id="stayupdated"></a>4. Stay Updated
Since the Zynx Health API is actively being developed, follow this page to keep up-to-date with the changes.

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
<br>

## Clinical Decision Support Content<a id="CDS"></a>
**Content**|**Type**|**Status**|**Product**|**ID**
:-----:|:-----:|:-----:|:-----:|:---:
Asthma - Admission to ICU|Order Set|Available Now|Free for approved developers. See developer license agreement for terms.|ZynxOS-795
Heart Failure Home Health|Plan of Care|Available Now|Requires paid license.
Transition of Care - General|Plan of Care|Available August 1, 2017|Free for approved developers. See developer license agreement for terms.|ZynxPOC-TransitionofCare-General-3811
ZynxOrder Content|Order Set|Estimated September 2017|Requires paid license.
Heart Failure Case Management|Plan of Care|Available September 30, 2017|Requires paid license.
ZynxCare Content|Plan of Care|Estimated October 2017|Requires paid license.

For a glossary of clinical terms and Zynx product offerings, [click here](../../clinical-glossary.md).
<br><br>

## Getting Started<a id="start"></a>

### 1. Get your API Key<a id="getkey"></a>
Each organization will need their own API key. If you haven't done so already, [apply for a key](http://www.zynxhealth.com/news-resources/developer/#apply).
> Wherever `API_KEY` is referenced below, replace it with the unique key that was emailed to you.
<br>

### 2. Make API Calls<a id="makecalls"></a>

#### A. Use [RESTful API](http://hl7.org/fhir/http.html)

>```VERB [base]/[type]/[id] {?_format=[mime-type]}```

| Field | Description                              | Acceptable Value(s)                      |
| :---- | :--------------------------------------- | :--------------------------------------- |
| base  | Zynx Health API [Service Base URL](http://hl7.org/fhir/http.html#general) | `https://api.cb.zynx.com/dev-v0/fhir-a/baseDstu3` |
| type  | Resource type (see below)                | `ActivityDefinition`, `PlanDefinition`   |
| id    | Logical identity of the resource         | `ZynxOS-795`                             |

Content surrounded by [] is mandatory, and will be replaced by acceptable values.
Content surrounded by {} is optional.
<br>
<br>

Presently two resource types will be exposed with Zynx content via the RESTful API of the FHIR workflow module/clinical process:
 - [`ActivityDefinition`](http://hl7.org/fhir/activitydefinition.html): This resource allows for the definition of some activity to be performed, independent of a particular patient, practitioner, or other performance context.
 - [`PlanDefinition`](http://hl7.org/fhir/plandefinition.html): This resource allows for the definition of various types of plans as a sharable, consumable, and executable artifact. The resource is general enough to support the description of a broad range of clinical artifacts such as clinical decision support rules, order sets and protocols.

##### Example Request

> Wherever `API_KEY` is referenced below, replace it with the unique key that was emailed to you.

```
curl --request GET \
  --url https://api.cb.zynx.com/dev-v0/fhir-a/baseDstu3/PlanDefinition/ZynxOS-795 \
  --header 'cache-control: no-cache' \
  --header 'x-api-key: API_KEY'
```
<br>

#### B. Search with RESTful API
For more information about how to search with the RESTful API, [click here](https://www.hl7.org/fhir/search.html).

##### Example Search Requests
Detailed search examples [click here](./search-examples.md).

> Wherever `API_KEY` is referenced below, replace it with the unique key that was emailed to you.

###### Search for PlanDefinition with cURL
```
curl --request GET \
  --url 'https://api.cb.zynx.com/dev-v0/fhir-a/baseDstu3/PlanDefinition?_lastUpdated=gt2017-03-01&_lastUpdated=lt2017-04-05&_format=json&_pretty=true&_summary=text' \
  --header 'cache-control: no-cache' \
  --header 'x-api-key: API_KEY'
```

###### Search for PlanDefinition with Postman GUI REST API tool
For instructions about using the Postman GUI REST API tool, [click here](./gui-api-request.md).

<br>

#### C. More Information
| Resource Type      |             Resource Content             |                XML Schema                |               JSON Schema                |              Search Params               |
| :----------------- | :--------------------------------------: | :--------------------------------------: | :--------------------------------------: | :--------------------------------------: |
| ActivityDefinition | [RC](http://hl7.org/fhir/activitydefinition.html#resource) | [XML](http://hl7.org/fhir/activitydefinition.xsd) | [JSON](http://hl7.org/fhir/ActivityDefinition.schema.json) | [Search](http://hl7.org/fhir/activitydefinition.html#search) |
| PlanDefinition     | [RC](http://hl7.org/fhir/plandefinition.html#resource) | [XML](http://hl7.org/fhir/plandefinition.xsd) | [JSON](http://hl7.org/fhir/PlanDefinition.schema.json) | [Search](http://hl7.org/fhir/plandefinition.html#search) |
<br>

### 3. Stay Updated<a id="stayupdated"></a>
Since the Zynx Health API is actively being developed, follow this page to keep up-to-date with the changes.

## Background

### What is the Zynx Health API and FHIR?
The Zynx Health API provides access to Zynx Content in the FHIR standard format.
[FHIR (Fast Healthcare Interoperability Resources)](http://hl7.org/fhir/summary.html) is a specification for exchanging healthcare data in a modern and developer-friendly way.
<br>
<br>
## Table of Contents

1. [What's New](#new)
2. [Production Release Notes](#prod)
3. [Clinical  Decision Support Content](#CDS)
   1. [Clinical Glossary](./clinical-glossary.md)
4. [Getting Started](#start)
   1. [Get your API Key](#getkey)
   2. [Make API Calls](#makecalls)
   3. [Stay Updated](#stayupdated)
5. [Functionality by Content Type \ Content Item Type](./content_item_details.md)
<br><br>

## <a id="new"></a>What's New
**Date**|**Description**
:-----:|:-----:
2024.4.29|Production Release

## <a id="prod"></a>Production Release Notes
### Content Updates – Last updated Q1, 2024<br>
•  ZynxCare<br> 
•  ZynxCare Extended<br>
•  ZynxCare for Home Health<br>
•  ZynxCare for Rehabilitation<br>
•  ZynxOrder<br>
<br>
### Zynx for Chronic Care Management Content Updates – Last updated 2024.3.26<br>
•  Content update containing 27 plans of care
<br>
### Zynx for Chronic Care Management Assessment Updates – Last updated 2024.3.26<br>
•  Content update containing 7 assessments
<br>

[Conformance Information](conformance.md)

## <a id="CDS"></a>Clinical Decision Support Content
Order set and plan of care content have Zynx evidence links, custom evidence links, performance measures and key clinical process information embedded. Users without license to ZynxEvidence will not be able to access actual evidence pages. 

### Trial
**Content**|**Type**|**Status**|**Pricing**|**Zynx Content ID**
:-----:|:-----:|:-----:|:-----:|:-----:
Asthma - Admission to ICU|Order Set|Available Now|Free for approved developers. See developer license agreement for terms.| 795
Transition of Care - General|Plan of Care|Available Now|Free for approved developers. See developer license agreement for terms.| 3811
Opioid Use Disorder|CCM|Available Now|Free for approved developers. See developer license agreement for terms.| CCM13
<br>

For a glossary of clinical terms and Zynx product offerings, [click here](./clinical-glossary.md).

### Premium
**Product**|**Type**|**Status**|**Pricing**
:-----:|:-----:|:-----:|:-----:
ZynxOrder<br/>[400+]|Order Set|Available Now|Requires paid license.
ZynxCare<br/>[300+]|Plan of Care|Available Now|Requires paid license.
ZynxCare Extended<br/> [100+]| Plan of Care |Available Now|Requires paid license.
ZynxCare for Chronic Conditions<br/> [26]| CCM |Available Now|Requires paid license. 
ZynxCare for Home Health<br/> [50+]| Plan of Care |Available Now|Requires paid license.
ZynxCare for Rehabilitation<br/> [50+]| Plan of Care |Available Now|Requires paid license. 

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
| base  | Zynx Health API [Service Base URL](http://hl7.org/fhir/http.html#general) | `https://api.zynx.com/t/zynx.com/connect/1.0.0/` |
| type  | Resource type                 | `PlanDefinition`    |
| id    | Logical identity of the resource         | Example: `a263fc5f-a8e5-4c15-8505-ad993967677c`                             |

<br>

Presently one resource type will be exposed with Zynx content via the RESTful API of the FHIR workflow module/clinical process:
 - [`PlanDefinition`](http://hl7.org/fhir/plandefinition.html): This resource allows for the definition of various types of plans as a sharable, consumable, and executable artifact. The resource is general enough to support the description of a broad range of clinical artifacts such as clinical decision support rules, order sets and protocols.

#### B. Content Examples

##### Example Requests

> Wherever `API_KEY` is referenced below, replace it with the unique key that was emailed to you.
> 
> Examples are provided for both JSON and XML.  Just update the Accept header.<br>
> <br>
> Examples can use "https://api.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition?identifier=http://www.zynxhealth.com/codings/id/zynx/contentid%7C0:<contentId>" to access a Plan Definition for a given contentId if the Zynx contentId is known and accessible.<br/>
> • Order Set content id 795 "https://api.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition?identifier=http://www.zynxhealth.com/codings/id/zynx/contentid%7C0:795"<br>
> • Plan of Care content id 3811 "https://api.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition?identifier=http://www.zynxhealth.com/codings/id/zynx/contentid%7C0:3811"<br>
> 
>Examples can use "https://api.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition?identifier=http://www.zynxhealth.com/codings/id/zynx/contentid%7C&_count=50" to access all Zynx content allowed per your given privileges per token or with Trial token.<br>
   
>
>Examples can use "https://api.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition?identifier=http://www.zynxhealth.com/codings/id/custom/contentid%7C&_count=50" to access all Custom content allowed per your given privileges per token.<br>
>
###### Order Sets
```
curl --request GET \
--header 'Authorization: Bearer API_KEY' \
--header 'Accept: application/json' \
--header 'cache-control: no-cache' \
https://api.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition/a263fc5f-a8e5-4c15-8505-ad993967677c

curl --request GET \
--header 'Authorization: Bearer API_KEY' \
--header 'Accept: application/xml' \
--header 'cache-control: no-cache' \
https://api.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition/a263fc5f-a8e5-4c15-8505-ad993967677c
```
###### Plans of Care
```
curl --request GET \
--header 'Authorization: Bearer API_KEY' \
--header 'Accept: application/json' \
--header 'cache-control: no-cache' \
https://api.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition/8ac80263-4468-48f4-af20-e47157599e7e

curl --request GET \
--header 'Authorization: Bearer API_KEY' \
--header 'Accept: application/xml' \
--header 'cache-control: no-cache' \
https://api.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition/8ac80263-4468-48f4-af20-e47157599e7e
```

###### Custom Plan of Care <br> 

##### Example Requests

```
curl --request GET \
--header 'Authorization: Bearer API_KEY' \
--header 'Accept: application/json' \
--header 'cache-control: no-cache' \
https://api.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition/<resourceId>

curl --request GET \
--header 'Authorization: Bearer API_KEY' \
--header 'Accept: application/xml' \
--header 'cache-control: no-cache' \
https://api.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition/<resourceId>
```

##### Example Response

See the full example FHIR response for the Pain Plan of Care, [click here](./response_custom_plan_of_care.md).<br>  

###### Postman GUI REST API tool
For instructions about using the Postman GUI REST API tool, [click here](./gui-api-request.md).


#### C. More Information
| Resource Type      |             Resource Content             |                XML Schema                |               JSON Schema                |              Search Params               |
| :----------------- | :--------------------------------------: | :--------------------------------------: | :--------------------------------------: | :--------------------------------------: |
| PlanDefinition     | [RC](http://hl7.org/fhir/plandefinition.html#resource) | [XML](http://hl7.org/fhir/plandefinition.xsd) | [JSON](http://hl7.org/fhir/plandefinition.schema.json.html) | [Search](http://hl7.org/fhir/plandefinition.html#search) |

###### Featured Parameters

| ([Parameter](http://hl7.org/fhir/search.html#all))     | Description     | Type    | Required   | Accepted Value  | Example   |
| :--- | :--- | :--- |:--- |:--- | :--- |
| count  | Returns the resource count specified that are available for the privileges of the token used | ([Number](http://hl7.org/fhir/search.html#number)) | No | 1-200 | \?\_count=50 | 
| identifier  | Returns content / Plan Definition for given contentId | N\A | No | Zynx contentIds |```\?identifier=http://www.zynxhealth.com/codings/id/zynx/ contentid%7C0:<AuthorSpace contentId>``` <br> Trial Order Set 795 example: ```\?identifier=http://www.zynxhealth.com/codings/id/zynx/ contentid%7C0:795``` | 
| lastUpdated  | Returns resources updated for given date or date range in results | ([Date](http://hl7.org/fhir/search.html#date)) | No | Date Format YYYY-MM-DD|  \?\_lastUpdated=2021-04 returns content updated in a given month <br> \?\_lastUpdated=2021 returns content updated in a given year <br>  \?\_lastUpdated=2021-05-01 returns content updated in a given day <br>  \?\_lastUpdated=gt2021-04 returns content updated after given date specified when ([Prefix](http://hl7.org/fhir/search.html#prefix)) gt is used|  
| title | Returns a content / Plan Definition resource with specified title | ([String](http://hl7.org/fhir/search.html#string)) | No | Characters |\?title=Asthma - Admission to ICU | 
| status | The current status of the plan definition | ([Token](http://hl7.org/fhir/search.html#token)) | No | active, or retired| \?status=active or \?status=retired |    

###### Zynx's Value Set for Content Item Types
[Click here](./content_item_details.md) for detailed funtionality within given content item types.
   
| FHIR Display Value \ [Description]   | Code Value    |   Explanation |
| :---------------- | :-----------: | :---------- |
| Section       | 2             | A category used to organize order items ([view full explanation](https://github.com/zynxhealth/documentation/blob/master/clinical-glossary.md#section))|
| Orderable (Med)  | 3          | Drug names that can be expressed as medication names or dispensable products ([view full explanation](https://github.com/zynxhealth/documentation/blob/master/clinical-glossary.md#medication))|
| Reminder \ [Patient Engagement] | 4          | An evidence-based note to the clinician at the point of care ([view full explanation](https://github.com/zynxhealth/documentation/blob/master/clinical-glossary.md#reminder))|
|Orderable | 5| Non-medication items that can be ordered by a clinician (e.g. nursing orders, laboratory tests, radiology, etc) ([view full explanation](https://github.com/zynxhealth/documentation/blob/master/clinical-glossary.md#orderable))|
|Problem|8| A condition experienced by a patient that can be treated in a clinical care setting ([view full explanation](https://github.com/zynxhealth/documentation/blob/master/clinical-glossary.md#problem))|
|Outcome \ [Goal]|10| Measurable patient-centered conditions/states, behaviors, or perceptions in response to interdisciplinary interventions ([view full explanation](https://github.com/zynxhealth/documentation/blob/master/clinical-glossary.md#outcome))|
|Activity|12|A specific action that the interdisciplinary care team carries out to address a patient problem ([view full explanation](https://github.com/zynxhealth/documentation/blob/master/clinical-glossary.md#activity))|
|Activitylet \ [Activity Detail]|15|Further description or clarification of key concepts for an activity in a plan of care.
|Frequency \ [Activity Frequency]|16|Frequency for an activity in a plan of care.

### <a id="stayupdated"></a>4. Stay Updated
Since the Zynx Health API is actively being developed, follow this page to keep up-to-date with the changes.

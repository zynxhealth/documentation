## Background

### What is the Zynx Health API and FHIR?
The Zynx Health API provides access to Zynx Content in the FHIR standard format.
[FHIR (Fast Healthcare Interoperability Resources)](http://hl7.org/fhir/summary.html) is a specification for exchanging healthcare data in a modern and developer-friendly way.
<br>
<br>
## What's New

| Date       | Description     |
| :--------- | :-------------- |
| 06.14.2017 | Initial release |
<br>

## Getting Started

### 1. Get your API key
Each organization will need their own API key. If you haven't done so already, apply for a key by contacting support@zynx.com.
> Wherever `API_KEY` is referenced below, replace it with the unique key that was emailed to you.
<br>

### 2. Make API Calls

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

Presently two resource types will be exposed with CaaS content via the RESTful API of the FHIR workflow module/clinical process:
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
For more information about how to search with the RESTful API, [click here](hl7.org/fhir/search.html).

##### Example Search Requests

> Wherever `API_KEY` is referenced below, replace it with the unique key that was emailed to you.

###### Search for PlanDefinition with cURL
```
curl --request GET \
  --url 'https://api.cb.zynx.com/dev-v0/fhir-a/baseDstu3/PlanDefinition?_lastUpdated=gt2017-03-01&_lastUpdated=lt2017-04-05&_format=json&_pretty=true&_summary=text' \
  --header 'cache-control: no-cache' \
  --header 'x-api-key: API_KEY'
```

###### Search for PlanDefinition with Postman GUI REST API tool
These instructions are for the [Postman App](https://www.getpostman.com), but you can use your own tool.
Click here [Install Postman](./gui-api-request.md)

<br>

#### C. More Information
| Resource Type      |             Resource Content             |                XML Schema                |               JSON Schema                |              Search Params               |
| :----------------- | :--------------------------------------: | :--------------------------------------: | :--------------------------------------: | :--------------------------------------: |
| ActivityDefinition | [RC](http://hl7.org/fhir/activitydefinition.html#resource) | [XML](http://hl7.org/fhir/activitydefinition.xsd) | [JSON](http://hl7.org/fhir/ActivityDefinition.schema.json) | [Search](http://hl7.org/fhir/activitydefinition.html#search) |
| PlanDefinition     | [RC](http://hl7.org/fhir/plandefinition.html#resource) | [XML](http://hl7.org/fhir/plandefinition.xsd) | [JSON](http://hl7.org/fhir/PlanDefinition.schema.json) | [Search](http://hl7.org/fhir/plandefinition.html#search) |
<br>

### 3. Stay Updated
Since the Zynx Health API is actively being developed, follow this page to keep up-to-date with the changes.

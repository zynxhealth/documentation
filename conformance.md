## FHIR Conformance:

### Supported:

**Category** | **Name** | **Description** | **Supported** | 
:-----:|:-----:|:-----:|:-----:
Capability | Capability Statement | The CapabilityStatement is used as a statement of the features of actual software, or of a set of rules for an application to provide. This statement connects to all the detailed statements of functionality, such as StructureDefinitions and ValueSets. | In progress |
RESTful API | Service Base URL | The protocols http: and https: SHALL NOT be used to refer to different underlying objects | Yes
RESTful API | Content Types and encodings 1 | The formal MIME-type for FHIR resources is application/fhir+xml or application/fhir+json. The correct mime type SHALL be used by clients and servers: **XML: application/fhir+xml** **JSON: application/fhir+json** **RDF: text/turtle (only the Turtle format is supported)** | XML: Completed JSON: Completed |
RESTful API | Content Types and encodings 2 |Servers SHALL support server-driven content negotiation as described in section 12 of the HTTP specification. | Yes |
RESTful API | Content Types and encodings 3 | FHIR uses UTF-8 for all request and response bodies. Since the HTTP specification (section 3.7.1) defines a default character encoding of ISO-8859-1, requests and responses SHALL explicitly set the character encoding to UTF-8 using the charset parameter of the MIME-type in the Content-Type header. | Yes |
RESTful API | HTTP Verb “read” | The returned resource SHALL have an id element with a value that is the [id]. | Yes |
RESTful API | Paging | f servers provide paging for the results of a search or history interaction, they SHALL conform to this method (adapted from RFC 5005 (Feed Paging and Archiving) for sending continuation links to the client when returning a Bundle (e.g. with history and search). If the server does not do this then there is no way to continue paging. | Yes |
Search | Parameters for all resources | Note that although the _ id parameter has a type of token, because servers SHALL use exact match with it, there is no system for the _ id parameter. | Yes |
Search | Search Parameter Types | Each search parameter is defined by a type that specifies how the search parameter behaves. These are the defined parameter types: a number search parameter SHALL be a number (a whole number, or a decimal). | Yes |
Search | Modifiers | Server SHALL reject any search request that contains a modifier that the server does not support for that parameter. | Yes |
Search | date | Technically, this is any of the date, dateTime, and instant data types; e.g. Any degree of precision can be provided, but it SHALL be populated from the left (e.g. can't specify a month without a year), except that the minutes SHALL be present if an hour is present, and you SHOULD provide a time zone if the time part is present. Note: Time can consist of hours and minutes with no seconds, unlike the XML Schema dateTime type. Some user agents may escape the : characters in the URL, and servers SHALL handle this correctly. | Yes |
Search | Page Count 1 | The parameter _ count is defined as a hint to the server regarding how many resources should be returned in a single page. Servers SHALL NOT return more resources than requested, even if they don't support paging, but are allowed to return less than the client requested. | Yes |
Search | Page Count 2 | if _ count has the value 0, this shall be treated the same as _ summary=count: the server resturns a bundle that reports the total number of resources that match in Bundle.total, but with no entries, and no prev/next/last links. | Yes
Search | Server Conformance | In order to allow the client to be confident about what search parameters were used as criteria by the server, the server SHALL return the parameters that were actually used to process the search. Applications processing search results SHALL check these returned values where necessary. For example, if the server did not support some of the filters specified in the search, a client might manually apply those filters to the retrieved result set, display a warning message to the user or take some other action. | Yes
<br>

### Future Supported:

**Category** | **Name** | **Description** | **Supported** | 
:-----:|:-----:|:-----:|:-----:
RESTful API | HTTP Verb “vread” | The returned resource SHALL have an id element with a value that is the [id]. | Future |
RESTful API | history | The return content is a Bundle with type set to history containing the specified version history, sorted with oldest versions last, and including deleted resources. Each entry SHALL minimally contain either a resource which holds the resource as it is at the conclusion of the interaction, or a request with entry.request.method The request provides information about the interaction that occurred to cause the new version, and allows, for instance, a subscriber system to differentiate between create and update interactions. The principal reason a resource might be missing is that the resource was changed by some other channel rather than via the RESTful interface. If the entry.request.method is a PUT or a POST, the entry SHALL contain a resource. | Future |
RESTful API | history | The updates list can be long, so servers may use paging. If they do, they SHALL use the method described below for breaking the list into pages if appropriate, and maintain the specified _ count across pages. | Future |
Search | Advanced Search | More advanced search operations are specified by the _ query parameter.  The _ query parameter names a custom search profile that describes a specific query operation. There can only ever be one _ query parameter in a set of search parameters. Servers processing search requests SHALL refuse to process a search request if they do not recognize the _ query parameter value. | |

## FHIR Search Parameter by Zynx content ID examples:

Search parameter name: | Description | Example
 --- | --- | ---
GET Resource by Zynx content **id** | returns all resources | 795 is the Zynx Content ID for our "Asthma - Admission to ICU"
<br>

| Example |
| --- |
| `https://api.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition?identifier=http://www.zynxhealth.com/codings/as/id%7C795` |
<br>

| Response |
| --- |
|<img src="img/postman-search-id.png">|
<br>

Search parameter name: | Description | Example
 --- | --- | ---
GET **Resource** | returns just the resource itself not a bundle | c1d06f95-c9f4-436d-ae8b-4de9c141867b is the resource id for "Asthma - Admission to ICU"
<br>

| Example |
| --- |
| `https://api.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition/c1d06f95-c9f4-436d-ae8b-4de9c141867b` |
<br>

| Response |
| --- |
|<img src="img/postman-search-resourceId.png">|
<br>

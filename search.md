## FHIR Search Parameter examples:

Search parameter name: | Description 
 --- | --- 
GET **Resource** | returns just the resource itself not a bundle
<br>

| Example |
| --- |
| `https://api-gw-beta2.cb.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition/c1d06f95-c9f4-436d-ae8b-4de9c141867b` |
<br>

Search parameter name: | Description 
 --- | --- 
GET Resource by **focus** | focus parameter returns all resources with this topic id
<br>

| Example |
| --- |
| `https://api-gw-beta2.cb.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition?focus=e363c402-ad6e-4534-b2ff-b0d82ecee6a0` |
<br>

[List of Focus Ids found here.](./focus_id.md)

Search parameter name: | Description 
 --- | --- 
GET Resource by **venue** | venue parameter returns all resources with this venue id
<br>

| Example |
| --- |
| `https://api-gw-beta2.cb.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition?venue=10e9de09-dbd0-47d8-a9cd-19ac5e39eca5` |
<br>

[List of Venue Ids found here.](./venue_id.md)

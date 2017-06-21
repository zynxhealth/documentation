###### Search for PlanDefinition with Postman GUI REST API tool
These instructions are for the [Postman App](https://www.getpostman.com), but you can use your own tool.

1. Launch Postman
2. Under "New Tab" select the verb GET
3. Enter this endpoint: `https://api.cb.zynx.com/dev-v0/fhir-a/baseDstu3/PlanDefinition`
4. Click "Params" and add the following key and value parameters (`key:value`):

   | Key            | Value Parameters |
   | :------------- | :--------------- |
   | `_lastUpdated` | `gt2017-03-01`   |
   | `_lastUpdated` | `lt2017-04-05`   |
   | `_format`      | `json`           |
   | `_pretty`      | `true`           |
   | `_summary`     | `text`           |
   
5. Click "Headers" and add the following key and value (`key:value`):

   | Key         | Value     | Description |
   | :---------- | :-------- | :---------- |
   | `x-api-key` | `API_KEY` | Key provided by Zynx Health for authentication |
   | `accept-encoding` | `gzip;q=0,deflate,sdch` | Disables gzip so Postman will work |
   
6. Click "Send"

![Postman](./img/postman.png)

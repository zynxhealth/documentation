## Retrieve Order Set with Postman
These instructions are for the [Postman](https://www.getpostman.com) application, but you can use your own tool.

> Wherever `API_KEY` is referenced below, replace it with the unique key that was emailed to you.

1. Install [Postman](https://www.getpostman.com)
2. Launch Postman
3. Under "New Tab" select the verb GET
4. Enter this endpoint:
```
https://api.zynx.com/t/zynx.com/connect/1.0.0/PlanDefinition/c6afff10-6cbf-4a19-b012-5344bfbf8080
```
5. Click "Headers" and add the following key and value (`key:value`):

   | Key         | Value     | Description |
   | :---------- | :--------  | :---------- |
   | `Authorization` | `Bearer API_KEY`  | Key provided by Zynx Health for authentication| 
   | `Accept` | `application/json`  | The expected response type.  Change to `application/xml` for XML| 
   
   
6. Click "Send"

<br>


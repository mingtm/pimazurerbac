# List roleDefinitions

Retrieve a list of roledefinition objects.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /providers/<id>/resources('<id>')/roleDefinitions
```
### Optional query parameters
This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.

### Request headers
| Name      |Description|
|:----------|:----------|
| Authorization  | Bearer {code}|
| Workbook-Session-Id  | Workbook session Id that determines if changes are persisted or not. Optional.|

### Request body
Do not supply a request body for this method.
### Response
If successful, this method returns a `200 OK` response code and collection of [roleDefinition](../resources/roledefinition.md) objects in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_roledefinitions"
}-->
```http
GET https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/resources('8575d82b-c7b6-4c69-8eee-1d452985a64e')/roleDefinitions 
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.roleDefinition",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 227

{
  "@odata.context": "https://api.azurerbac.mspim.azure.com/api/v1/$metadata#resources('8575d82b-c7b6-4c69-8eee-1d452985a64e')/roleDefinitions",
  "value": [
    {
      "id": "8575d82b-c7b6-4c69-8eee-1d452985a64e_21d96096-b162-414a-8302-d8354f9d91b2",
      "templateId": "21d96096-b162-414a-8302-d8354f9d91b2",
      "displayName": "Azure Service Deploy Release Management Contributor",
      "subjectCount": 0,
      "activationRequiredCount": 0,
      "assignedCount": 0,
      "ruleSettings": [ ]
    },
    {
      "id": "8575d82b-c7b6-4c69-8eee-1d452985a64e_9f15f5f5-77bd-413a-aa88-4b9c68b1e7bc",
      "templateId": "9f15f5f5-77bd-413a-aa88-4b9c68b1e7bc",
      "displayName": "GenevaWarmPathResourceContributor",
      "subjectCount": 0,
      "activationRequiredCount": 0,
      "assignedCount": 0,
      "ruleSettings": [ ]
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List roleDefinitions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
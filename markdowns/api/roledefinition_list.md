# List roleDefinitions

Retrieve a list of roledefinition objects.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /providers/<id>/roleDefinitions
GET /providers/<id>/resource('<id>')/roleDefinitions
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
Here is an example of the request to get all role definitions for a particular resource.
<!-- {
  "blockType": "request",
  "name": "get_roledefinitions"
}-->
```http
GET https://graph.microsoft.com/beta//api/v1/providers('00000000-0000-0000-0000-000000000002')/resources('bc6f10e6-6dd9-4393-853e-09e13c036b17')/roleDefinitions
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
    "@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#resources('bc6f10e6-6dd9-4393-853e-09e13c036b17')/roleDefinitions",
    "value": [
        {
            "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17_21d96096-b162-414a-8302-d8354f9d91b2",
            "templateId": "21d96096-b162-414a-8302-d8354f9d91b2",
            "displayName": "Azure Service Deploy Release Management Contributor",
            "subjectCount": 0,
            "activationRequiredCount": 0,
            "assignedCount": 0,
            "ruleSettings": [            ]
        },
        {F
            "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17_9f15f5f5-77bd-413a-aa88-4b9c68b1e7bc",
            "templateId": "9f15f5f5-77bd-413a-aa88-4b9c68b1e7bc",
            "displayName": "GenevaWarmPathResourceContributor",
            "subjectCount": 0,
            "activationRequiredCount": 0,
            "assignedCount": 0,
            "ruleSettings": [            ]
        },
        {
            "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17_a042fe8d-14b3-4850-9120-e2f357577b2d",
            "templateId": "a042fe8d-14b3-4850-9120-e2f357577b2d",
            "displayName": "Monitor permissions",
            "subjectCount": 0,
            "activationRequiredCount": 0,
            "assignedCount": 0,
            "ruleSettings": [            ]
        },
        {
            "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17_7fd64851-3279-459b-b614-e2b2ba760f5b",
            "templateId": "7fd64851-3279-459b-b614-e2b2ba760f5b",
            "displayName": "Office DevOps",
            "subjectCount": 0,
            "activationRequiredCount": 0,
            "assignedCount": 0,
            "ruleSettings": [            ]
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
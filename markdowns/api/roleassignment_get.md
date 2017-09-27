# Get roleAssignment

Retrieve the properties and relationships of roleassignment object.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /providers/<id>/roleAssignments('<id>')
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
If successful, this method returns a `200 OK` response code and [roleAssignment](../resources/roleassignment.md) object in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_roleassignment"
}-->
```http
GET https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/roleAssignments('8575d82b-c7b6-4c69-8eee-1d452985a64e_312a565d-c81f-4fd8-895a-4e21e48d571c_795ed4a8-e4e5-48f5-b60c-ee9845a7a790_9102e255-0f98-45d1-967d-00ddd0fd0200')?$expand=linkedAssignment,subject,roleDefinition($expand=resource)
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.roleAssignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 182

{
  "id": "8575d82b-c7b6-4c69-8eee-1d452985a64e_312a565d-c81f-4fd8-895a-4e21e48d571c_795ed4a8-e4e5-48f5-b60c-ee9845a7a790_9102e255-0f98-45d1-967d-00ddd0fd0200",
  "originId": "/subscriptions/f90f7b96-b06f-4ee4-bc38-a001deb2375f/providers/Microsoft.Authorization/roleAssignments/9102e255-0f98-45d1-967d-00ddd0fd0200",
  "isPermanent": true,
  "expirationDateTime": null,
  "startDateTime": null,
  "level": "Member",
  "assignmentType": "Direct",
  "linkedAssignment": null,
  "subject": {
    "id": "795ed4a8-e4e5-48f5-b60c-ee9845a7a790",
    "displayName": "af",
    "type": "User",
    "principalName": "af@foo.com",
    "email": "af@foo.com"
  },
  "roleDefinition": {
    "id": "8575d82b-c7b6-4c69-8eee-1d452985a64e_312a565d-c81f-4fd8-895a-4e21e48d571c",
    "templateId": "312a565d-c81f-4fd8-895a-4e21e48d571c",
    "displayName": "API Management Service Contributor",
    "subjectCount": 0,
    "activationRequiredCount": 0,
    "assignedCount": 0,
    "ruleSettings": [    ],
    "resource": {
      "id": "8575d82b-c7b6-4c69-8eee-1d452985a64e",
      "originalId": "/subscriptions/f90f7b96-b06f-4ee4-bc38-a001deb2375f",
      "displayName": "Deep Dive",
      "resourceType": "subscription",
      "roleDefinitionCount": 0,
      "roleAssignmentCount": 0
    }
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get roleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
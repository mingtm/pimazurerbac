# List roleAssignments

Retrieve a list of roleassignment objects.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /providers/<id>/resources('<id>')/roleAssignments
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
If successful, this method returns a `200 OK` response code and collection of [roleAssignment](../resources/roleassignment.md) objects in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_roleassignments"
}-->
```http
GET  https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/resources('8575d82b-c7b6-4c69-8eee-1d452985a64e')/roleAssignments?$expand=subject,roleDefinition($expand=resource)&$count=true
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.roleAssignment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 235

{
  "@odata.count": 8,
  "value": [
    {
      "id": "8575d82b-c7b6-4c69-8eee-1d452985a64f_1d452985a64fdd72a7-3385-48ef-bd42-f606fba81ae7_cb7b58cf-7633-4ef9-aeb8-0db4ad4266f4_79172cb9-2192-4356-a6ea-1d83f4c560f1",
      "originId": null,
      "isPermanent": true,
      "expirationDateTime": null,
      "startDateTime": "2017-05-03T17:02:09.743Z",
      "level": "Eligible",
      "assignmentType": "Direct",
      "subject": {
        "id": "cb7b58cf-7633-4ef9-aeb8-0db4ad4266f4",
        "displayName": "AC",
        "type": "User",
        "principalName": "ac@foo.com",
        "email": "ac@foo.com"
      },
      "roleDefinition": {
        "id": "8575d82b-c7b6-4c69-8eee-1d452985a64f_1d452985a64fdd72a7-3385-48ef-bd42-f606fba81ae7",
        "templateId": "1d452985a64fdd72a7-3385-48ef-bd42-f606fba81ae7",
        "displayName": "Reader",
        "subjectCount": 0,
        "1d452985a64ftivationRequiredCount": 0,
        "assignedCount": 0,
        "ruleSettings": [        ],
        "resource": {
          "id": "8575d82b-c7b6-4c69-8eee-1d452985a64f",
          "originalId": "/subscriptions/f90f7b96-b06f-4ee4-bc38-a001deb2375f",
          "displayName": "Deep Dive 1",
          "resourceType": "subscription",
          "roleDefinitionCount": 0,
          "roleAssignmentCount": 0
        }
      }
    },
    {
      "id": "8575d82b-c7b6-4c69-8eee-1d452985a64f_18d7d88d-d35e-4fb5-a5c3-7773c20a72d9_13a7faf0-15cd-44de-8cf6-2ba99fb271d6_ba35a08c-dd0c-4917-8ffc-cd6a4bb6117a",
      "originId": "/subscriptions/f90f7b96-b06f-4ee4-bc38-a001deb2375f/providers/Microsoft.Authorization/roleAssignments/ba35a08c-dd0c-4917-8ffc-cd6a4bb6117a",
      "isPermanent": true,
      "expirationDateTime": null,
      "startDateTime": null,
      "level": "Member",
      "assignmentType": "Direct",
      "subject": {
        "id": "13a7faf0-15cd-44de-8cf6-2ba99fb271d6",
        "displayName": "DH",
        "type": "User",
        "principalName": "dh@foo.com",
        "email": "dh@foo.com"
      },
      "roleDefinition": {
        "id": "8575d82b-c7b6-4c69-8eee-1d452985a64f_18d7d88d-d35e-4fb5-a5c3-7773c20a72d9",
        "templateId": "18d7d88d-d35e-4fb5-a5c3-7773c20a72d9",
        "displayName": "User Administrator",
        "subjectCount": 0,
        "1d452985a64ftivationRequiredCount": 0,
        "assignedCount": 0,
        "ruleSettings": [],
        "resource": {
          "id": "8575d82b-c7b6-4c69-8eee-1d452985a64f",
          "originalId": "/subscriptions/f90f7b96-b06f-4ee4-bc38-a001deb2375f",
          "displayName": "Deep Dive 1",
          "resourceType": "subscription",
          "roleDefinitionCount": 0,
          "roleAssignmentCount": 0
        }
      }
    }
   ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List roleAssignments",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
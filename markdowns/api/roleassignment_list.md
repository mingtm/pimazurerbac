# List roleAssignments

Retrieve a list of roleassignment objects.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /providers/<id>/roleAssignments
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
Here is an example of the request, which queries all role assignments for a given resource and a target user subject.
<!-- {
  "blockType": "request",
  "name": "get_roleassignments"
}-->
```http
GET https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/roleAssignments?$expand=linkedAssignment,subject,roleDefinition($expand=resource)&$filter=(roleDefinition/resource/id%20eq%20%27bc6f10e6-6dd9-4393-853e-09e13c036b17%27)+and+(subject/id%20eq%20%27795ed4a8-e4e5-48f5-b60c-ee9845a7a791%27) 
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
Content-length: 2335

{
    "@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#roleAssignments",
    "value": [
        {
            "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17_d3881f73-407a-4167-8283-e981cbba0404_795ed4a8-e4e5-48f5-b60c-ee9845a7a790_f4269ff2-542b-4b3a-b021-294a51760006",
            "originId": "/subscriptions/b3797212-a671-4ab5-b866-d71fd4159331/providers/contoso.Authorization/roleAssignments/f4269ff2-542b-4b3a-b021-294a51760006",
            "isPermanent": true,
            "expirationDateTime": null,
            "startDateTime": null,
            "level": "Member",
            "assignmentType": "Direct",
            "linkedAssignment": null,
            "subject@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#roleAssignments('bc6f10e6-6dd9-4393-853e-09e13c036b17_d3881f73-407a-4167-8283-e981cbba0404_795ed4a8-e4e5-48f5-b60c-ee9845a7a790_f4269ff2-542b-4b3a-b021-294a51760006')/subject/$entity",
            "subject": {
                "id": "795ed4a8-e4e5-48f5-b60c-ee9845a7a790",
                "displayName": "alpha",
                "type": "User",
                "principalName": "alpha@ntdev.contoso.com",
                "email": "alpha@contoso.com"
            },
            "roleDefinition@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#roleAssignments('bc6f10e6-6dd9-4393-853e-09e13c036b17_d3881f73-407a-4167-8283-e981cbba0404_795ed4a8-e4e5-48f5-b60c-ee9845a7a790_f4269ff2-542b-4b3a-b021-294a51760006')/roleDefinition/$entity",
            "roleDefinition": {
                "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17_d3881f73-407a-4167-8283-e981cbba0404",
                "templateId": "d3881f73-407a-4167-8283-e981cbba0404",
                "displayName": "Automation Operator",
                "subjectCount": 0,
                "activationRequiredCount": 0,
                "assignedCount": 0,
                "ruleSettings": [],
                "resource@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#roleAssignments('bc6f10e6-6dd9-4393-853e-09e13c036b17_d3881f73-407a-4167-8283-e981cbba0404_795ed4a8-e4e5-48f5-b60c-ee9845a7a790_f4269ff2-542b-4b3a-b021-294a51760006')/roleDefinition/resource/$entity",
                "resource": {
                    "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17",
                    "originalId": "/subscriptions/b3797212-a671-4ab5-b866-d71fd4159331",
                    "displayName": "alpha",
                    "resourceType": "subscription",
                    "status": "Active",
                    "roleDefinitionCount": 0,
                    "roleAssignmentCount": 0
                }
            }
        },
        {
            "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17_8e3af657-a8ff-443c-a75c-2fe8c4bcb635_795ed4a8-e4e5-48f5-b60c-ee9845a7a790_00000000-0000-0000-0000-000000000000",
            "originId": "/subscriptions/b3797212-a671-4ab5-b866-d71fd4159331/providers/contoso.Authorization/classicAdministrators/10030000801B6D49",
            "isPermanent": true,
            "expirationDateTime": null,
            "startDateTime": null,
            "level": "Member",
            "assignmentType": "Group",
            "linkedAssignment": null,
            "subject@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#roleAssignments('bc6f10e6-6dd9-4393-853e-09e13c036b17_8e3af657-a8ff-443c-a75c-2fe8c4bcb635_795ed4a8-e4e5-48f5-b60c-ee9845a7a790_00000000-0000-0000-0000-000000000000')/subject/$entity",
            "subject": {
                "id": "795ed4a8-e4e5-48f5-b60c-ee9845a7a790",
                "displayName": "alpha",
                "type": "User",
                "principalName": "alpha@ntdev.contoso.com",
                "email": "alpha@contoso.com"
            },
            "roleDefinition@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#roleAssignments('bc6f10e6-6dd9-4393-853e-09e13c036b17_8e3af657-a8ff-443c-a75c-2fe8c4bcb635_795ed4a8-e4e5-48f5-b60c-ee9845a7a790_00000000-0000-0000-0000-000000000000')/roleDefinition/$entity",
            "roleDefinition": {
                "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17_8e3af657-a8ff-443c-a75c-2fe8c4bcb635",
                "templateId": "8e3af657-a8ff-443c-a75c-2fe8c4bcb635",
                "displayName": "Owner",
                "subjectCount": 0,
                "activationRequiredCount": 0,
                "assignedCount": 0,
                "ruleSettings": [],
                "resource@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#roleAssignments('bc6f10e6-6dd9-4393-853e-09e13c036b17_8e3af657-a8ff-443c-a75c-2fe8c4bcb635_795ed4a8-e4e5-48f5-b60c-ee9845a7a790_00000000-0000-0000-0000-000000000000')/roleDefinition/resource/$entity",
                "resource": {
                    "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17",
                    "originalId": "/subscriptions/b3797212-a671-4ab5-b866-d71fd4159331",
                    "displayName": "alpha",
                    "resourceType": "subscription",
                    "status": "Active",
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
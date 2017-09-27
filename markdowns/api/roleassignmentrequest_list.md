# List roleAssignmentRequests

Retrieve a list of roleassignmentrequest objects.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /providers/<id>/roleAssignmentRequests
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
If successful, this method returns a `200 OK` response code and collection of [roleAssignmentRequest](../resources/roleassignmentrequest.md) objects in the response body.
### Example
##### Request
Here is an example of the request to query all the pending role assignment requests for a particular resource.
<!-- {
  "blockType": "request",
  "name": "get_roleassignmentrequests"
}-->
```http
GET https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/roleAssignmentRequests?$expand=subject,roleDefinition($expand=resource)&$filter=(status+eq+%27Accepted%27+or+status+eq+%27PendingEvaluation%27+or+status+eq+%27Granted%27+or+status+eq+%27PendingProvisioning%27)+and+(roleDefinition/resource/id+eq+%27bc6f10e6-6dd9-4393-853e-09e13c036b17%27)
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.roleAssignmentRequest",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 279

{
    "@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#roleAssignmentRequests",
    "value": [
        {
            "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17_7fd64851-3279-459b-b614-e2b2ba760f5b_7c53453e-d5a4-41e0-8eb1-32d5ec8bfdee",
            "assignmentLevel": "Eligible",
            "requestType": "AdminAdd",
            "requestedDateTime": "2017-09-27T23:01:44.127Z",
            "roleAssignmentStartDateTime": "2017-10-05T23:01:15.99Z",
            "status": "Granted",
            "reason": null,
            "statusDetail": [
                {
                    "key": "AdminRequestRule",
                    "value": "Grant"
                },
                {
                    "key": "ExpirationRule",
                    "value": "Grant"
                },
                {
                    "key": "MfaRule",
                    "value": "Grant"
                }
            ],
            "schedule": {
                "duration": "PT0S",
                "type": "Once",
                "details": null,
                "startDateTime": "2017-10-05T23:01:15.99Z",
                "isPermanent": false,
                "stopDateTime": "2017-12-26T23:01:15.99Z"
            },
            "targetLinkedRoleAssignmentId": null,
            "evaluateOnly": false,
            "subject@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#roleAssignmentRequests('bc6f10e6-6dd9-4393-853e-09e13c036b17_7fd64851-3279-459b-b614-e2b2ba760f5b_7c53453e-d5a4-41e0-8eb1-32d5ec8bfdee')/subject/$entity",
            "subject": {
                "id": "795ed4a8-e4e5-48f5-b60c-ee9845a7a793",
                "displayName": "alpha",
                "type": "User",
                "principalName": "alpha@microsoft.com",
                "email": "alpha@microsoft.com"
            },
            "roleDefinition@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#roleAssignmentRequests('bc6f10e6-6dd9-4393-853e-09e13c036b17_7fd64851-3279-459b-b614-e2b2ba760f5b_7c53453e-d5a4-41e0-8eb1-32d5ec8bfdee')/roleDefinition/$entity",
            "roleDefinition": {
                "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17_7fd64851-3279-459b-b614-e2b2ba760f5b",
                "templateId": "7fd64851-3279-459b-b614-e2b2ba760f5b",
                "displayName": "Office DevOps",
                "subjectCount": 0,
                "activationRequiredCount": 0,
                "assignedCount": 0,
                "ruleSettings": [],
                "resource@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#roleAssignmentRequests('bc6f10e6-6dd9-4393-853e-09e13c036b17_7fd64851-3279-459b-b614-e2b2ba760f5b_7c53453e-d5a4-41e0-8eb1-32d5ec8bfdee')/roleDefinition/resource/$entity",
                "resource": {
                    "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17",
                    "originalId": "/subscriptions/b3797212-a671-4ab5-b866-d71fd4159334",
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
  "description": "List roleAssignmentRequests",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
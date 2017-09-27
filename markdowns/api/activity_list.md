# List activities

Retrieve a list of activity objects.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /providers/<id>/activities
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
If successful, this method returns a `200 OK` response code and collection of [activity](../resources/activity.md) objects in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_activities"
}-->
```http
GET https://graph.microsoft.com/beta//providers('00000000-0000-0000-0000-000000000002')/activities?$filter=createdDateTime+ge+2017-09-26T23:31:48.173Z+and+createdDateTime+le+2017-09-27T23:31:48.173Z+and+originalRequestor+ne+null+and+resource/id+eq+%27bc6f10e6-6dd9-4393-853e-09e13c036b17%27&$orderby=createdDateTime+desc&$expand=requestor,originalRequestor,subject,target,resource
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.activity",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 2276

{
    "@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#activities",
    "value": [
        {
            "id": "47f9ccb8-1e60-4884-881d-30bd147c4028",
            "correlationId": "05c59fcd-0707-412c-9938-e8d6727e5dea",
            "createdDateTime": "2017-09-27T23:28:48.4064178Z",
            "expirationDateTime": "9999-12-31T23:59:59.9999999Z",
            "operationType": "CancelRequestEligibleRole",
            "reason": null,
            "status": "Succeeded",
            "requestor@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#activities('47f9ccb8-1e60-4884-881d-30bd147c4028')/requestor/$entity",
            "requestor": {
                "id": "795ed4a8-e4e5-48f5-b60c-ee9845a7a790",
                "displayName": "alpha",
                "type": "User",
                "principalName": "alpha@contoso.com",
                "email": null
            },
            "originalRequestor@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#activities('47f9ccb8-1e60-4884-881d-30bd147c4028')/originalRequestor/$entity",
            "originalRequestor": {
                "id": "795ed4a8-e4e5-48f5-b60c-ee9845a7a790",
                "displayName": "alpha",
                "type": "User",
                "principalName": "alpha@contoso.com",
                "email": null
            },
            "subject@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#activities('47f9ccb8-1e60-4884-881d-30bd147c4028')/subject/$entity",
            "subject": {
                "id": "795ed4a8-e4e5-48f5-b60c-ee9845a7a790",
                "displayName": "alpha",
                "type": "User",
                "principalName": "alpha@contoso.com",
                "email": "alpha@contoso.com"
            },
            "target@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#activities('47f9ccb8-1e60-4884-881d-30bd147c4028')/target/$entity",
            "target": {
                "id": "7fd64851-3279-459b-b614-e2b2ba760f5b",
                "displayName": "Office DevOps",
                "uniqueName": null,
                "objectType": "RoleDefinition",
                "internalType": null
            },
            "resource@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#activities('47f9ccb8-1e60-4884-881d-30bd147c4028')/resource/$entity",
            "resource": {
                "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17",
                "originalId": "/subscriptions/b3797212-a671-4ab5-b866-d71fd4159335",
                "displayName": "alpha",
                "resourceType": "subscription",
                "status": "Active",
                "roleDefinitionCount": 0,
                "roleAssignmentCount": 0
            }
        },
        {
            "id": "31c0fa61-2d62-43bb-9ebd-cb3a7f670d16",
            "correlationId": "dbe4c2d9-cd79-41ef-abad-16eb85c68c4e",
            "createdDateTime": "2017-09-27T23:01:44.3254796Z",
            "expirationDateTime": "9999-12-31T23:59:59.9999999Z",
            "operationType": "CreateRequestEligibleRole",
            "reason": null,
            "status": "Succeeded",
            "requestor@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#activities('31c0fa61-2d62-43bb-9ebd-cb3a7f670d16')/requestor/$entity",
            "requestor": {
                "id": "795ed4a8-e4e5-48f5-b60c-ee9845a7a790",
                "displayName": "alpha",
                "type": "User",
                "principalName": "alpha@contoso.com",
                "email": null
            },
            "originalRequestor@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#activities('31c0fa61-2d62-43bb-9ebd-cb3a7f670d16')/originalRequestor/$entity",
            "originalRequestor": {
                "id": "795ed4a8-e4e5-48f5-b60c-ee9845a7a790",
                "displayName": "alpha",
                "type": "User",
                "principalName": "alpha@contoso.com",
                "email": null
            },
            "subject@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#activities('31c0fa61-2d62-43bb-9ebd-cb3a7f670d16')/subject/$entity",
            "subject": {
                "id": "795ed4a8-e4e5-48f5-b60c-ee9845a7a790",
                "displayName": "alpha",
                "type": "User",
                "principalName": "alpha@contoso.com",
                "email": "alpha@contoso.com"
            },
            "target@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#activities('31c0fa61-2d62-43bb-9ebd-cb3a7f670d16')/target/$entity",
            "target": {
                "id": "7fd64851-3279-459b-b614-e2b2ba760f5b",
                "displayName": "Office DevOps",
                "uniqueName": null,
                "objectType": "RoleDefinition",
                "internalType": null
            },
            "resource@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#activities('31c0fa61-2d62-43bb-9ebd-cb3a7f670d16')/resource/$entity",
            "resource": {
                "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17",
                "originalId": "/subscriptions/b3797212-a671-4ab5-b866-d71fd4159335",
                "displayName": "alpha",
                "resourceType": "subscription",
                "status": "Active",
                "roleDefinitionCount": 0,
                "roleAssignmentCount": 0
            }
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List activities",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
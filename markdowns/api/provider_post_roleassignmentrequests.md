# Create roleAssignmentRequest

Use this API to create a new roleAssignmentRequest.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /providers/<id>/roleAssignmentRequests

```
### Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {code}|
| Workbook-Session-Id  | Workbook session Id that determines if changes are persisted or not. Optional.|

### Request body
In the request body, supply a JSON representation of [roleAssignmentRequest](../resources/roleassignmentrequest.md) object.


### Response
If successful, this method returns `201, Created` response code and [roleAssignmentRequest](../resources/roleassignmentrequest.md) object in the response body.

### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_roleassignmentrequest_from_provider"
}-->
```http
POST https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/providers/<id>/roleAssignmentRequests
Content-type: application/json
Content-length: 206

{
  "assignmentLevel": "assignmentLevel-value",
  "requestType": "requestType-value",
  "requestedDateTime": "datetime-value",
  "roleAssignmentStartDateTime": "datetime-value",
  "status": "status-value"
}
```
In the request body, supply a JSON representation of [roleAssignmentRequest](../resources/roleassignmentrequest.md) object.
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.roleAssignmentRequest"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 226

{
  "id": "id-value",
  "assignmentLevel": "assignmentLevel-value",
  "requestType": "requestType-value",
  "requestedDateTime": "datetime-value",
  "roleAssignmentStartDateTime": "datetime-value",
  "status": "status-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create roleAssignmentRequest",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
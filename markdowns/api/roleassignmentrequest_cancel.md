# roleAssignmentRequest: cancel


### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /providers/<id>/roleAssignmentRequests/<id>/cancel
```
### Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {code}|
| Workbook-Session-Id  | Workbook session Id that determines if changes are persisted or not. Optional.|

### Request body

### Response
If successful, this method returns `200, OK` response code. It does not return anything in the response body.

### Example
Here is an example of how to call this API.
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "roleassignmentrequest_cancel"
}-->
```http
POST https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/roleAssignmentRequests('bc6f10e6-6dd9-4393-853e-09e13c036b17_7fd64851-3279-459b-b614-e2b2ba760f5b_7c53453e-d5a4-41e0-8eb1-32d5ec8bfdee')/cancel
```

##### Response
Here is an example of the response. 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "roleAssignmentRequest: cancel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
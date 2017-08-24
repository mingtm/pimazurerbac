# Create roleAssignment

Use this API to create a new roleAssignment.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /roleAssignments

```
### Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {code}|
| Workbook-Session-Id  | Workbook session Id that determines if changes are persisted or not. Optional.|

### Request body
In the request body, supply a JSON representation of [roleAssignment](../resources/roleassignment.md) object.


### Response
If successful, this method returns `201, Created` response code and [roleAssignment](../resources/roleassignment.md) object in the response body.

### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_roleassignment_from_roleassignments"
}-->
```http
POST https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/roleAssignments
Content-type: application/json
Content-length: 162

{
  "originId": "originId-value",
  "isPermanent": true,
  "expirationDateTime": "datetime-value",
  "startDateTime": "datetime-value",
  "level": "level-value"
}
```
In the request body, supply a JSON representation of [roleAssignment](../resources/roleassignment.md) object.
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.roleAssignment"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 182

{
  "id": "id-value",
  "originId": "originId-value",
  "isPermanent": true,
  "expirationDateTime": "datetime-value",
  "startDateTime": "datetime-value",
  "level": "level-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create roleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
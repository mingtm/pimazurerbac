# resource: permissions


### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /providers/<id>/resources('<id>')/permissions
```
### Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {code}|
| Workbook-Session-Id  | Workbook session Id that determines if changes are persisted or not. Optional.|

### Request body

### Response
If successful, this method returns `200, OK` response code and [permission](../resources/permission.md) collection object in the response body.

### Example
Here is an example of how to call this API.
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "resource_permissions"
}-->
```http
GET https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/resources('05a02078-aa1f-482a-8afa-ce1620d03099')/permissions
```

##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.permission",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 123

{
  "value": [
    {
      "accessLevel": "AdminRead",
      "isActive": true,
      "isEligible": false
    },
    {
      "accessLevel": "UserRead",
      "isActive": true,
      "isEligible": false
    },
    {
      "accessLevel": "AdminReadWrite",
      "isActive": true,
      "isEligible": false
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "resource: permissions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
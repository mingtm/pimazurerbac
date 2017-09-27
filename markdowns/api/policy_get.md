# Get policy

Retrieve the properties and relationships of policy object.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /providers/<id>/policies/<id>
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
If successful, this method returns a `200 OK` response code and [policy](../resources/policy.md) object in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_policy"
}-->
```http
GET https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/policies/<id>
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.policy"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 370

{
  "id": "id-value",
  "default": true,
  "lastUpdated": "datetime-value",
  "lastUpdatedBy": "lastUpdatedBy-value",
  "adminEligibleSettings": [
    {
      "ruleIdentifier": "ruleIdentifier-value",
      "setting": "setting-value"
    }
  ],
  "adminMemberSettings": [
    {
      "ruleIdentifier": "ruleIdentifier-value",
      "setting": "setting-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get policy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
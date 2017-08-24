# Create policy

Use this API to create a new policy.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /policies

```
### Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {code}|
| Workbook-Session-Id  | Workbook session Id that determines if changes are persisted or not. Optional.|

### Request body
In the request body, supply a JSON representation of [policy](../resources/policy.md) object.


### Response
If successful, this method returns `201, Created` response code and [policy](../resources/policy.md) object in the response body.

### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_policy_from_policies"
}-->
```http
POST https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/policies
Content-type: application/json
Content-length: 350

{
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
In the request body, supply a JSON representation of [policy](../resources/policy.md) object.
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.policy"
} -->
```http
HTTP/1.1 201 Created
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
  "description": "Create policy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
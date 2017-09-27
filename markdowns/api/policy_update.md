# Update policy

Update the properties of policy object.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
PUT /providers/<id>/policies/<id>
```
### Optional request headers
| Name       | Description|
|:-----------|:-----------|
| Authorization  | Bearer {code}|
| Workbook-Session-Id  | Workbook session Id that determines if changes are persisted or not. Optional.|

### Request body
In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.

| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|adminEligibleSettings|rulesetting||
|adminMemberSettings|rulesetting||
|default|Boolean||
|lastUpdated|DateTimeOffset||
|lastUpdatedBy|String||
|userEligibleSettings|rulesetting||
|userMemberSettings|rulesetting||

### Response
If successful, this method returns a `200 OK` response code and updated [policy](../resources/policy.md) object in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "update_policy"
}-->
```http
PATCH https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/policies/<id>
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
  "description": "Update policy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
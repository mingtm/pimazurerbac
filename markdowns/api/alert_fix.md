# alert: fix


### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /providers/<id>/resources/<id>/alerts/<id>/fix
```
### Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {code}|
| Workbook-Session-Id  | Workbook session Id that determines if changes are persisted or not. Optional.|

### Request body
In the request body, provide a JSON object with the following parameters.

| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|resourceId|String||
|alert|alert||

### Response
If successful, this method returns `200, OK` response code. It does not return anything in the response body.

### Example
Here is an example of how to call this API.
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "alert_fix"
}-->
```http
POST https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/alerts/<id>/fix
Content-type: application/json
Content-length: 937

{
  "resourceId": "resourceId-value",
  "alert": {
    "id": "id-value",
    "resourceId": "resourceId-value",
    "alertName": "alertName-value",
    "alertDescription": "alertDescription-value",
    "numberOfAffectedItems": 99,
    "additionalData": [
      {
        "item": [
          {
            "key": "key-value",
            "value": "value-value"
          }
        ]
      }
    ],
    "lastModifiedDateTime": "datetime-value",
    "lastScannedDateTime": "datetime-value",
    "severityLevel": "severityLevel-value",
    "alertType": "alertType-value",
    "securityImpact": "securityImpact-value",
    "mitigationSteps": "mitigationSteps-value",
    "howToPrevent": "howToPrevent-value",
    "isDisabled": true,
    "isActive": true,
    "isResolvable": true,
    "isConfigurable": true,
    "status": "status-value",
    "settings": [
      {
        "key": "key-value",
        "value": "value-value"
      }
    ]
  }
}
```

##### Response
Here is an example of the response. 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "alert: fix",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
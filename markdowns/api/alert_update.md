# Update alert

Update the properties of alert object.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
PATCH /alerts/<id>
PATCH /providers/<id>/alerts/<id>
PATCH /resources/<id>/alerts/<id>
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
|additionalData|KeyValueList||
|alertDescription|String||
|alertName|String||
|alertType|AlertType||
|howToPrevent|String||
|isActive|Boolean||
|isConfigurable|Boolean||
|isDisabled|Boolean||
|isResolvable|Boolean||
|lastModifiedDateTime|DateTimeOffset||
|lastScannedDateTime|DateTimeOffset||
|mitigationSteps|String||
|numberOfAffectedItems|Int32||
|resourceId|String||
|securityImpact|String||
|settings|KeyValue||
|severityLevel|AlertSeverity||
|status|AlertStatus||

### Response
If successful, this method returns a `200 OK` response code and updated [alert](../resources/alert.md) object in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "update_alert"
}-->
```http
PATCH https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/alerts/<id>
Content-type: application/json
Content-length: 190

{
  "resourceId": "resourceId-value",
  "alertName": "alertName-value",
  "alertDescription": "alertDescription-value",
  "numberOfAffectedItems": 99,
  "additionalData": [
    {
    }
  ]
}
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 210

{
  "id": "id-value",
  "resourceId": "resourceId-value",
  "alertName": "alertName-value",
  "alertDescription": "alertDescription-value",
  "numberOfAffectedItems": 99,
  "additionalData": [
    {
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update alert",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
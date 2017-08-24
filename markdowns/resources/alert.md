# alert resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get alert](../api/alert_get.md) | [alert](alert.md) |Read properties and relationships of alert object.|
|[Update](../api/alert_update.md) | [alert](alert.md)	|Update alert object. |
|[Delete](../api/alert_delete.md) | None |Delete alert object. |
|[Deactivate](../api/alert_deactivate.md)|None||
|[Disable](../api/alert_disable.md)|None||
|[Enable](../api/alert_enable.md)|None||
|[Fix](../api/alert_fix.md)|None||
|[Refresh](../api/alert_refresh.md)|None||
|[Refresh](../api/alert_refresh.md)|None||

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|additionalData|[KeyValueList](keyvaluelist.md) collection||
|alertDescription|String||
|alertName|String||
|alertType|String||
|howToPrevent|String||
|id|String| Read-only.|
|isActive|Boolean||
|isConfigurable|Boolean||
|isDisabled|Boolean||
|isResolvable|Boolean||
|lastModifiedDateTime|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|lastScannedDateTime|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|mitigationSteps|String||
|numberOfAffectedItems|Int32||
|resourceId|String||
|securityImpact|String||
|settings|[KeyValue](keyvalue.md) collection||
|severityLevel|String||
|status|String||

### Relationships
None


### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.alert"
}-->

```json
{
  "additionalData": [{"@odata.type": "microsoft.graph.KeyValueList"}],
  "alertDescription": "String",
  "alertName": "String",
  "alertType": "String",
  "howToPrevent": "String",
  "id": "String (identifier)",
  "isActive": true,
  "isConfigurable": true,
  "isDisabled": true,
  "isResolvable": true,
  "lastModifiedDateTime": "String (timestamp)",
  "lastScannedDateTime": "String (timestamp)",
  "mitigationSteps": "String",
  "numberOfAffectedItems": 1024,
  "resourceId": "String",
  "securityImpact": "String",
  "settings": [{"@odata.type": "microsoft.graph.KeyValue"}],
  "severityLevel": "String",
  "status": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "alert resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
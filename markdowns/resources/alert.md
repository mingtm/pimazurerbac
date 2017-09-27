# alert resource type
Represents a security alert that could be a security weakness of the current system. 

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get alert](../api/alert_get.md) | [alert](alert.md) |Read properties and relationships of alert object.|
|[List alerts](../api/resource_list_alerts.md) |[alert](alert.md) collection| Get a collection of alert objects.|
|[Deactivate](../api/alert_deactivate.md)|None|Deactivate an alert.|
|[Disable](../api/alert_disable.md)|None|Disable an alert.|
|[Enable](../api/alert_enable.md)|None|Enable an alert.|
|[Fix](../api/alert_fix.md)|None|Fix an alert.|
|[Refresh](../api/alert_refresh.md)|None|Refresh the status of the alert.|


### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|additionalData|[KeyValueList](keyvaluelist.md) collection|The additional data of the alert.|
|alertDescription|String|The description of the alert.|
|alertName|String|The alert name.|
|alertType|String|The alert type.|
|howToPrevent|String|The description string of how to prevent the security alert.|
|id|String| The alert id. Read-only.|
|isActive|Boolean|Indicates if the alert is still active.|
|isConfigurable|Boolean|Indicates if the alert setting is configurable.|
|isDisabled|Boolean|Indicates if the alert is disabled.|
|isResolvable|Boolean|Indicates if the alert can be resolved automatically.|
|lastModifiedDateTime|DateTimeOffset|The last time when the security alert is modified. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|lastScannedDateTime|DateTimeOffset|The last time when the alert is scanned. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|mitigationSteps|String|The description string about the steps to mitigate the alert.|
|numberOfAffectedItems|Int32|The number of affected items for the alert.|
|resourceId|String|The resource id.|
|securityImpact|String|The description string of the security impact of the alert.|
|settings|[KeyValue](keyvalue.md) collection|The settings of the alert.|
|severityLevel|String|The severity level of the alert. The value can be ``High``, ``Medium`` and ``Low``.|
|status|String|The status of the alert. The value can be ``Active``, ``Disabled`` and ``Inactive``.|

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
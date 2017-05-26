# activity resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get activity](../api/activity_get.md) | [activity](activity.md) |Read properties and relationships of activity object.|
|[Update](../api/activity_update.md) | [activity](activity.md)	|Update activity object. |
|[Delete](../api/activity_delete.md) | None |Delete activity object. |

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|correlationId|Guid||
|createTime|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|expirationTime|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|id|Guid| Read-only.|
|partitionId|String||
|reason|String||
|sourceType|[SourceType](sourcetype.md)||
|status|String||
|type|String||

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|originalRequestor|[subject](subject.md)| Read-only. Nullable.|
|requestor|[subject](subject.md)| Read-only. Nullable.|
|resource|[resource](resource.md)| Read-only. Nullable.|
|subject|[subject](subject.md)| Read-only. Nullable.|
|target|[target](target.md)| Read-only. Nullable.|

### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.activity"
}-->

```json
{
  "correlationId": "Guid",
  "createTime": "String (timestamp)",
  "expirationTime": "String (timestamp)",
  "id": "Guid (identifier)",
  "partitionId": "String",
  "reason": "String",
  "sourceType": {"@odata.type": "microsoft.graph.SourceType"},
  "status": "String",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "activity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
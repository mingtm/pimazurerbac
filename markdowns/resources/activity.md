# activity resource type
Represents an auditing activity object that is created to track the role management operations, such as an administrator did a role assignment, a user activated his role, a role setting was changed, etc. 

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get activity](../api/activity_get.md) | [activity](activity.md) |Read properties and relationships of activity object.|
|[Update](../api/activity_update.md) | [activity](activity.md)	|Update activity object. |
|[Delete](../api/activity_delete.md) | None |Delete activity object. |
|[My](../api/activity_my.md)|[activity](activity.md) collection||

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|correlationId|String||
|createdDateTime|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|expirationDateTime|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|id|String| Read-only.|
|operationType|String||
|reason|String||
|resourceId|String||
|status|String||

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|originalRequestor|[subject](subject.md)| Read-only. Nullable.|
|requestor|[subject](subject.md)| Read-only. Nullable.|
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
  "correlationId": "String",
  "createdDateTime": "String (timestamp)",
  "expirationDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "operationType": "String",
  "reason": "String",
  "resourceId": "String",
  "status": "String"
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
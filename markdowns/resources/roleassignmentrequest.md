# roleAssignmentRequest resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get roleAssignmentRequest](../api/roleassignmentrequest_get.md) | [roleAssignmentRequest](roleassignmentrequest.md) |Read properties and relationships of roleAssignmentRequest object.|
|[Update](../api/roleassignmentrequest_update.md) | [roleAssignmentRequest](roleassignmentrequest.md)	|Update roleAssignmentRequest object. |
|[Delete](../api/roleassignmentrequest_delete.md) | None |Delete roleAssignmentRequest object. |
|[Cancel](../api/roleassignmentrequest_cancel.md)|None||

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|assignmentLevel|String||
|evaluateOnly|Boolean||
|id|String| Read-only.|
|reason|String||
|requestType|String||
|requestedDate|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|roleAssignmentStartDate|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|schedule|[schedule](schedule.md)||
|status|String||
|statusDetail|[KeyValue](keyvalue.md) collection||

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|roleDefinition|[roleDefinition](roledefinition.md)| Read-only. Nullable.|
|subject|[subject](subject.md)| Read-only. Nullable.|

### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.roleAssignmentRequest"
}-->

```json
{
  "assignmentLevel": "String",
  "evaluateOnly": true,
  "id": "String (identifier)",
  "reason": "String",
  "requestType": "String",
  "requestedDate": "String (timestamp)",
  "roleAssignmentStartDate": "String (timestamp)",
  "schedule": {"@odata.type": "microsoft.graph.schedule"},
  "status": "String",
  "statusDetail": [{"@odata.type": "microsoft.graph.KeyValue"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "roleAssignmentRequest resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
# roleAssignment resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get roleAssignment](../api/roleassignment_get.md) | [roleAssignment](roleassignment.md) |Read properties and relationships of roleAssignment object.|
|[Create roleAssignment](../api/resource_post_roleassignments.md) |[roleAssignment](roleassignment.md)| Create a new roleAssignment by posting to the roleAssignments collection.|
|[Update](../api/roleassignment_update.md) | [roleAssignment](roleassignment.md)	|Update roleAssignment object. |
|[Delete](../api/roleassignment_delete.md) | None |Delete roleAssignment object. |
|[Getmyassignments](../api/roleassignment_getmyassignments.md)|[roleAssignment](roleassignment.md) collection||

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|assignmentType|String||
|expirationDateTime|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|id|String| Read-only.|
|isPermanent|Boolean||
|level|String||
|originId|String||
|startDateTime|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|linkedAssignment|[roleAssignment](roleassignment.md)| Read-only. Nullable.|
|roleDefinition|[roleDefinition](roledefinition.md)| Read-only. Nullable.|
|subject|[subject](subject.md)| Read-only. Nullable.|

### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.roleAssignment"
}-->

```json
{
  "assignmentType": "String",
  "expirationDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "isPermanent": true,
  "level": "String",
  "originId": "String",
  "startDateTime": "String (timestamp)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "roleAssignment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
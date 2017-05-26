# roleAssignment resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get roleAssignment](../api/roleassignment_get.md) | [roleAssignment](roleassignment.md) |Read properties and relationships of roleAssignment object.|
|[Update](../api/roleassignment_update.md) | [roleAssignment](roleassignment.md)	|Update roleAssignment object. |
|[Delete](../api/roleassignment_delete.md) | None |Delete roleAssignment object. |
|[Getmyassignments](../api/roleassignment_getmyassignments.md)|[roleAssignment](roleassignment.md) collection||

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|activationRequired|Boolean||
|assigned|Boolean||
|assignmentExpirationDate|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|assignmentStartDate|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|assignmentType|String||
|derivedEligibleGroup|String||
|eligibilityExpirationDate|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|eligibilityStartDate|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|id|String| Read-only.|
|inherited|Boolean||
|isAssignmentPermanent|Boolean||
|isEligibilityPermanent|Boolean||
|name|String||
|originId|String||

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
  "@odata.type": "microsoft.graph.roleAssignment"
}-->

```json
{
  "activationRequired": true,
  "assigned": true,
  "assignmentExpirationDate": "String (timestamp)",
  "assignmentStartDate": "String (timestamp)",
  "assignmentType": "String",
  "derivedEligibleGroup": "String",
  "eligibilityExpirationDate": "String (timestamp)",
  "eligibilityStartDate": "String (timestamp)",
  "id": "String (identifier)",
  "inherited": true,
  "isAssignmentPermanent": true,
  "isEligibilityPermanent": true,
  "name": "String",
  "originId": "String"
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
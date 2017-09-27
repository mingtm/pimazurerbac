# roleAssignment resource type
Represents a role assignment that is assigned to a principal for a resource.

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[List roleAssignments](../api/roleassignment_list.md) | [roleAssignment](roleassignment.md) |List roleAssignment collection.|
|[Get roleAssignment](../api/roleassignment_get.md) | [roleAssignment](roleassignment.md) |Read properties and relationships of roleAssignment object.|

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|assignmentType|String|The assignment type. The value can be ``Direct`` - for a direct role assignment, ``Inherited`` - the role assignment is inherited from a parent resource scope, or ``Group`` - the role assignment is from a user group role assignment.|
|expirationDateTime|DateTimeOffset|For a non-permanent role assignment, this is the time when the role assignment will be expired. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|id|String| The id of the role assignment. Read-only.|
|isPermanent|Boolean|Indicates if the role assignment is permanent.|
|level|String|The level of the assignment. The value can be ``Eligible`` or ``Member``.|
|originId|String|The original id of the resource that is used to identify the resource in the provider.|
|startDateTime|DateTimeOffset|The start time of the role assignment. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|linkedAssignment|[roleAssignment](roleassignment.md)|The linked role assignment. When an eligible role assignment is activated by the user, a member role assignment object will be created in the system. Meanwhile, the member role assignment object will have linkedAssignment set to the eligible role assignment object. Read-only. Nullable.|
|roleDefinition|[roleDefinition](roledefinition.md)|The role definition associated with the role assignment. Read-only. Nullable.|
|subject|[subject](subject.md)|The principal subject associated with the role assignment. Read-only. Nullable.|

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
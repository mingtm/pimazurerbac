# activity resource type
Represents an auditing activity object that is created to track the role management operations, such as an administrator did a role assignment, a user activated his role, a role setting was changed, etc. 

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get activity](../api/activity_get.md) | [activity](activity.md) |Read properties and relationships of activity object.|


### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|correlationId|String|The GUID string correlating the operation that triggered the auditing activity.|
|createdDateTime|DateTimeOffset|The time when the auditing activity is created. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|expirationDateTime|DateTimeOffset|This field is meaningful only if the operation is to do a role assignment or role activation. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|id|String|The id of the activity object. Read-only.|
|operationType|String|The operation type. For example, "Create request for eligible role assignment", "Add eligible role assignment", "Refresh alert", etc. |
|reason|String|The reason provided by the user when he activates the role assignment.|
|resourceId|String|The Azure resource id.|
|status|String|The status of the associated operation. The value can be "Succeeded" or "Failed".|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|originalRequestor|[subject](subject.md)| The original reqestor for the operation. Read-only. Nullable.|
|requestor|[subject](subject.md)| The direct requestor. Read-only. Nullable.|
|subject|[subject](subject.md)| The user subject that is involved in the operation. Read-only. Nullable.|
|target|[target](target.md)| The target object involved in the operation. Read-only. Nullable.|

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
# target resource type
The operation target. This entity type is used for auditing purpose.

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|displayName|String|The display name of the target.|
|id|String| The target id. Read-only.|
|internalType|String|The PIM internal type of the target. The value can be ``Resource``, ``RoleAssignment``, ``RoleAssignmentRequest``, and ``Subject``.|
|objectType|String|The target object type. The value can be ``Alert``, ``Subject``, ``RoleDefintion``, ``RoleAssignment``, ``RoleAssignmentRequest``, ``Resource``, ``Tenant``, ``Request``, ``Policy``, ``Provider``, ``PolicyRoleAssociation``, ``JobRequest``, and ``AlertInfo``.|
|uniqueName|String|The unique name of the target.|

### Relationships
None


### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.target"
}-->

```json
{
  "displayName": "String",
  "id": "String (identifier)",
  "internalType": "String",
  "objectType": "String",
  "uniqueName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "target resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
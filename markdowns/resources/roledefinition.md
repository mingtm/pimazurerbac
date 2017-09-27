# roleDefinition resource type

Represents the role definition. For Azure RBAC provider, the role definition can be Owner, Reader, Contributor, etc.


### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[List roleDefinitions](../api/roledefinition_list.md) | [roleDefinition](roledefinition.md) |Get roleDefinition collection.|
|[Get roleDefinition](../api/roledefinition_get.md) | [roleDefinition](roledefinition.md) |Read properties and relationships of roleDefinition object.|
|[Create roleDefinition](../api/resource_post_roledefinitions.md) |[roleDefinition](roledefinition.md)| Create a new roleDefinition by posting to the roleDefinitions collection.|


### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|activationRequiredCount|Int32|The number of eligible role assignments associated with the role definition.|
|assignedCount|Int32|The number of member role assignments associated with the role definition.|
|displayName|String|The role definition display name.|
|id|String| The id of the role definition. Read-only.|
|ruleSettings|[rulesetting](rulesetting.md) collection|The rule settings for the role definition.|
|subjectCount|Int32|The number of subjects that are assigned with the role.|
|templateId|String|The role definition template id that is managed by the resource provider.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|resource|[resource](resource.md)|The associated resource for the role definition. Read-only. Nullable.|

### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.roleDefinition"
}-->

```json
{
  "activationRequiredCount": 1024,
  "assignedCount": 1024,
  "displayName": "String",
  "id": "String (identifier)",
  "ruleSettings": [{"@odata.type": "microsoft.graph.rulesetting"}],
  "subjectCount": 1024,
  "templateId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "roleDefinition resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
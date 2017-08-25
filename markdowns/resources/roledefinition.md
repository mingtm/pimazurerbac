# roleDefinition resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get roleDefinition](../api/roledefinition_get.md) | [roleDefinition](roledefinition.md) |Read properties and relationships of roleDefinition object.|
|[Create roleDefinition](../api/resource_post_roledefinitions.md) |[roleDefinition](roledefinition.md)| Create a new roleDefinition by posting to the roleDefinitions collection.|
|[Update](../api/roledefinition_update.md) | [roleDefinition](roledefinition.md)	|Update roleDefinition object. |
|[Delete](../api/roledefinition_delete.md) | None |Delete roleDefinition object. |

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|activationRequiredCount|Int32||
|assignedCount|Int32||
|displayName|String||
|id|String| Read-only.|
|ruleSettings|[rulesetting](rulesetting.md) collection||
|subjectCount|Int32||
|templateId|String||

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|resource|[resource](resource.md)| Read-only. Nullable.|

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
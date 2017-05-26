# resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get resource](../api/resource_get.md) | [resource](resource.md) |Read properties and relationships of resource object.|
|[List alerts](../api/resource_list_alerts.md) |[alert](alert.md) collection| Get a alert object collection.|
|[List roleAssignments](../api/resource_list_roleassignments.md) |[roleAssignment](roleassignment.md) collection| Get a roleAssignment object collection.|
|[List roleDefinitions](../api/resource_list_roledefinitions.md) |[roleDefinition](roledefinition.md) collection| Get a roleDefinition object collection.|
|[Accesslevel](../api/resource_accesslevel.md)|String||
|[Activities](../api/resource_activities.md)|[resource](resource.md) collection||

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|displayName|String|Resource display name.|
|id|String| Read-only. Resource unique id.|
|originalId|String|Resource original id.|
|resourceType|String|Resource type.|
|roleAssignmentCount|Int32|Count of role assignments for the given resource.|
|roleDefinitionCount|Int32|Count of role definitions for the give resource.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|alerts|[alert](alert.md) collection| Read-only. Nullable.|
|parent|[resource](resource.md)| Read-only. Nullable.|
|provider|[provider](provider.md)| Read-only. |
|roleAssignments|[roleAssignment](roleassignment.md) collection| Read-only. Nullable.|
|roleDefinitions|[roleDefinition](roledefinition.md) collection| Read-only. Nullable.|

### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.resource"
}-->

```json
{
  "displayName": "String",
  "id": "String (identifier)",
  "originalId": "String",
  "resourceType": "String",
  "roleAssignmentCount": 1024,
  "roleDefinitionCount": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "resource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
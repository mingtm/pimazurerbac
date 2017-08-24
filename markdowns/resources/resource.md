# resource resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get resource](../api/resource_get.md) | [resource](resource.md) |Read properties and relationships of resource object.|
|[Create alert](../api/resource_post_alerts.md) |[alert](alert.md)| Create a new alert by posting to the alerts collection.|
|[List alerts](../api/resource_list_alerts.md) |[alert](alert.md) collection| Get a alert object collection.|
|[Create roleAssignment](../api/resource_post_roleassignments.md) |[roleAssignment](roleassignment.md)| Create a new roleAssignment by posting to the roleAssignments collection.|
|[List roleAssignments](../api/resource_list_roleassignments.md) |[roleAssignment](roleassignment.md) collection| Get a roleAssignment object collection.|
|[Create roleDefinition](../api/resource_post_roledefinitions.md) |[roleDefinition](roledefinition.md)| Create a new roleDefinition by posting to the roleDefinitions collection.|
|[List roleDefinitions](../api/resource_list_roledefinitions.md) |[roleDefinition](roledefinition.md) collection| Get a roleDefinition object collection.|
|[Update](../api/resource_update.md) | [resource](resource.md)	|Update resource object. |
|[Delete](../api/resource_delete.md) | None |Delete resource object. |
|[Permissions](../api/resource_permissions.md)|[permission](permission.md) collection||

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|displayName|String||
|id|String| Read-only.|
|originalId|String||
|resourceType|String||
|roleAssignmentCount|Int32||
|roleDefinitionCount|Int32||

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|alerts|[alert](alert.md) collection| Read-only. Nullable.|
|parent|[resource](resource.md)| Read-only. Nullable.|
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
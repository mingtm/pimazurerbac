# resource resource type
Represents the resource object. For Azure RBAC provider, the resource can be a subscription, a virtual machine, a SQL database, etc.



### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[List resources](../api/resource_list.md) | [resource](resource.md) |List resource collection.|
|[Get resource](../api/resource_get.md) | [resource](resource.md) |Read properties and relationships of resource object.|
|[Create](../api/resource_update.md) | [resource](resource.md)	|Create resource object. For Azure RBAC provider, creating resource is not allowed.|
|[List roleAssignments](../api/resource_list_roleassignments.md) |[roleAssignment](roleassignment.md) collection| Get a roleAssignment object collection for the given resource.|
|[List roleDefinitions](../api/resource_list_roledefinitions.md) |[roleDefinition](roledefinition.md) collection| Get a roleDefinition object collection for the given resource.|
|[Permissions](../api/resource_permissions.md)|[permission](permission.md) collection|Get a permission object collection for the given resource and requestor.|

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|displayName|String|The resource display name.|
|id|String| The id of the resource. This is in GUID format. Read-only.|
|originalId|String|The original id of the resource in its provider. For example, for Azure RBAC provider, a subscription resource's original id can be /subscriptions/c14ae696-5e0c-4e5d-88cc-bef6637737ac. |
|resourceType|String|Resource type. For example, for Azure RBAC provider, the type could be subscription, ResourceGroup, Microsoft.Sql/server, etc.|
|roleAssignmentCount|Int32|The number of role assignments for the given resource.|
|roleDefinitionCount|Int32|The number of role definitions for the given resource.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|alerts|[alert](alert.md) collection| The security alerts that are associated with the resource. Read-only. Nullable.|
|parent|[resource](resource.md)| The parent resource. Read-only. Nullable.|
|roleAssignments|[roleAssignment](roleassignment.md) collection| The collection of role assignments for the resource. Read-only. Nullable.|
|roleDefinitions|[roleDefinition](roledefinition.md) collection| The collection of role defintions for the resource. Read-only. Nullable.|

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
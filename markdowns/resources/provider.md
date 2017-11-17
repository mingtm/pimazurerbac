# provider resource type

Represents the resource provider that is managed by Privileged Identity Management (PIM). Currently Azure RBAC is the only provider onboarded to PIM. 


### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get provider](../api/provider_get.md) | [provider](provider.md) |Read properties and relationships of provider object.|

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|displayName|String|Provider display name.|
|id|String| Provider id (in GUID format). Read-only.|


### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|activities|[activity](activity.md) collection|  Read-only. Nullable.|
|alerts|[alert](alert.md) collection| Read-only. Nullable.|
|policies|[policy](policy.md) collection|Read-only. Nullable.|
|resources|[resource](resource.md) collection| Read-only. Nullable.|
|roleAssignmentRequests|[roleAssignmentRequest](roleassignmentrequest.md) collection| Read-only. Nullable.|
|roleAssignments|[roleAssignment](roleassignment.md) collection| Read-only. Nullable.|
|roleDefinitions|[roleDefinition](roledefinition.md) collection| Read-only. Nullable.|

### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.provider"
}-->

```json
{
  "displayName": "String",
  "id": "String (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "provider resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
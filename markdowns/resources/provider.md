# provider resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get provider](../api/provider_get.md) | [provider](provider.md) |Read properties and relationships of provider object.|
|[Create activity](../api/provider_post_activities.md) |[activity](activity.md)| Create a new activity by posting to the activities collection.|
|[List activities](../api/provider_list_activities.md) |[activity](activity.md) collection| Get a activity object collection.|
|[Create alert](../api/provider_post_alerts.md) |[alert](alert.md)| Create a new alert by posting to the alerts collection.|
|[List alerts](../api/provider_list_alerts.md) |[alert](alert.md) collection| Get a alert object collection.|
|[Create policy](../api/provider_post_policies.md) |[policy](policy.md)| Create a new policy by posting to the policies collection.|
|[List policies](../api/provider_list_policies.md) |[policy](policy.md) collection| Get a policy object collection.|
|[Create resource](../api/provider_post_resources.md) |[resource](resource.md)| Create a new resource by posting to the resources collection.|
|[List resources](../api/provider_list_resources.md) |[resource](resource.md) collection| Get a resource object collection.|
|[Create roleAssignmentRequest](../api/provider_post_roleassignmentrequests.md) |[roleAssignmentRequest](roleassignmentrequest.md)| Create a new roleAssignmentRequest by posting to the roleAssignmentRequests collection.|
|[List roleAssignmentRequests](../api/provider_list_roleassignmentrequests.md) |[roleAssignmentRequest](roleassignmentrequest.md) collection| Get a roleAssignmentRequest object collection.|
|[Create roleAssignment](../api/provider_post_roleassignments.md) |[roleAssignment](roleassignment.md)| Create a new roleAssignment by posting to the roleAssignments collection.|
|[List roleAssignments](../api/provider_list_roleassignments.md) |[roleAssignment](roleassignment.md) collection| Get a roleAssignment object collection.|
|[Create roleDefinition](../api/provider_post_roledefinitions.md) |[roleDefinition](roledefinition.md)| Create a new roleDefinition by posting to the roleDefinitions collection.|
|[List roleDefinitions](../api/provider_list_roledefinitions.md) |[roleDefinition](roledefinition.md) collection| Get a roleDefinition object collection.|
|[Update](../api/provider_update.md) | [provider](provider.md)	|Update provider object. |
|[Delete](../api/provider_delete.md) | None |Delete provider object. |

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|displayName|String||
|id|String| Read-only.|
|isMultiTenant|Boolean||
|ownerTemplateId|String||
|readerTemplateId|String||
|requiresResourceProvisioning|Boolean||

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|activities|[activity](activity.md) collection| Read-only. Nullable.|
|addRoleAssignmentConnection|[providerConnection](providerconnection.md)| Read-only. Nullable.|
|alerts|[alert](alert.md) collection| Read-only. Nullable.|
|getResourceConnection|[providerConnection](providerconnection.md)| Read-only. Nullable.|
|getResourcesConnection|[providerConnection](providerconnection.md)| Read-only. Nullable.|
|getRoleAssignmentConnection|[providerConnection](providerconnection.md)| Read-only. Nullable.|
|getRoleAssignmentsForResourceAndRoleDefinitionConnection|[providerConnection](providerconnection.md)| Read-only. Nullable.|
|getRoleAssignmentsForResourceConnection|[providerConnection](providerconnection.md)| Read-only. Nullable.|
|getRoleDefinitionConnection|[providerConnection](providerconnection.md)| Read-only. Nullable.|
|getRoleDefinitionsConnection|[providerConnection](providerconnection.md)| Read-only. Nullable.|
|policies|[policy](policy.md) collection| Read-only. Nullable.|
|removeRoleAssignmentConnection|[providerConnection](providerconnection.md)| Read-only. Nullable.|
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
  "id": "String (identifier)",
  "isMultiTenant": true,
  "ownerTemplateId": "String",
  "readerTemplateId": "String",
  "requiresResourceProvisioning": true
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
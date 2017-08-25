# provider resource type

Represents the resource provider that is managed by Privileged Identity Management (PIM). Currently Azure RBAC is the only provider onboarded to PIM. 


### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get provider](../api/provider_get.md) | [provider](provider.md) |Read properties and relationships of provider object.|
|[Create provider](../api/provider_update.md) | [provider](provider.md)	|Create a new provider. |

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|displayName|String|Provider display name.|
|id|String| Provider id (in GUID format). Read-only.|
|isMultiTenant|Boolean|Indicate if the provider supports multiple tenants. (Not used currently.) |
|ownerTemplateId|String|The template id for owner read/write operations. (Not used currently.)|
|readerTemplateId|String|The template id for read operations. (Not used currently.)|
|requiresResourceProvisioning|Boolean|The provider requires resource provisioning.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|activities|[activity](activity.md) collection| TODO: Remove this from entity. |
|addRoleAssignmentConnection|[providerConnection](providerconnection.md)|The external provider connection to add role assignment. Read-only. Nullable.|
|alerts|[alert](alert.md) collection| TODO: Remove this navigation.|
|getResourceConnection|[providerConnection](providerconnection.md)|The external provider connection to get resource. Read-only. Nullable.|
|getResourcesConnection|[providerConnection](providerconnection.md)| The external provider connection to list resources. Read-only. Nullable.|
|getRoleAssignmentConnection|[providerConnection](providerconnection.md)| The external provider connection to get a role assignment. Read-only. Nullable.|
|getRoleAssignmentsForResourceAndRoleDefinitionConnection|[providerConnection](providerconnection.md)| The external provider connection to get role assignments with the given resource and role definition. Read-only. Nullable.|
|getRoleAssignmentsForResourceConnection|[providerConnection](providerconnection.md)| The external provider connection to get role assignments for a given resource. Read-only. Nullable.|
|getRoleDefinitionConnection|[providerConnection](providerconnection.md)| The external provider connection to get a role definition. Read-only. Nullable.|
|getRoleDefinitionsConnection|[providerConnection](providerconnection.md)| The external provider connection to list role definitions. Read-only. Nullable.|
|policies|[policy](policy.md) collection|TODO: Remove this from entity.|
|removeRoleAssignmentConnection|[providerConnection](providerconnection.md)| The external provider connection to remove a role assignment. Read-only. Nullable.|
|resources|[resource](resource.md) collection| Read-only. Nullable.|
|roleAssignmentRequests|[roleAssignmentRequest](roleassignmentrequest.md) collection| TODO: Remove this navigation.|
|roleAssignments|[roleAssignment](roleassignment.md) collection| TODO: Remove this navigation.|
|roleDefinitions|[roleDefinition](roledefinition.md) collection| TODO: Remove this navigation.|

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
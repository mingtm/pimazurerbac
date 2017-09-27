# Service root
Azure RBAC Privileged Identity Management (PIM) service allows the Azure resource administrators to manage, control, and monitor access for the resources. Rather than the traditional permanent role assignments, PIM RBAC supports the temporary (eligible) role assignments with a time schedule configured, and allows the user to activate the role assignment in the way like Just-In-Time (JIT) but with more controls.

Here is the list of methods that are provided by Azure RBAC Privileged Identity Management service.

The service is built on top of OData. To filter the results from the query, use the standard OData $filter expressions in the URIs.

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[List activities](../api/activity_list.md) | [activity](activity.md) collection |Get activity object collection. |
|[List alerts](../api/alert_list.md) | [alert](alert.md) collection |Get alert object collection. |
|[Create policy](../api/policy_post_policies.md) |[policy](policy.md)| Create a new policy by posting to the policies collection.|
|[List policies](../api/policy_list.md) | [policy](policy.md) collection |Get policy object collection. |
|[Create provider](../api/provider_post_providers.md) |[provider](provider.md)| Create a new provider by posting to the providers collection.|
|[List providers](../api/provider_list.md) | [provider](provider.md) collection |Get provider object collection. |
|[List resources](../api/resource_list.md) | [resource](resource.md) collection |Get resource object collection. |
|[Create roleAssignmentRequest](../api/roleassignmentrequest_post_roleassignmentrequests.md) |[roleAssignmentRequest](roleassignmentrequest.md)| Create a new roleAssignmentRequest by posting to the roleAssignmentRequests collection.|
|[List roleAssignmentRequests](../api/roleassignmentrequest_list.md) | [roleAssignmentRequest](roleassignmentrequest.md) collection |Get roleAssignmentRequest object collection. |
|[List roleAssignments](../api/roleassignment_list.md) | [roleAssignment](roleassignment.md) collection |Get roleAssignment object collection. |
|[Create roleDefinition](../api/roledefinition_post_roledefinitions.md) |[roleDefinition](roledefinition.md)| Create a new roleDefinition by posting to the roleDefinitions collection.|
|[List roleDefinitions](../api/roledefinition_list.md) | [roleDefinition](roledefinition.md) collection |Get roleDefinition object collection. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Service root",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
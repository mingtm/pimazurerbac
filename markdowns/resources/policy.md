# policy resource type
The policy defines the prerequisites that will be checked when an administrator tries to add a new role assignment or a user tries to activate his role.



### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[List policy](../api/policy_list.md) | [policy](policy.md) |List policy objects.|
|[Get policy](../api/policy_get.md) | [policy](policy.md) |Read properties and relationships of policy object.|
|[Update](../api/policy_update.md) | [policy](policy.md)	|Update policy object. |

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|adminEligibleSettings|[rulesetting](rulesetting.md) collection|The rule settings that are evaluated when an administrator tries to add an eligible role assignment.|
|adminMemberSettings|[rulesetting](rulesetting.md) collection|The rule settings that are evaluated when an administrator tries to add a direct member role assignment.|
|default|Boolean|Indicate if the policy is a default policy|
|id|String| The id of the policy. Read-only.|
|lastUpdated|DateTimeOffset|The time when the policy was last updated. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|lastUpdatedBy|String|The display name of the administrator who updated the policy.|
|userEligibleSettings|[rulesetting](rulesetting.md) collection|The rule settings that are evaluated when a user tries to add an eligible role assignment. This is not used for Azure RBAC provider.|
|userMemberSettings|[rulesetting](rulesetting.md) collection|The rule settings that are evaluated when a user tries to activate his role assignment.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|resource|[resource](resource.md)| The resource that is enforced with this policy. Read-only. Nullable.|
|roleDefinitions|[roleDefinition](roledefinition.md) collection| The role definitions that are enforced with this policy. Read-only. Nullable.|

### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.policy"
}-->

```json
{
  "adminEligibleSettings": [{"@odata.type": "microsoft.graph.rulesetting"}],
  "adminMemberSettings": [{"@odata.type": "microsoft.graph.rulesetting"}],
  "default": true,
  "id": "String (identifier)",
  "lastUpdated": "String (timestamp)",
  "lastUpdatedBy": "String",
  "userEligibleSettings": [{"@odata.type": "microsoft.graph.rulesetting"}],
  "userMemberSettings": [{"@odata.type": "microsoft.graph.rulesetting"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "policy resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
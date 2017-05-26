# policy resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get policy](../api/policy_get.md) | [policy](policy.md) |Read properties and relationships of policy object.|
|[Create roleDefinition](../api/policy_post_roledefinitions.md) |[roleDefinition](roledefinition.md)| Create a new roleDefinition by posting to the roleDefinitions collection.|
|[List roleDefinitions](../api/policy_list_roledefinitions.md) |[roleDefinition](roledefinition.md) collection| Get a roleDefinition object collection.|
|[Update](../api/policy_update.md) | [policy](policy.md)	|Update policy object. |
|[Delete](../api/policy_delete.md) | None |Delete policy object. |

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|adminEligibleSettings|[rulesetting](rulesetting.md) collection||
|adminMemberSettings|[rulesetting](rulesetting.md) collection||
|default|Boolean||
|id|String| Read-only.|
|lastUpdated|DateTimeOffset|The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|lastUpdatedBy|String||
|userEligibleSettings|[rulesetting](rulesetting.md) collection||
|userMemberSettings|[rulesetting](rulesetting.md) collection||

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|resource|[resource](resource.md)| Read-only. Nullable.|
|roleDefinitions|[roleDefinition](roledefinition.md) collection| Read-only. Nullable.|

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
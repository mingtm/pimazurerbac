# roleAssignmentRequest resource type
Represents the request of role assignment operation. The request can be a new role assignment, removing role assignment, self activation, self deactivation, etc.

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[List roleAssignmentRequests](../api/roleassignmentrequest_list.md) | [roleAssignmentRequest collection](roleassignmentrequest.md) |Get roleAssignmentRequest collection.|
|[Create](../api/roleassignmentrequest_post.md) | [roleAssignmentRequest](roleassignmentrequest.md)	|Create roleAssignmentRequest object. |
|[Cancel](../api/roleassignmentrequest_cancel.md)|[roleAssignmentRequest](roleassignmentrequest.md)|Cancel a pending role assignment request.|

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|assignmentLevel|String|The role assignment level. The value can be ``Eligible`` and ``Member``.|
|evaluateOnly|Boolean|Indicates if the role assignment is for evaluation purpose only.|
|id|String| The id of the role assignment request. Read-only.|
|reason|String|The user provided reason for the role assignment request.|
|requestType|String|The type of the role assignment request. The value can be ``AdminAdd``, ``UserAdd``, ``AdminUpdate``, ``AdminRemove``, and ``UserRemove``.|
|requestedDateTime|DateTimeOffset|The request create time. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|roleAssignmentStartDateTime|DateTimeOffset|The start time for the role assignment. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|schedule|[schedule](schedule.md)|The schedule of the role assignment request.|
|status|String|The status of the role assignment request. The value can be ``Accepted``, ``PendingEvaluation``, ``Granted``, ``Denied``, ``PendingProvisioning``, ``Provisioned``, `` PendingRevocation``, ``Revoked``, ``Canceled``, ``Failed``, ``PendingApprovalProvisioning``, and ``PendingApproval``.|
|statusDetail|[KeyValue](keyvalue.md) collection|The details of the request status.|
|targetLinkedRoleAssignmentId|String|The target linked role assignment id. For example, when a user tries to activate an eligible role assignment, TargetLinkedRoleAssignmentId will be the eligible role assignment id in the request. |

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|roleDefinition|[roleDefinition](roledefinition.md)|The role definition that the request aims to. Read-only. Nullable.|
|subject|[subject](subject.md)| The  user/group principal. Read-only. Nullable.|

### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.roleAssignmentRequest"
}-->

```json
{
  "assignmentLevel": "String",
  "evaluateOnly": true,
  "id": "String (identifier)",
  "reason": "String",
  "requestType": "String",
  "requestedDateTime": "String (timestamp)",
  "roleAssignmentStartDateTime": "String (timestamp)",
  "schedule": {"@odata.type": "microsoft.graph.schedule"},
  "status": "String",
  "statusDetail": [{"@odata.type": "microsoft.graph.KeyValue"}],
  "targetLinkedRoleAssignmentId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "roleAssignmentRequest resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
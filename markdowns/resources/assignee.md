# assignee resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get assignee](../api/assignee_get.md) | [assignee](assignee.md) |Read properties and relationships of assignee object.|
|[Update](../api/assignee_update.md) | [assignee](assignee.md)	|Update assignee object. |
|[Delete](../api/assignee_delete.md) | None |Delete assignee object. |

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|assigneeType|String||
|displayName|String||
|email|String||
|id|String| Read-only.|
|principalName|String||
|tenantId|String||

### Relationships
None


### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.assignee"
}-->

```json
{
  "assigneeType": "String",
  "displayName": "String",
  "email": "String",
  "id": "String (identifier)",
  "principalName": "String",
  "tenantId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "assignee resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
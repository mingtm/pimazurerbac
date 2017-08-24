# target resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get target](../api/target_get.md) | [target](target.md) |Read properties and relationships of target object.|
|[Update](../api/target_update.md) | [target](target.md)	|Update target object. |
|[Delete](../api/target_delete.md) | None |Delete target object. |

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|displayName|String||
|id|String| Read-only.|
|internalType|String||
|objectType|String||
|uniqueName|String||

### Relationships
None


### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.target"
}-->

```json
{
  "displayName": "String",
  "id": "String (identifier)",
  "internalType": "String",
  "objectType": "String",
  "uniqueName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "target resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
# providerConnection resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get providerConnection](../api/providerconnection_get.md) | [providerConnection](providerconnection.md) |Read properties and relationships of providerConnection object.|
|[Update](../api/providerconnection_update.md) | [providerConnection](providerconnection.md)	|Update providerConnection object. |
|[Delete](../api/providerconnection_delete.md) | None |Delete providerConnection object. |

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|content|String||
|contentType|String||
|headers|[KeyValue](keyvalue.md) collection||
|httpMethod|String||
|url|String| Read-only.|

### Relationships
None


### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.providerConnection"
}-->

```json
{
  "content": "String",
  "contentType": "String",
  "headers": [{"@odata.type": "microsoft.graph.KeyValue"}],
  "httpMethod": "String",
  "url": "String (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "providerConnection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
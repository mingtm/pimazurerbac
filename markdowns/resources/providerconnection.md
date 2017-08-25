# providerConnection resource type
Represents the HTTP connection to the external provider. 


### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|content|String|The http content.|
|contentType|String|The HTTP content type.|
|headers|[KeyValue](keyvalue.md) collection|The HTTP headers.|
|httpMethod|String|The HTTP method.|
|url|String| URL for the connection. Read-only.|

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
# subject resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get subject](../api/subject_get.md) | [subject](subject.md) |Read properties and relationships of subject object.|
|[Update](../api/subject_update.md) | [subject](subject.md)	|Update subject object. |
|[Delete](../api/subject_delete.md) | None |Delete subject object. |

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|displayName|String||
|email|String||
|id|String| Read-only.|
|principalName|String||
|type|String||

### Relationships
None


### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.subject"
}-->

```json
{
  "displayName": "String",
  "email": "String",
  "id": "String (identifier)",
  "principalName": "String",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "subject resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
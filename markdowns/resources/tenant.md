# tenant resource type




### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get tenant](../api/tenant_get.md) | [tenant](tenant.md) |Read properties and relationships of tenant object.|
|[Update](../api/tenant_update.md) | [tenant](tenant.md)	|Update tenant object. |
|[Delete](../api/tenant_delete.md) | None |Delete tenant object. |

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|additionalInformation|String||
|displayName|String||
|id|String| Read-only.|
|initialDomainName|String||
|status|String||

### Relationships
None


### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.tenant"
}-->

```json
{
  "additionalInformation": "String",
  "displayName": "String",
  "id": "String (identifier)",
  "initialDomainName": "String",
  "status": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "tenant resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
# permission resource type
The permissions that the requestor has for the specific resource.



### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|accessLevel|String|The access level. Valid values: ``None``, ``UserRead``, ``AdminRead``, and ``AdminReadWrite``.|
|isActive|Boolean|Indicate if the the requestor has the active role for the access level.|
|isEligible|Boolean|Indicate if the requestor has the eligible role for the access level.|

### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.permission"
}-->

```json
{
  "accessLevel": "String",
  "isActive": true,
  "isEligible": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "permission resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
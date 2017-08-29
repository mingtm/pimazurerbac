# subject resource type
The user/group subject.


### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|displayName|String|Subject display name.|
|email|String|The subject's email.|
|id|String| The subject id. Read-only.|
|principalName|The principal name of the subject. String||
|type|String|The type of the subject. The value can be ``User``, ``Group``, ``ServicePrincipal``, ``GroupSecurityNotEnabled``, and ``Role``.|

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
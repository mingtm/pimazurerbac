# rulesetting resource type

The rule setting for role assignment operation.


### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|ruleIdentifier|String|The id of the rule. For example, ``ExpirationRule`` and ``MfaRule``.|
|setting|String|The settings of the rule. The value is a JSON string with a list of pairs in the format of Parameter_Name:Parameter_Value. For example, {"permanentAssignment":false,"maximumGrantPeriodInMinutes":129600}|

### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.rulesetting"
}-->

```json
{
  "ruleIdentifier": "String",
  "setting": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "rulesetting resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
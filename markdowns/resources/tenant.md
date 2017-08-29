# tenant resource type
The tenant object.

### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|additionalInformation|String|The additional information of the tenant.|
|displayName|String|The display name of the tenant.|
|id|String| The tenant id. Read-only.|
|initialDomainName| String|The initial domain name of the tenant.|
|status|String|The status of the tenant. The value can be ``Unknown``, ``NotRegisteredYet``, ``RegisteredSetupInProgress``, ``RegistrationAndSetupCompleted``, ``RegistrationFailed``, ``RegistrationTimeout``, ``Disabled``, ``UnregisterStarted``, ``UnregisterInProgress``, and ``UnregisterCompleted``.|

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
# Create provider

Use this API to create a new provider.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /providers

```
### Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {code}|
| Workbook-Session-Id  | Workbook session Id that determines if changes are persisted or not. Optional.|

### Request body
In the request body, supply a JSON representation of [provider](../resources/provider.md) object.


### Response
If successful, this method returns `201, Created` response code and [provider](../resources/provider.md) object in the response body.

### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_provider_from_providers"
}-->
```http
POST https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/providers
Content-type: application/json
Content-length: 199

{
  "displayName": "displayName-value",
  "ownerTemplateId": "ownerTemplateId-value",
  "readerTemplateId": "readerTemplateId-value",
  "requiresResourceProvisioning": true,
  "isMultiTenant": true
}
```
In the request body, supply a JSON representation of [provider](../resources/provider.md) object.
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.provider"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 219

{
  "id": "id-value",
  "displayName": "displayName-value",
  "ownerTemplateId": "ownerTemplateId-value",
  "readerTemplateId": "readerTemplateId-value",
  "requiresResourceProvisioning": true,
  "isMultiTenant": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create provider",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
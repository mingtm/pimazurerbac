# Create provider

Use this API to create a new provider.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /providers
```
### Optional request headers
| Name       | Description|
|:-----------|:-----------|
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
  "name": "update_provider"
}-->
```http
POST https://graph.microsoft.com/beta/providers
Content-type: application/json
Content-length: 199

{
    "id": "id-value",
    "displayName": "displayName-value",
    "ownerTemplateId": "ownerTemplateId-value",
    "readerTemplateId": "readerTemplateId-value",
    "requiresResourceProvisioning": true,
    "isMultiTenant": true,
    "GetResourcesConnection": {
        "content": "String",
        "contentType": "String",
        "headers": [ { "@odata.type": "microsoft.graph.KeyValue" } ],
        "httpMethod": "String",
        "url": "String (identifier)"
    },
    "GetResourcesConnection": {
        "content": "String",
        "contentType": "String",
        "headers": [ { "@odata.type": "microsoft.graph.KeyValue" } ],
        "httpMethod": "String",
        "url": "String (identifier)"
    },
    "GetRoleDefinitionsConnection": {
        "content": "String",
        "contentType": "String",
        "headers": [ { "@odata.type": "microsoft.graph.KeyValue" } ],
        "httpMethod": "String",
        "url": "String (identifier)"
    },
    "GetRoleDefinitionConnection": {
        "content": "String",
        "contentType": "String",
        "headers": [ { "@odata.type": "microsoft.graph.KeyValue" } ],
        "httpMethod": "String",
        "url": "String (identifier)"
    },
    "GetRoleAssignmentsForResourceConnection": {
        "content": "String",
        "contentType": "String",
        "headers": [ { "@odata.type": "microsoft.graph.KeyValue" } ],
        "httpMethod": "String",
        "url": "String (identifier)"
    },
    "GetRoleAssignmentsForResourceAndRoleDefinitionConnection": {
        "content": "String",
        "contentType": "String",
        "headers": [ { "@odata.type": "microsoft.graph.KeyValue" } ],
        "httpMethod": "String",
        "url": "String (identifier)"
    },
    "GetRoleAssignmentConnection": {
        "content": "String",
        "contentType": "String",
        "headers": [ { "@odata.type": "microsoft.graph.KeyValue" } ],
        "httpMethod": "String",
        "url": "String (identifier)"
    },
    "AddRoleAssignmentConnection": {
        "content": "String",
        "contentType": "String",
        "headers": [ { "@odata.type": "microsoft.graph.KeyValue" } ],
        "httpMethod": "String",
        "url": "String (identifier)"
    },
    "RemoveRoleAssignmentConnection": {
        "content": "String",
        "contentType": "String",
        "headers": [ { "@odata.type": "microsoft.graph.KeyValue" } ],
        "httpMethod": "String",
        "url": "String (identifier)"
    }
}
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.provider"
} -->
```http
HTTP/1.1 200 OK
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
  "description": "Update provider",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
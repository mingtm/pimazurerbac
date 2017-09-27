# List resources

Retrieve a list of resource objects.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /providers/<id>/resources
```
### Optional query parameters
This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.

### Request headers
| Name      |Description|
|:----------|:----------|
| Authorization  | Bearer {code}|
| Workbook-Session-Id  | Workbook session Id that determines if changes are persisted or not. Optional.|

### Request body
Do not supply a request body for this method.
### Response
If successful, this method returns a `200 OK` response code and collection of [resource](../resources/resource.md) objects in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_resources"
}-->
```http
GET https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/resources?$orderby=displayName&$filter=((parent/id%20eq%20%279ef79d21-f590-43c7-80e4-3c6d6699b8db%27)%20and%20(resourceType%20ne%20%27subscription%27%20and%20resourceType%20ne%20%27resourcegroup%27))&$expand=parent 
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.resource",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 247

{
  "value": [
	{
	"id":"be2a4b77-c939-4d96-a580-d030b80d3424",
	"originalId":"/subscriptions/ce06ac4b-5d7b-4324-9196-8a4c6d2f7ffd/resourceGroups/Default-Storage-WestUS/providers/Microsoft.ClassicStorage/storageAccounts/2mportalvhdsrq97kcckvfdx",
	"displayName":"2mportalvhdsrq97kcckvfdx",
	"resourceType":"Microsoft.ClassicStorage/storageAccounts",
	"roleDefinitionCount":13,
	"roleAssignmentCount":13
	},
	{
	"id":"3f299d53-17f0-4924-87b4-ccd607a5be3d",
	"originalId":"/subscriptions/ce06ac4b-5d7b-4324-9196-8a4c6d2f7ffd/resourceGroups/Default-ApplicationInsights-CentralUS/providers/microsoft.insights/components/accessreviews.answers.api",
	"displayName":"accessreviews.answers.api",
	"resourceType":"microsoft.insights/components",
	"roleDefinitionCount":11,
	"roleAssignmentCount":13
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List resources",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
# List alerts

Retrieve a list of alert objects.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /providers/<id>/resources('<id>')/alerts
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
If successful, this method returns a `200 OK` response code and collection of [alert](../resources/alert.md) objects in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_alerts"
}-->
```http
GET https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/resources('9ef79d21-f590-43c7-80e4-3c6d6699b8db')/alerts HTTP/1.1
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.alert",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 406

{
  "value": [
    {

      "id": "TooManyOwnersAssignedToResource",
      "resourceId": "9ef79d21-f590-43c7-80e4-3c6d6699b8db",
      "alertName": "Too many owners assigned to a resource",
      "alertDescription": "The number of users with the Owner role is too high. We recommend assigning these individuals to less privileged roles or roles more suitable to their daily needs. Take a moment to review the current assignments, and suggested changes here.",
      "numberOfAffectedItems": 0,
      "additionalData": [
      ],
      "lastModifiedDateTime": "0001-01-01T00:00:00Z",
      "lastScannedDateTime":  "2017-08-30T06:17:00Z",
      "severityLevel": "Medium",
      "alertType": "Vulnerability",
      "securityImpact": "As the number of users with the owner role increases, so does the potential for malicious or mistaken actions affecting your resource.",
      "mitigationSteps": "To mitigate this issue, reduce the number of users in the Owner role. Review the list of users in the list, and reassign them to a less privileged role such as Contributor.",
      "howToPrevent": "Choose a role that provides the fewest privileges necessary for a user or group to complete their tasks.",
      "isDisabled": false,
      "isActive": false,
      "isResolvable": true,
      "isConfigurable": true,
      "status": "Inactive",
      "settings": [
        {
          "key": "ThresholdNumberOfOwners",
          "value": "5"
        },
        {
          "key": "ThresholdPercentageOfOwnersOutOfAllRoleMembers",
          "value": "50"
        }
      ]
    },
    {
      "id": "TooManyPermanentOwnersAssignedToResource",
      "resourceId": "9ef79d21-f590-43c7-80e4-3c6d6699b8db",
      "alertName": "Too many permanent owners assigned to a resource",
      "alertDescription": "The number of users set to never expire is too high. To enhance the security of your resources, we recommend requiring activation for role use. Take a moment to review the list of users, and suggested changes here.",
      "numberOfAffectedItems": 1,
      "additionalData": [
        {
          "item": [
            {
              "key": "id",
              "value": "1c8b3602-77a2-4e8a-8c1e-f127f2af5ca2"
            },
            {
              "key": "assigneeName",
              "value": "MSPIM"
            },
            {
              "key": "assigneeType",
              "value": "ServicePrincipal"
            }
          ]
        },
        {
          "item": [
            {
              "key": "id",
              "value": "b83c177a-10e0-4eeb-8d0b-f3668fbf81fa"
            },
            {
              "key": "assigneeName",
              "value": "Subscription Admins"
            },
            {
              "key": "assigneeType",
              "value": "Group"
            }
          ]
        }
      ],
      "lastModifiedDateTime": "2017-08-30T06:17:03.007Z",
      "lastScannedDateTime": "2017-08-30T06:17:03.007Z",
      "severityLevel": "Medium",
      "alertType": "Vulnerability",
      "securityImpact": "Providing users permanent access in a role may leave resources vulnerable to accidental or malicious activity.",
      "mitigationSteps": "To mitigate this issue, require the user to activate the role before use.",
      "howToPrevent": "Enable \u201cActivation Required\u201d in the role settings menu. This will ensure newly added users must activate their role.",
      "isDisabled": false,
      "isActive": true,
      "isResolvable": true,
      "isConfigurable": true,
      "status": "Active",
      "settings": [
        {
          "key": "ThresholdNumberOfPermanentOwners",
          "value": "1"
        },
        {
          "key": "ThresholdPercentageOfPermanentOwnersOutOfAllOwners",
          "value": "0"
        }
      ]
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List alerts",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
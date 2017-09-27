# List policies

Retrieve a list of policy objects.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /providers/<id>/policies
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
If successful, this method returns a `200 OK` response code and collection of [policy](../resources/policy.md) objects in the response body.
### Example
##### Request
Here is an example of the request to list all the role assignment policies for a given resource.
<!-- {
  "blockType": "request",
  "name": "get_policies"
}-->
```http
GET https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/policies?$expand=resource,roleDefinitions($expand=resource)&$filter=(resource/id+eq+%27bc6f10e6-6dd9-4393-853e-09e13c036b17%27)&$orderby=lastUpdated+desc
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.policy",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 463

{
    "@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#policies",
    "value": [
        {
            "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17_2199084d-1c5c-45ab-bf9c-cddcd6cab633_21d96096-b162-414a-8302-d8354f9d91b2",
            "default": true,
            "lastUpdated": null,
            "lastUpdatedBy": null,
            "adminEligibleSettings": [
                {
                    "ruleIdentifier": "ExpirationRule",
                    "setting": "{\"MaximumGrantPeriod\":\"90.00:00:00\",\"MaximumGrantPeriodInMinutes\":129600,\"PermanentAssignment\":false}"
                },
                {
                    "ruleIdentifier": "MfaRule",
                    "setting": "{\"MfaRequired\":false}"
                }
            ],
            "adminMemberSettings": [
                {
                    "ruleIdentifier": "ExpirationRule",
                    "setting": "{\"MaximumGrantPeriod\":\"30.00:00:00\",\"MaximumGrantPeriodInMinutes\":43200,\"PermanentAssignment\":false}"
                },
                {
                    "ruleIdentifier": "MfaRule",
                    "setting": "{\"MfaRequired\":false}"
                },
                {
                    "ruleIdentifier": "JustificationRule",
                    "setting": "{\"Required\":true}"
                }
            ],
            "userEligibleSettings": [ ],
            "userMemberSettings": [
                {
                    "ruleIdentifier": "ExpirationRule",
                    "setting": "{\"MaximumGrantPeriod\":\"08:00:00\",\"MaximumGrantPeriodInMinutes\":480,\"PermanentAssignment\":false}"
                },
                {
                    "ruleIdentifier": "MfaRule",
                    "setting": "{\"MfaRequired\":false}"
                },
                {
                    "ruleIdentifier": "JustificationRule",
                    "setting": "{\"Required\":true}"
                },
                {
                    "ruleIdentifier": "ActivationDayRule",
                    "setting": "{\"AllowedDaysOfWeek\":[1,2,3,4,5],\"AllowedDays\":[\"Monday\",\"Tuesday\",\"Wednesday\",\"Thursday\",\"Friday\"],\"TimeZoneInfo\":{\"Id\":\"UTC\",\"DisplayName\":\"UTC\",\"StandardName\":\"UTC\",\"DaylightName\":\"UTC\",\"BaseUtcOffset\":\"00:00:00\",\"AdjustmentRules\":null,\"SupportsDaylightSavingTime\":false},\"TimeZoneId\":\"UTC\",\"CustomSetting\":false}"
                },
                {
                    "ruleIdentifier": "ApprovalRule",
                    "setting": "{\"Enabled\":false,\"BusinessFlowId\":\"00000000-0000-0000-0000-000000000000\",\"Approvers\":null}"
                }
            ],
            "resource@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#policies('bc6f10e6-6dd9-4393-853e-09e13c036b17_2199084d-1c5c-45ab-bf9c-cddcd6cab633_21d96096-b162-414a-8302-d8354f9d91b2')/resource/$entity",
            "resource": {
                "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17",
                "originalId": "/subscriptions/b3797212-a671-4ab5-b866-d71fd4159334",
                "displayName": "alpha",
                "resourceType": "subscription",
                "status": "Active",
                "roleDefinitionCount": 0,
                "roleAssignmentCount": 0
            },
            "roleDefinitions@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#policies('bc6f10e6-6dd9-4393-853e-09e13c036b17_2199084d-1c5c-45ab-bf9c-cddcd6cab633_21d96096-b162-414a-8302-d8354f9d91b2')/roleDefinitions",
            "roleDefinitions": [
                {
                    "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17_21d96096-b162-414a-8302-d8354f9d91b2",
                    "templateId": "21d96096-b162-414a-8302-d8354f9d91b2",
                    "displayName": "Azure Service Deploy Release Management Contributor",
                    "subjectCount": 0,
                    "activationRequiredCount": 0,
                    "assignedCount": 0,
                    "ruleSettings": [],
                    "resource@odata.context": "https://api.azrbac.mspim.azure.com/api/v1/$metadata#policies('bc6f10e6-6dd9-4393-853e-09e13c036b17_2199084d-1c5c-45ab-bf9c-cddcd6cab633_21d96096-b162-414a-8302-d8354f9d91b2')/roleDefinitions('bc6f10e6-6dd9-4393-853e-09e13c036b17_21d96096-b162-414a-8302-d8354f9d91b2')/resource/$entity",
                    "resource": {
                        "id": "bc6f10e6-6dd9-4393-853e-09e13c036b17",
                        "originalId": "/subscriptions/b3797212-a671-4ab5-b866-d71fd4159334",
                        "displayName": "alpha",
                        "resourceType": "subscription",
                        "status": "Active",
                        "roleDefinitionCount": 0,
                        "roleAssignmentCount": 0
                    }
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
  "description": "List policies",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
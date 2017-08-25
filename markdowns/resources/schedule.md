# schedule resource type
Represents the schedule for a role assignment request. For a role assignment request, schedule controls when to perform the role assignment operation, when to stop the role assignment, and how frequent to do the role assignment operation for the reoccurring scenario. 



### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|details|String|The details of a schedule. Not used currently.|
|duration|Duration|The duration of a role assignment.|
|isPermanent|Boolean|Indicates if the role assignment is permanent. When **isPermanent** is true, **duration** and **stopDateTime** can be ignored.|
|startDateTime|DateTimeOffset|The start time of the role assignment. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|stopDateTime|DateTimeOffset|The stop time of the role assignment. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`|
|type|String|The role assignment schedule type. The value can be ``Once``, ``Daily``, and ``Weekly``.|

### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.schedule"
}-->

```json
{
  "details": "String",
  "duration": "String (timestamp)",
  "isPermanent": true,
  "startDateTime": "String (timestamp)",
  "stopDateTime": "String (timestamp)",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "schedule resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
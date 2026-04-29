---
title: AWA Manual Assignment API
description: The AWA Manual Assignment API provides an endpoint to manually assign available work items to available Advanced Work Assignment \(AWA\) agents.Assigns an available work item to an available Advanced Work Assignment \(AWA\) agent.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# AWA Manual Assignment API

The AWA Manual Assignment API provides an endpoint to manually assign available work items to available Advanced Work Assignment \(AWA\) agents.

A work item is a single piece of work handled by an AWA agent from start to finish. For example, one chat or one case is an object that can be routed and assigned to agents. For more information, refer to [Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-overview&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

This API requires the Advanced Work Assignment \(com.glide.awa\) plugin. To call this API, you must have either the awa\_manager or awa\_integration\_user role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## AWA Manual Assignment – POST /now/awa/workitems/\{work\_item\_sys\_id\}/assignments

Assigns an available work item to an available Advanced Work Assignment \(AWA\) agent.

The primary use case for this endpoint is to enable external routing systems to route work items. If Advanced Work Assignment is configured to use external routing, work items in the queue are assigned using external routing and not AWA. You can assign the work item task by calling this endpoint. For more information, refer to [Use external routing](https://www.servicenow.com/docs/access?context=awa-external-routing-overview&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

### URL format

Versioned URL: `/now/{api_version}/awa/workitems/{sys_id}/assignments`

Default URL: `/now/awa/workitems/{sys_id}/assignments`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

work\_item\_sys\_id

</td><td>

Sys\_id of the work item to assign to an available agent. The work item must be unassigned and in the **Pending Accept** or **Queued** state. For more information, refer to [Check unassigned task work items](https://www.servicenow.com/docs/access?context=awa-unassigned-task-work-items&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

Data type: String

Table: Work Items \[awa\_work\_item\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

after\_timeout\_presence

</td><td>

Sys\_id of the presence state that the agent switches to if the **timeout** parameter expires.If the **timeout** parameter isn't passed, this parameter is ignored.

For additional information on presence states, see [Configure agent presence states](https://www.servicenow.com/docs/access?context=awa-configure-agent-presence&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

Data type: String

Default: "" \(Empty string\)

Table: AWA Presence State \[awa\_presence\_state\]

</td></tr><tr><td>

agent\_sys\_id

</td><td>

Required. Sys\_id of the available agent to receive the work item. Agents are users with the awa\_agent role.For information on how to determine if an agent is available, refer to [Agent Inbox controls](https://www.servicenow.com/docs/access?context=agent-experience&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

allowed\_to\_decline

</td><td>

Flag that indicates whether agents are allowed to reject work items. If this parameter is `true`, the inbox card displays both the **Accept** and **Reject** buttons on the inbox card.Valid values:

-   true/yes/1: Agent can reject work items.
-   false/no/0: Agent can't reject work items.

Data type: Boolean

Default: true

</td></tr><tr><td>

display\_option

</td><td>

Display option for the card and tab when a work item is automatically assigned. This parameter is only valid if the **enable\_auto\_assign** is passed as `true`.

Valid values:

-   card\_and\_tab: Display both the card and tab.
-   card\_only: Display only the card.

Data type: String

Default: card\_only

</td></tr><tr><td>

enable\_auto\_assign

</td><td>

Flag that indicates whether the work item should be automatically accepted or should allow the agent to manually accept or reject the work item.Valid values:

-   true/yes/1: Automatically accept.
-   false/no/0: Allow agent to manually accept or reject.

Data type: Boolean

Default: false

</td></tr><tr><td>

offered\_on

</td><td>

Work item offer time. The offer time is used to calculate the remaining time the agent has left to accept the work item in the inbox. It helps account for the discrepancy between the time when the API request gets processed, and when the third-party routing system invokes the API request. This parameter allows external systems calling this endpoint to configure the offer time of the work item so that it stays in synchronization with the external system’s internal tracking of the work item.For example, if the work item was offered on 11:30:30, the timeout is 30 seconds, and the current time is 11:30:45, the countdown timer displays 00:15 \(as in 15 seconds remaining\).

This value is stored in the offered\_on field on the work item.

This parameter is ignored if the **timeout** parameter isn't passed.

Data type: String

Format: UTC timestamp \(yyyy-MM-dd'T'HH:mm:ss.SSS\)

</td></tr><tr><td>

timeout

</td><td>

Amount of time that the work item stays in the agent’s inbox waiting for the agent to accept the work assignment.Data type: Number

Unit: Seconds

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|409|Conflict. The request couldn't pass due to an error with the provided work item or agent sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

success

</td><td>

Flag that indicates whether the manual work item assignment is successful.Possible values:

-   true: Work item assignment successful.
-   false: Work item assignment unsuccessful.

Data type: Boolean

</td></tr><tr><td>

message

</td><td>

Response message acknowledging successful assignment or an exception.Success: "Manual assignment successfully requested."

Exceptions:

-   "&lt;work\_item\_sys\_id&gt; is not a valid work item" – Provided work item sys\_id does not exist.
-   "Caller &lt;API\_caller\_sys\_id&gt; does not have the awa\_manager or awa\_integration\_user role" – The authenticated user making the API request must have either the awa\_manager or awa\_integration\_user role.
-   "Work item &lt;work\_item\_sys\_id&gt; cannot be assigned" – Work item provided cannot be assigned because it is in **Accepted** or **Canceled** state. Refer to [Check work items and AWA events](https://www.servicenow.com/docs/access?context=awa-work-items-all&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).
-   "&lt;agent\_sys\_id&gt; is not a valid agent" – Agent does not have the awa\_agent role.
-   "Work Item is already assigned to &lt;agent\_sys\_id&gt;" – Provided work item is assigned to another agent.
-   "Agent is not available" – Agent is not in the **Available** state in AWA. Refer to [Agent Inbox controls](https://www.servicenow.com/docs/access?context=agent-experience&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).
-   "Timeout value cannot be negative" – Provided timeout value cannot be a negative value.
-   "&lt;presence\_state\_sys\_id&gt; is not a valid presence state” – Provided presence state sys\_id doesn't exist in the AWA Presence State \[awa\_presence\_state\] table.
-   "Offered time \(&lt;offered\_on\_timestamp&gt;\) must be in the following format: yyyy-MM-dd'T'HH:mm:ss.SSS" – Provided **offered\_on** timestamp must be in the specified format.
-   "Offered time \(&lt;offered\_on\_timestamp &gt;\) must be before the current time, otherwise agent will have more time to accept the work item" – Provided **offered\_on** timestamp can't be before the time the request is made.
-   "Timestamp after timeout \(&lt;offered\_on\_timestamp &gt;\) must be after the current time, otherwise agent has no time to accept the work item" – The timestamp after adding the timeout value to the provided **offered\_on** timestamp must be after the time the request was made.
-   "&lt;display\_option&gt; is not a valid display option" – Provided display\_option must be either of the following values: "card\_only” or “card\_and\_tab"
-   "%s is not a valid boolean value" – Provided Boolean-type value must be in one of the following Boolean formats: "yes"/"no", "true"/"false", "1"/"0"

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to assign a work item to an available AWA agent using only the required parameters.

```
curl "https://instance.servicenow.com/api/now/awa/workitems/<work_item_sys_id>/assignments" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"agent_sys_id\":\"<agent_sys_id>\"}" \
--user 'username':'password'
```

The result shows that the task has been successfully assigned to the agent. You can verify results in the **Assigned to** field of the Work Items \[awa\_work\_item\] table.

```
{
  "result": {
    "success": true,
    "message": "Manual assignment successfully requested."
  }
}
```

### cURL request

The following example shows how to assign a work item to an available AWA agent including the optional parameters.

```
curl "https://instance.servicenow.com/api/now/awa/workitems/<work_item_sys_id>/assignments" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data '{
    "agent_sys_id": "46d44a23a9fe19810012d100cca80666",
    "timeout":"10",
    "offered_on":"2024-04-03T23:09:31.000"
  }'
--user 'username':'password'
```

The result shows that the task has been successfully assigned to the agent. You can verify results in the **Assigned to** field of the Work Items \[awa\_work\_item\] table.

```
{
  "result": {
    "success": true,
    "message": "Manual assignment successfully requested."
  }
}
```


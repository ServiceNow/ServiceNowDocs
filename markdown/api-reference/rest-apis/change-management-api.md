---
title: Change Management API
description: The Change Management API provides endpoints that enable third-party application integration with the ServiceNow Change Management process.Deletes the change request task identified by the specified sys\_ids.Deletes the change request associated with the specified sys\_id.Cancels the running conflict checking process for the specified change request \(sys\_id\).Deletes the emergency change request identified by the specified sys\_id.Deletes the normal change request identified by the specified sys\_id.Deletes the standard change request identified by the specified sys\_id.Enables retrieving available time slots by configuration item ID and duration, with an option to include planned start time.Retrieves one or more change requests based on the specified criteria.Retrieves a list of available states for the specified change request, including the current state.Enables retrieving the available time slots for a change request.Retrieves one or more tasks associated with a specified change request based on the specified criteria.Retrieves the change request identified by the specified sys\_id.Retrieves multiple configuration items \(CIs\) associated to a specified change request based on the specified association type.Retrieves the status of the currently running change request conflict checking process or the results of the last completed conflict checking process for the specified change request.Retrieves one or more emergency change requests based on the specified criteria.Retrieves the emergency change request identified by the specified sys\_id.Retrieves one or more change models based on the specified criteria.Retrieves the change model identified by the specified sys\_id.Retrieves one or more normal change requests based on the specified criteria.Retrieves the normal change request identified by the specified sys\_id.Retrieves one or more standard change requests based on the specified criteria.Retrieves the standard change request identified by the specified sys\_id.Retrieves one or more standard change templates based on the specified criteria.Retrieves the standard change template identified by the specified sys\_id.Retrieves the current status, information, and errors for the specified asynchronous worker.Updates the change request identified by the specified sys\_id with the key-value pairs in the request body or URL.Allows the current user to approve or reject a change request approval record for the specified change request.Updates the planned start and end times of a change request using the first available time slot found.Updates the change request task identified by the specified sys\_ids with the key-value pairs in the request body or the URL.Updates the emergency change request identified by the specified sys\_id with the key-value pairs in the request body or the URL.Updates the normal change request identified by the specified sys\_id with the parameters in the request body or the URL.Updates the standard change request identified by the specified sys\_id with the parameters in the request body or in the URL.Calculates the risk and impact of the specified standard change based on an evaluation of the risk conditions.Creates a change request record based on the change request. Creating multiple change requests within a single call isn’t supported.Creates the association between a change request and Configuration Management Database \(CMDB\) configuration items \(CI\).Starts a change request conflict checking process for the specified change request \(sys\_id\).Creates one emergency change request based on the default emergency change request record. Multiple emergency change request creations within a single call is not supported.Creates one normal change request based on the default normal change request record. Multiple normal change request creations within a single call is not supported.Populates the impacted services/configuration items \(CIs\) related list based on the primary CI.Creates one standard change request based on an existing standard change template as specified by the passed-in template sys\_id. Multiple standard change request creations within a single call is not supported.Creates one change request task based on the default change request task record and associates it with the specified change request. Multiple change request task creations within a single call is not supported.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 204
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Change Management API

The Change Management API provides endpoints that enable third-party application integration with the ServiceNow Change Management process.

By integrating your application with the ServiceNow Change Management process, all change requests, regardless of where they are initiated, have a single source of truth, providing a single audit source.

Use this REST API to integrate your change management process with external applications and when developing ServiceNow client-side applications.

This REST API enables integrators to:

-   Initiate a standard change request from a published standard change request template.
-   Create a change request of type emergency or normal.
-   Update any field that exists in the change request table for any change request.
-   Update any field that exists in the change task table and work tasks from creation through closure/cancellation.
-   Retrieve a specific change request, standard template, change request task, or change model.
-   Retrieve multiple change requests, standard templates, change request tasks using pagination.
-   Perform risk evaluation.
-   Refresh impacted services.
-   Generate and process any related approval activity associated with a change request.
-   Identify potential scheduling conflicts and identify periods where conflicts do not exist.
-   Delete change requests, change request tasks, and conflict checking processes.
-   Create a change request record based on a change model record.
-   Retrieves a list of available states for the specified change request, including the current state.

The Change Management API supports ITIL types and change models using Workflow Studio and Workflow. Change models deliver fit-for-purpose change. Types and models define transition criteria that must be met before the change request can progress to the next state. You can define this criteria using states, workflows, tools, and business rules.

-   Traditional ITIL types: Standard, Emergency, and Normal.
-   Change model states: New, Scheduled, Implement, Review, and Closed.

You can configure additional change models within your ServiceNow instance and then create change requests based on those change models using endpoints in this API. Use the [Change Management - GET /sn\_chg\_rest/change/model/\{sys\_id\}](change-management-api.md#) and [Change Management - GET /sn\_chg\_rest/change/model](change-management-api.md#) endpoints to obtain the available change models in an instance. Then use the [Change Management - POST /sn\_chg\_rest/change](change-management-api.md#) to create a change request based on a specified change model.

For information on configuring change models, see [Configure Change Management](https://www.servicenow.com/docs/access?context=configure-change-management&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

The following roles are required to access the Change Management endpoints:

-   DELETE: change\_manager or admin
-   GET: change\_manager, itil, sn\_change\_read, or admin
-   PATCH/POST: change\_manager, itil, or admin

In addition, administrators can set change properties to configure Change Management behavior. For a list of these properties and a description of their available functionality, see [Change Management properties](https://www.servicenow.com/docs/access?context=r_ChangeManagementProperties&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Change Management - DELETE /sn\_chg\_rest/change/\{change\_sys\_id\}/task/\{task\_sys\_id\}

Deletes the change request task identified by the specified sys\_ids.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{change_sys_id}/task/{task_sys_id}`

Default URL: `/api/sn_chg_rest/change/{change_sys_id}/task/{task_sys_id}`

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

change\_sys\_id

</td><td>

Sys\_id of the change request to which the task is associated. Verifies that the task is actually associated to the specified change request.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

task\_sys\_id

</td><td>

Sys\_id of the change request task to delete.Data type: String

Table: Change Tasks \[change\_task\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

All fields \(key\) with their associated values for the identified change request task prior to the delete.Data type: Object

</td></tr><tr><td>

parent

</td><td>

Information for the change request to which this task was associated.Data type: Object

```
parent: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

parent.display\_value

</td><td>

Sys\_id of the parent task to display in a UI.Data type: String

</td></tr><tr><td>

parent.value

</td><td>

Sys\_id of the parent task.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id information for the deleted change request.Data type: Object

```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the change request to display in a UI.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the change request.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/0f4ac6c4b750230096c3e4f6ee11a9fe/task/12629ec4b750230096c3e4f6ee11a9d5" \
--request DELETE \
--header "Accept:application/json" \ 
--user "username":"password"
```

```
{
  result: [
    {
      sys_id: {
        value: "12629ec4b750230096c3e4f6ee11a9d5",
        display_value: "12629ec4b750230096c3e4f6ee11a9d5"
      },
      parent: {
        value: "0f4ac6c4b750230096c3e4f6ee11a9fe", 
        display_value: "CHG0033046 "
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Retire both nodes",
        display_value: "Retire both nodes"
      }
    }
  ]
}
```

## Change Management - DELETE /sn\_chg\_rest/change/\{sys\_id\}

Deletes the change request associated with the specified sys\_id.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{sys_id}`

Default URL: `/api/sn_chg_rest/change/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the change request record to delete.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Change request record that was deleted. Each element in this object corresponds to a field in the record of the Change Request \[change\_request\] table.Data type: Object

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/b0dbda5347c12200e0ef563dbb9a718f" \
--request DELETE \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result":
    {
      "reason": {
        "display_value": "",
        "value": ""
      },
      "parent": {
        "display_value": "",
        "value": ""
      },
      "watch_list": {
        "display_value": "",
        "value": ""
       },
       "proposed_change": {
         "display_value": "",
         "value": ""
       },
       "upon_reject": {
         "display_value": "Cancel all future Tasks",
         "value": "cancel"
       },
       "sys_updated_on": {
         "display_value": "2015-07-06 11:59:27",
         "value": "2015-07-06 18:59:27",
         "display_value_internal": "2015-07-06 11:59:27"
      },
      "type": {
        "display_value": "Standard",
        "value": "standard"
      },
      "approval_history": {
        "display_value": "",
        "value": ""
      },
      "skills": {
        "display_value": "",
        "value": ""
      },
      "test_plan": {
        "display_value": "--Confirm that there are no monitoring alerts for the router",
        "value": "--Confirm that there are no monitoring alerts for the router"
      },
      "number": {
        "display_value": "CHG0000024",
        "value": "CHG0000024"
      },
      "is_bulk": {
        "display_value": "false",
        "value": false
      },
      "cab_delegate": {
        "display_value": "",
        "value": ""
      },
      "requested_by_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "ci_class": {
        "display_value": "cmdb_ci",
        "value": "cmdb_ci"
      },
      "state": {
        "display_value": "Closed",
        "value": 3.0
      },
      "sys_created_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "knowledge": {
        "display_value": "false",
        "value": false
      },
      "order": {
        "display_value": "",
        "value": ""
      },
      "phase": {
        "display_value": "Requested",
        "value": "requested"
      },
      "cmdb_ci": {
        "display_value": "",
        "value": ""
      },
      "delivery_plan": {
        "display_value": "",
        "value": ""
      },
      "impact": {
        "display_value": "3 - Low",
        "value": 3.0
      },
      "contract": {
        "display_value": "",
        "value": ""
      },
      "active": {
        "display_value": "false",
        "value": false
      },
      "work_notes_list": {
        "display_value": "",
        "value": ""
      },
      "priority": {
        "display_value": "4 - Low",
        "value": 4.0
      },
      "sys_domain_path": {
        "display_value": "/",
        "value": "/"
      },
      "cab_recommendation": {
        "display_value": "",
        "value": ""
      },
      "production_system": {
        "display_value": "false",
        "value": false
      },
      "rejection_goto": {
        "display_value": "",
        "value": ""
      },
      "review_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "requested_by": {
        "display_value": "System Administrator",
        "value": "6816f79cc0a8016401c5a33be04be441"
      },
      "business_duration": {
        "display_value": "",
        "value": ""
      },
      "group_list": {
        "display_value": "",
        "value": ""
      },
      "change_plan": {
        "display_value": "",
        "value": ""
      },
      "approval_set": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "wf_activity": {
        "display_value": "",
        "value": ""
      },
      "implementation_plan": {
        "display_value": "-- Place router into maintenance mode in the monitoring platform\r\n-- Logon to router through SSH\r\n-- Run the following command\r\n\r\nrouter(config-router)#router bgp 12345\r\nrouter(config-router)#neighbor {neighbor ip} soft-reconfig [inbound]\r\nrouter#clear ip bgp {neighbor ip} soft in\r\n\r\n-- Confirm the sessions have been cleared\r\n-- Place router back into operational mode in the monitoring platform",
        "value": "-- Place router into maintenance mode in the monitoring platform\r\n-- Logon to router through SSH\r\n-- Run the following command\r\n\r\nrouter(config-router)#router bgp 12345\r\nrouter(config-router)#neighbor {neighbor ip} soft-reconfig [inbound]\r\nrouter#clear ip bgp {neighbor ip} soft in\r\n\r\n-- Confirm the sessions have been cleared\r\n-- Place router back into operational mode in the monitoring platform"
      },
      "universal_request": {
        "display_value": "",
        "value": ""
      },
      "end_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "short_description": {
        "display_value": "Reboot the server at 6 am",
        "value": "Reboot the server at 6 am"
      },
      "correlation_display": {
        "display_value": "",
        "value": ""
      },
      "work_start": {
        "display_value": "2015-07-06 11:56:04",
        "value": "2015-07-06 18:56:04",
        "display_value_internal": "2015-07-06 11:56:04"
      },
      "delivery_task": {
        "display_value": "",
        "value": ""
      },
      "outside_maintenance_schedule": {
        "display_value": "false",
        "value": false
      },
      "additional_assignee_list": {
        "display_value": "",
        "value": ""
      },
      "std_change_producer_version": {
        "display_value": "Clear BGP sessions on a Cisco router - 1",
        "value": "16c2273c47010200e90d87e8dee49006"
      },
      "sys_class_name": {
        "display_value": "Change Request",
        "value": "change_request"
      },
      "service_offering": {
        "display_value": "",
        "value": ""
      },
      "closed_by": {
        "display_value": "System Administrator",
        "value": "6816f79cc0a8016401c5a33be04be441"
      },
      "follow_up": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "review_status": {
        "display_value": "",
        "value": ""
      },
      "reassignment_count": {
        "display_value": "2",
        "value": 2.0
      },
      "start_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "assigned_to": {
        "display_value": "",
        "value": ""
      },
      "variables": {
        "display_value": "variable_pool",
        "value": "variable_pool"
      },
      "sla_due": {
        "display_value": "UNKNOWN",
        "value": "",
        "display_value_internal": ""
      },
      "comments_and_work_notes": {
        "display_value": "",
        "value": ""
      },
      "escalation": {
        "display_value": "Normal",
        "value": 0.0
      },
      "upon_approval": {
        "display_value": "Proceed to Next Task",
        "value": "proceed"
      },
      "correlation_id": {
        "display_value": "",
        "value": ""
      },
      "made_sla": {
        "display_value": "true",
        "value": true
      },
      "backout_plan": {
        "display_value": "Due to the limited number of commands in the implementation plan it is not possible to backout the change.\r\n\r\nIf required you are authorized to reboot the router if BGP fails to work",
        "value": "Due to the limited number of commands in the implementation plan it is not possible to backout the change.\r\n\r\nIf required you are authorized to reboot the router if BGP fails to work"
      },
      "conflict_status": {
        "display_value": "Not Run",
        "value": "Not Run"
      },
      "task_effective_number": {
        "display_value": "CHG0000024",
        "value": "CHG0000024"
      },
      "sys_updated_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "opened_by": {
        "display_value": "System Administrator",
        "value": "6816f79cc0a8016401c5a33be04be441"
      },
      "user_input": {
        "display_value": "",
        "value": ""
      },
      "sys_created_on": {
        "display_value": "2015-07-06 11:55:46",
        "value": "2015-07-06 18:55:46",
        "display_value_internal": "2015-07-06 11:55:46"
      },
      "on_hold_task": {
        "display_value": "",
        "value": ""
      },
      "sys_domain": {
        "display_value": "global",
        "value": "global"
      },
      "route_reason": {
        "display_value": "",
        "value": ""
      },
      "closed_at": {
        "display_value": "2015-07-06 11:56:23",
        "value": "2015-07-06 18:56:23",
        "display_value_internal": "2015-07-06 11:56:23"
      },
      "review_comments": {
        "display_value": "",
        "value": ""
      },
      "business_service": {
        "display_value": "",
        "value": ""
      },
      "time_worked": {
        "display_value": "",
        "value": ""
      },
      "chg_model": {
        "display_value": "",
        "value": ""
      },
      "expected_start": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "opened_at": {
        "display_value": "2015-06-09 11:55:46",
        "value": "2015-06-09 18:55:46",
        "display_value_internal": "2015-06-09 11:55:46"
      },
      "work_end": {
        "display_value": "2015-07-06 11:56:10",
        "value": "2015-07-06 18:56:10",
        "display_value_internal": "2015-07-06 11:56:10"
      },
      "phase_state": {
        "display_value": "Open",
        "value": "open"
      },
      "cab_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "work_notes": {
        "display_value": "",
        "value": ""
      },
      "close_code": {
        "display_value": "Successful",
        "value": "successful"
      },
      "assignment_group": {
        "display_value": "Network",
        "value": "287ebd7da9fe198100f92cc8d1d2154e"
      },
      "description": {
        "display_value": "Resend the complete BGP table to neighboring routers\r\n\r\n--Both neighbors need to support soft reset route refresh capability.\r\n--Stores complete BGP table of you neighbor in router memory.\r\n--Not a good idea on a peering router with full feed, due to the memory requirements.\r\n",
        "value": "Resend the complete BGP table to neighboring routers\r\n\r\n--Both neighbors need to support soft reset route refresh capability.\r\n--Stores complete BGP table of you neighbor in router memory.\r\n--Not a good idea on a peering router with full feed, due to the memory requirements.\r\n"
      },
      "on_hold_reason": {
        "display_value": "",
        "value": ""
      },
      "calendar_duration": {
        "display_value": "",
        "value": ""
      },
      "close_notes": {
        "display_value": "Completed without issues",
        "value": "Completed without issues"
      },
      "sys_id": {
        "display_value": "b0dbda5347c12200e0ef563dbb9a718f",
        "value": "b0dbda5347c12200e0ef563dbb9a718f"
      },
      "contact_type": {
        "display_value": "Phone",
        "value": "phone"
      },
      "cab_required": {
        "display_value": "false",
        "value": false
      },
      "urgency": {
        "display_value": "3 - Low",
        "value": 3.0
      },
      "scope": {
        "display_value": "Medium",
        "value": 3.0
      },
      "company": {
        "display_value": "",
        "value": ""
      },
      "justification": {
        "display_value": "",
        "value": ""
      },
      "activity_due": {
        "display_value": "UNKNOWN",
        "value": "",
        "display_value_internal": ""
      },
      "comments": {
        "display_value": "",
        "value": ""
      },
      "approval": {
        "display_value": "Approved",
        "value": "approved"
      },
      "due_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "sys_mod_count": {
        "display_value": "10",
        "value": 10.0
      },
      "on_hold": {
        "display_value": "false",
        "value": false
      },
      "sys_tags": {
        "display_value": "",
        "value": ""
      },
      "conflict_last_run": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "risk_value": {
        "display_value": "",
        "value": ""
      },
      "unauthorized": {
        "display_value": "false",
        "value": false
      },
      "risk": {
        "display_value": "Moderate",
        "value": 3.0
      },
      "location": {
        "display_value": "",
        "value": ""
      },
      "category": {
        "display_value": "Other",
        "value": "Other"
      },
      "risk_impact_analysis": {
        "display_value": "",
        "value": ""
      }
    }
}
```

## Change Management - DELETE /sn\_chg\_rest/change/\{sys\_id\}/conflict

Cancels the running conflict checking process for the specified change request \(sys\_id\).

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{sys_id}/conflict`

Default URL: `/api/sn_chg_rest/change/{sys_id}/conflict`

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

sys\_id

</td><td>

Sys\_id of the change request record for which to cancel the running conflict checking process.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad request. Cancel request failed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

|Name|Description|
|----|-----------|
|None||

### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/0f4ac6c4b750230096c3e4f6ee11a9fe/conflict" \
--request DELETE \
--user "username":"password"

```

```
None
```

## Change Management - DELETE /sn\_chg\_rest/change/emergency/\{sys\_id\}

Deletes the emergency change request identified by the specified sys\_id.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/emergency/{sys_id}`

Default URL: `/api/sn_chg_rest/change/emergency/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the emergency change request to delete.Data type: String

Table: Change Request \[ change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Values for all fields in the associated change request.Data type: Object

</td></tr><tr><td>

state

</td><td>

State of the change request prior to the delete.Data type: Object

```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in the UI.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id information for the change request.Data type: Object

```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the change request to display in a UI.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the change request.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of change request.Data type: Object

```
type: {
  display_value: "String",
  value: "String"
}
```

</td></tr><tr><td>

type.display\_value

</td><td>

Change type to display in a UI.Value is always "Emergency".

Data type: String

</td></tr><tr><td>

type.value

</td><td>

Internal type value.Value is always "emergency".

Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/emergency/b0dbda5347c12200e0ef563dbb9a718f" \
--request DELETE \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  result: [
    {
      sys_id: {
        value: "b0dbda5347c12200e0ef563dbb9a718f", 
        display_value: "b0dbda5347c12200e0ef563dbb9a718f"
      },
      state: {
        value: "-5", 
        display_value: "New"
      },
      type: {
        value: "emergency",
        display_value: "Emergency"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Remove server",
        display_value: "Remove server"
      },
    }, 
  ]
}
```

## Change Management - DELETE /sn\_chg\_rest/change/normal/\{sys\_id\}

Deletes the normal change request identified by the specified sys\_id.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/normal/{sys_id}`

Default URL: `/api/sn_chg_rest/change/normal/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the normal change request to delete.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Values for all fields in the associated change request.Data type: Object

</td></tr><tr><td>

state

</td><td>

State of the change request prior to the delete.Data type: Object

```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in the UI.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the change request.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of change request.Data type: Object

```
type: {
  display_value: "String",
  value: "String"
}
```

</td></tr><tr><td>

type.display\_value

</td><td>

Change type to display in the UI.Value is always "Normal".

Data type: String

</td></tr><tr><td>

type.value

</td><td>

Internal type value.Value is always "normal".

Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/normal/b0dbda5347c12200e0ef563dbb9a718f" \
--request DELETE \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  result: [
    {
      sys_id: "b0dbda5347c12200e0ef563dbb9a718f",
      state: {
        value: "-5", 
        display_value: "New"
      },
      type: {
        value: "normal",
        display_value: "Normal"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Remove server",
        display_value: "Remove server"
      },
    }, 
  ]
}

```

## Change Management - DELETE /sn\_chg\_rest/change/standard/\{sys\_id\}

Deletes the standard change request identified by the specified sys\_id.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/standard/{sys_id}`

Default URL: `/api/sn_chg_rest/change/standard/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the standard change request to delete.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

All fields \(key\) with their associated values for the identified change request.

</td></tr><tr><td>

state

</td><td>

State of the change request prior to the delete.Data type: Object

 ```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in the UI.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Unique identifier of the change request.

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/standard/1c87925347c12200e0ef563dbb9a7177" \
--request DELETE \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  result: [
    {
      sys_id: "1c87925347c12200e0ef563dbb9a7177",
      state: {
        value: "-5", 
        display_value: "New"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Add network switch to cabinet",
        display_value: "Add network switch to cabinet"
      },
    }, 
  ]
}

```

## Change Management - GET /sn\_chg\_rest/change/ci/\{cmdb\_ci\_sys\_id\}/schedule

Enables retrieving available time slots by configuration item ID and duration, with an option to include planned start time.

Role required: sn\_change\_writer.

**Note:** Running this endpoint doesn't list the available start and end times. Use the link provided in the response body **worker.link** property to get the schedule data.

See also:

-   [GET /sn\_chg\_rest/change/\{change\_sys\_id\}/schedule](change-management-api.md#)
-   [PATCH /sn\_chg\_rest/change/\{change\_sys\_id\}/schedule/first\_available](change-management-api.md#)

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/ci/{cmdb_ci_sys_id}/schedule`

Default URL: `/api/sn_chg_rest/change/ci/{cmdb_ci_sys_id}/schedule`

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

cmdb\_ci\_sys\_id

</td><td>

Sys\_id of the configuration item record. This endpoint doesn't require a change request.Data type: String

Table: Configuration Items \[cmdb\_ci\]

</td></tr></tbody>
</table><table id="table_fd4_yhf_jpb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

duration\_in\_seconds

</td><td>

Duration of change in seconds, that is, how much time is required to complete the change request task.Data type: Integer

</td></tr><tr><td>

planned\_start\_time

</td><td>

Optional. Date and time that the change request is planned to start implementation in UTC.Retrieve the available time slot start at or later than this time. If not provided, the system uses the current time as the start time.

Format: yyyy-mm-dd hh:mm:ss

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

202

</td><td>

System accepted the request.

</td></tr><tr><td>

400

</td><td>

Bad Request. A bad request type or malformed request was detected. Possible issues:

-   Can't find the cmdb\_ci with the provided sys\_id. The record either doesn't exist the or the user doesn't have read access to it.
-   The duration\_in\_seconds query parameter value wasn't provided.
-   Invalid duration\_in\_seconds or planned\_start\_time query parameter value provided.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_is2_n4s_jpb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-result-error-cmdb"><td>

error

</td><td>

Information on any errors encountered while processing the endpoint request. Data type: Object

```
"error": {
  "detail": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr id="row-result-error_detail-cmdb"><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr id="row-result-error_message-cmdb"><td>

error.message

</td><td>

Message that identifies the error.Data type: String

</td></tr><tr><td>

messages

</td><td>

Message information.Data type: Object

```
"messages": {
  "errorMessages": [Array],
  "infoMessages": [Array],
  "warningMessages": [Array]
}
```

</td></tr><tr><td>

messages.errorMessages

</td><td>

Error messages encountered while processing the request. Data type: Array

</td></tr><tr><td>

messages.infoMessages

</td><td>

Information messages encountered while processing the request. Data type: Array

</td></tr><tr><td>

messages.warningMessages

</td><td>

Warning messages encountered while processing the request. Data type: Array

</td></tr><tr><td>

request

</td><td>

Original endpoint request.Data type: String

</td></tr><tr><td>

state

</td><td>

Information on the current state of the worker.Data type: Object

```
state: {
  display_value: "String", 
  value: Number
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

Display value of the state of the worker. These values directly correlate to the **state.value** parameter.Possible values:

-   Complete
-   Error
-   In-Progress
-   Waiting

Data type: String

</td></tr><tr><td>

state.value

</td><td>

Numeric value of the state of the worker.Possible values:

-   1
-   2
-   3
-   4

Data type: Number

</td></tr><tr><td>

type

</td><td>

Type of request.Valid value: schedule

Data type: String

</td></tr><tr><td>

worker

</td><td>

Information about the associated worker.Data type: Object

```
"worker": {
  "link": "String",
  "sysId": "String"
}
```

</td></tr><tr><td>

worker.link

</td><td>

Link for retrieving time slot data. Use the sys\_id in [GET /sn\_chg\_rest/change/worker/\{sys\_id\}](change-management-api.md#) to view results.Data type: String

</td></tr><tr><td>

worker.sysId

</td><td>

Sys\_id of the worker associated with the change request.Data type: String

</td></tr><tr><td>

status

</td><td>

Only appears if an error is encountered. Status of the endpoint processing.Possible value: failure

Data type: String

</td></tr></tbody>
</table>### Get available time slots

Use the value provided in the **worker.link** to get schedule window details. The value is in the following format:

`https://instance.service-now.com/api/sn_chg_rest/change/worker/<worker_sys_id>`

Use the worker\_sys\_id in [GET /sn\_chg\_rest/change/worker/\{sys\_id\}](change-management-api.md#) to view results.

The response body contains the status and provides results when processing is complete.

Worker response body parameter results vary depending on time slot availability.

-   If the provided time slot is available for the change request within the schedule time slot, the worker API lists the available time slots in the **payload.spans** property. The **payload.spans** property isn't listed in the results otherwise.
-   If there are no time slots available for change request duration provided within the defined scheduling time slot, the **messages.infoMessages** states the following: `D`

    **Note:** The change request scheduling time slot default value is 90 days. To change this value, modify the **change.conflict.next\_available.schedule\_window** property. For more information, see [Configure conflict analysis properties](https://www.servicenow.com/docs/access?context=configure-conflict-properties&version=australia&pubname=australia-it-service-management&ft:locale=en-US).


The following GET /sn\_chg\_rest/change/worker/\{sys\_id\} example shows output provided using the ID provided in the worker.link detail. The results list open time spans available for the task duration.

```
{
  "result": {
    "worker": {
      "sysId": "d7d1f2b4a444b010f87712198fe9caae",
      "link": "https://instance.service-now.com/api/sn_chg_rest/change/worker/d7d1f2b4a444b010f87712198fe9caae"
    },
    "request": "{\"cmdb_ci_sys_id\":\"82967cdd0ad3370236092104ce988d76\",\"planned_start_time\":\"\",\"duration_in_seconds\":10800,\"timezone\":\"America/Los_Angeles\"}",
    "state": {
      "value": 3,
      "display_value": "Complete"
    },
    "type": "schedule",
    "messages": {
      "errorMessages": [],
      "warningMessages": [],
      "infoMessages": []
    },
    "payload": {
      "spans": [
        {
          "start": {
            "value": "2021-05-15 08:00:00",
            "display_value": "2021-05-15 01:00:00"
          },
          "end": {
            "value": "2021-05-15 11:00:00",
            "display_value": "2021-05-15 04:00:00"
          }
        },
        {
          "start": {
            "value": "2021-05-22 08:00:00",
            "display_value": "2021-05-22 01:00:00"
          },
          "end": {
            "value": "2021-05-22 11:00:00",
            "display_value": "2021-05-22 04:00:00"
          }
        },
        ...
      ]
    }
  }
}
```

### cURL request

```
curl "https://instance.service-now.com/api/sn_chg_rest/change/ci/<cmdb_ci_sys_id>/schedule?duration_in_seconds=10800" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Results include worker.link details you can use to run the provided sys\_id in the GET /sn\_chg\_rest/change/worker/ endpoint.

```
{
  "result": {
    "worker": {
      "sysId": "1049419c1b4c3010f58a6572604bcb7a",
      "link": "https://instance.service-now.com/api/sn_chg_rest/change/worker/1049419c1b4c3010f58a6572604bcb7a"
    },
    "request": "{\"cmdb_ci_sys_id\":\"<cmdb_ci_sys_id>\",\"planned_start_time\":\"\",\"duration_in_seconds\":10800,\"timezone\":\"America/Los_Angeles\"}",
    "state": {
      "value": 1,
      "display_value": "Waiting"
    },
    "type": "schedule",
    "messages": {
      "errorMessages": [],
      "warningMessages": [],
      "infoMessages": []
    }
  }
}
```

## Change Management - GET /sn\_chg\_rest/change

Retrieves one or more change requests based on the specified criteria.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change`

Default URL: `/api/sn_chg_rest/change`

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

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Name-value pairs to use to filter the result set. The name is the field on which the specified value is filtered. This parameter is mutually exclusive with **sysparm\_query**. For example, instead of using `&sysparm_query=active=true`, you can simplify the calling statement by using `&active=true`. You can also use the display value when the field is a choice or reference type field, such as `&state=closed` instead of `&state=7`. To specify multiple key-value pairs, separate each with an ampersand, such as `&active=true&assigned_to=john.smith`. Data type: String

</td></tr><tr><td>

order

</td><td>

Field by which to sort the returned change requests.Data type: String

 Default: *name*

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-entry-RESTAPI">

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td id="sysparm-query-RESTAPI">

[Encoded query](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) used to filter the result set. You can use a UI filter to obtain a properly encoded query.Syntax: `sysparm_query=<col_name><operator><value>`. Column names, operators, and values are case-sensitive.

-   &lt;col\_name&gt;: Name of the table column to filter on.
-   &lt;operator&gt;: Supports the following values:
    -   `=`: &lt;col\_name&gt; exactly matches &lt;value&gt;.
    -   `!=`: &lt;col\_name&gt; does not match &lt;value&gt;.
    -   `LIKE`: &lt;col\_name&gt; contains the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `STARTSWITH`: &lt;col\_name&gt; starts with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `ENDSWITH`: &lt;col\_name&gt; ends with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `^`: AND operator to add an additional query condition. Records included in the result set match both conditions.
    -   `^OR`: OR operator to add an additional query condition. Records included in the result set match at least one of the conditions.
-   &lt;value&gt;: Value to filter on.

For more information about operators, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Queries can contain multiple conditions. For example, the following query returns records where the caller is the current user and the record is active.

`sysparm_query=caller_id=javascript:gs.getUserID()^active=true`

Encoded queries also support order by ascending and descending functionality. To sort responses based on certain fields, use the `ORDERBY` and `ORDERBYDESC` clauses in **sysparm\_query**.

Syntax:

-   `ORDERBY<col_name>`
-   `ORDERBYDESC<col_name>`

For example, the following query gets all active records and orders the results in ascending order by number, and then in descending order by category.

`sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory`

By default, if part of a query is invalid, such as an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. Set the property **glide.invalid\_query.returns\_no\_rows** to `true` to instead return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

</td></tr><tr><td>

textSearch

</td><td>

String to use to search all normal change request record fields. This search uses ServiceNow full text search platform functionality. For more information on ServiceNow search capabilities, see [Search administration](https://www.servicenow.com/docs/access?context=search-administration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).Default: `IR_AND_OR_QUERY`

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

List containing one or more change request record objects. Each object describes a change request. Each element in the change request object corresponds to a field in its associated record in the Change Request \[change\_request\] table.All elements contain value and display\_value name-value pairs. Date fields also contain display\_value\_internal name-value pairs.

Data type: Array

</td></tr><tr><td>

action\_status

</td><td id="action_status-entry-chg_req">

Current action status of the associated change request.Possible values:

-   1: Blocked internally
-   2: Blocked by customer
-   3: Blocked internally and by customer
-   4: Needs attention

Data type: Number

</td></tr><tr><td>

active

</td><td id="active-entry-chg_req">

Flag that indicates whether the change request is active.Possible values:

-   true: Change request is active
-   false: Change request isn't active

Data type: Boolean

Default: true

</td></tr><tr><td>

activity\_due

</td><td id="activity_due-entry-chg_req">

Date and time for which the associated case is expected to be completed.Data type: String

</td></tr><tr><td>

additional\_assignee\_list

</td><td id="add_assignee_list-entry-chg_req">

List of sys\_ids of additional persons assigned to work on the change request.Data type: Array

</td></tr><tr><td>

approval

</td><td id="approval-entry-chg_req">

Type of approval process required.Data type: String

Default: not requested

</td></tr><tr><td>

approval\_history

</td><td id="approval_history-entry-chg_req">

Most recent approval history journal entry.Data type: String

</td></tr><tr><td>

approval\_set

</td><td id="approval_set-entry-chg_req">

Date and time that the associated action was approved.Data type: String

</td></tr><tr><td>

assigned\_to

</td><td id="assigned_to-entry-chg_req">

Sys\_id of the user assigned to the change request.Data type: String

</td></tr><tr><td>

assignment\_group

</td><td id="assign_group-entry-chg_req">

Sys\_id of the group assigned to the change request.Data type: String

</td></tr><tr><td>

backout\_plan

</td><td id="backout_plan-entry-chg_req">

Description of the plan to execute if the change must be reversed.Data type: String

</td></tr><tr><td>

business\_duration

</td><td id="business_dur-entry-chg_req">

Length in scheduled work hours, work days, and work weeks that it took to complete the change.Data type: String

</td></tr><tr><td>

business\_service

</td><td id="business_service-entry-chg_req">

Sys\_id of the business service associated with the change request. Located in the Service \[cmdb\_ci\_service\] table.Data type: String

</td></tr><tr><td>

cab\_date

</td><td id="cab_date-entry-chg_req">

Date on which the Change Advisory Board \(CAB\) meets.Data type: String

</td></tr><tr><td>

cab\_delegate

</td><td id="cab_delegate-entry-chg_req">

Sys\_id of the user that can substitute for the CAB manager during a CAB meeting. Located in the User \[sys\_user\] tableData type: String

</td></tr><tr><td>

cab\_recommendation

</td><td id="cab_rec-entry-chg_req">

Description of the CAB recommendations for the change request.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cab\_required

</td><td id="cab_req-entry-chg_req">

Flag that indicates whether the CAB is required.Possible values:

-   true: Change Advisory Board is required.
-   false: Change Advisory Board isn't required.

Data type: Boolean

Default: false

</td></tr><tr><td>

calendar\_duration

</td><td id="cal_dur-entry-chg_req">

Not currently used by Change Management.Data type: String

</td></tr><tr><td>

category

</td><td id="category-entry-chg_req">

Category of the change, for example hardware, network, or software.Data type: String

Default: Other

</td></tr><tr><td>

change\_plan

</td><td id="change_plan-entry-chg_req">

Activities and roles for managing and controlling the change request.Data type: String

</td></tr><tr><td>

chg\_model

</td><td id="chg_model-entry-chg_req">

Sys\_id of the change model that the associated change request was based on. The Change Model defines the state flow, transitions, and process activities that must be completed for the change request.Data type: String

Table: Change Model \[chg\_model\]

</td></tr><tr><td>

closed\_at

</td><td id="closed_at-entry-chg_req">

Date and time that the associated change request was closed.Data type: String

</td></tr><tr><td>

closed\_by

</td><td id="closed_by-entry-chg_req">

Sys\_id of the person that closed the change request.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

close\_code

</td><td id="close_code-entry-chg_req">

Code assigned to the change request when it was closed. For example, Successful, Successful with issues, and Unsuccessful.Data type: String

</td></tr><tr><td>

close\_notes

</td><td id="close_notes-entry-chg_req">

Notes that the person entered when closing the change request.Data type: String

</td></tr><tr><td>

cmdb\_ci

</td><td id="cmdb_ci-entry-chg_req">

Sys\_id of the configuration item associated with the change request.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr><td>

comments

</td><td id="comments-entry-chg_req">

List of customer-facing work notes entered in the associated change request.Data type: Array

</td></tr><tr><td>

comments\_and\_work\_notes

</td><td id="comments_work_notes-entry-chg_req">

List of both internal and customer-facing work notes entered for the associated change request.Data type: Array

Maximum length: 4,000

</td></tr><tr><td>

company

</td><td id="company-entry-chg_req">

Sys\_id of the company associated with the change request.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

conflict\_last\_run

</td><td id="conflict_last_run-entry-chg_req">

Date and time that the conflict detection script was last run on the change request.Data type: String

</td></tr><tr><td>

conflict\_status

</td><td id="conflict_status-entry-chg_req">

Current conflict status as detected by the conflict detection script, such as Conflict and Not Run.Data type: String

Maximum length: 40

Default: Not Run

</td></tr><tr><td>

contact\_type

</td><td id="contact_type-entry-chg_req">

Method in which the change request was initially requested.Possible values:

-   chat
-   email
-   phone
-   social
-   web

Data type: String

</td></tr><tr><td>

contract

</td><td id="contract-entry-chg_req">

Sys\_id of the contract associated with the change request.Data type: String

Table: Contract \[ast\_contract\]

</td></tr><tr><td>

correlation\_display

</td><td id="corr_display-entry-chg_req">

User-friendly name for the **correlation\_id**.Data type: String

Maximum length: 100

</td></tr><tr><td>

correlation\_id

</td><td id="corr_id-entry-chg_req">

Globally unique ID \(GUID\) of a matching change request record in a third-party system.Data type: String

Maximum length: 100

</td></tr><tr><td>

delivery\_plan

</td><td id="delivery_plan-entry-chg_req">

No longer in use. Sys\_id of the delivery plan associated with the change request.Data type: String

Table: Execution Plan \[sc\_cat\_item\_delivery\_plan\]

</td></tr><tr><td>

delivery\_task

</td><td id="delivery_task-entry-chg_req">

No longer in use. Sys\_id of the delivery task associated with the change request.Data type: String

Table: Execution Plan Task \[sc\_cat\_item\_delivery\_task\]

</td></tr><tr><td>

description

</td><td id="description-entry-chg_req">

Detailed description of the change request.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

due\_date

</td><td>

Task due date. Not used by change request process.Data type: String

</td></tr><tr><td>

end\_date

</td><td id="end_date-entry-chg_req">

Date and time when the change request is to be completed.Data type: String

</td></tr><tr><td>

escalation

</td><td id="escalation-entry-chg_req">

Current escalation level.Possible values:

-   0: Normal
-   1: Moderate
-   2: High
-   3: Overdue

Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

expected\_start

</td><td id="expected_start-entry-chg_req">

Date and time when the task is to start. Not used by the change request process.Data type: String

</td></tr><tr><td>

follow\_up

</td><td id="follow_up-entry-chg_req">

Date and time when a user followed-up with the person requesting the change request.Data type: String

</td></tr><tr><td>

group\_list

</td><td id="group_list-entry-chg_req">

List of sys\_ids and names of the groups associated with the change request.Data type: Array

Maximum length: 4,000

</td></tr><tr><td>

impact

</td><td id="impact-entry-chg_req">

Impact on the change request will have on the customer.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr><td>

implementation\_plan

</td><td id="imp_plan-entry-chg_req">

Sequential steps to execute to implement this change. It also contains any dependencies between steps and assignee details for each step.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

justification

</td><td id="justification-entry-chg_req">

Benefits of implementing this change and the impact if this change is not implemented.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

knowledge

</td><td id="knowledge-entry-chg_req">

Flag that indicates whether there are any knowledge base \(\)KB\) articles associated with the change request.Possible values:

-   true: Associated KB articles
-   false: No associated KB articles

Data type: Boolean

</td></tr><tr><td>

location

</td><td id="location-entry-chg_req">

Sys\_id and name of the location of the equipment referenced in the change request.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

made\_sla

</td><td id="made_sla-entry-chg_req">

No longer used. Flag that indicates whether the change request was implemented in alignment with the associated service level agreement.Data type: Boolean

</td></tr><tr><td>

needs\_attention

</td><td id="needs_attention-entry-chg_req">

Flag that indicates whether the change request needs attention.Possible values:

-   true: Change request needs additional attention.
-   false: Change request doesn't need additional attention.

Data type: Boolean

Default: false

</td></tr><tr><td>

number

</td><td id="number-entry-chg_req">

Change number assigned to the change request by the system, such as CHG0040007.Data type: String

</td></tr><tr><td>

on\_hold

</td><td id="on_hold-entry-chg_req">

Flag that indicates whether the change request is currently on hold.Possible values:

-   true: On hold
-   false: Not on hold

Data type: Boolean

Default: false

</td></tr><tr><td>

on\_hold\_reason

</td><td id="on_hold_reason-entry-chg_req">

If the **on\_hold** parameter is "true", description of the reason why the change request is being held up.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

on\_hold\_task

</td><td id="on_hold_task-entry-chg_req">

If the **on\_hold** parameter is "true", list of the sys\_ids of the tasks that must be completed before the hold is released.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

opened\_at

</td><td id="opened_at-entry-chg_req">

Date and time that the change release was created.Data type: String

</td></tr><tr><td>

opened\_by

</td><td id="opened_by-entry-chg_req">

Sys\_id and name of the user that created the change release.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

order

</td><td id="order-entry-chg_req">

Not used by Change Management. Optional numeric field by which to order records, such as when retrieving them from a database.Data type: Number \(Integer\)

</td></tr><tr><td>

outside\_maintenance\_schedule

</td><td id="outside_maint_sched-entry-chg_req">

Flag that indicates whether maintenance by an outside company has been schedule for the change request.Possible values:

-   true: Outside maintenance scheduled
-   false: No outside maintenance scheduled

Data type: Boolean

Default: false

</td></tr><tr><td>

parent

</td><td id="parent-entry-chg_req">

Sys\_id and name of the parent task to this change request, if any.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

phase

</td><td id="phase-entry-chg_req">

Current phase of the change request. This defines what the change is doing in greater detail.Possible values:

-   accept
-   build
-   plan
-   requested

Data type: String

</td></tr><tr><td>

phase\_state

</td><td id="phase_state-entry-chg_req">

Change\_phase records that should be created for a change. They are dependent on the category, such that each type of change may have different change\_phase records. The change\_phase records provide an opportunity to control the approval process as each change\_phase can have a schedule and a set of approvers.Possible values:

-   complete
-   on hold
-   open
-   rejected
-   requested
-   work in progress

Data type: String

</td></tr><tr><td>

priority

</td><td id="priority-entry-chg_req">

Priority of the change request.Possible values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low

Data type: Number \(Integer\)

Default: 4

</td></tr><tr><td>

production\_system

</td><td id="prod_system-entry-chg_req">

Flag that indicates whether the change request is for a ServiceNow instance that is in a production environment.Possible values:

-   true: Production environment
-   false: Non-production environment

Data type: Boolean

</td></tr><tr><td>

reason

</td><td id="reason-entry-chg_req">

Description of why the change request was initiated.Possible values:

-   Business requirements
-   Hardware upgrade
-   Legislation
-   Location change
-   Network requirements
-   New or removed CI
-   Other
-   Problem resolved
-   Product or service changed
-   Software upgrade
-   User requested

Data type: String

Maximum length: 40

</td></tr><tr><td>

reassignment\_count

</td><td id="reassign_count-entry-chg_req">

Number of times that the change request has been reassigned to a new owner.Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

rejection\_goto

</td><td id="rejection_goto-entry-chg_req">

Sys\_id of the task to perform if the change request is rejected.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

requested\_by

</td><td id="requested_by-entry-chg_req">

Sys\_id of the user that requested the change.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

requested\_by\_date

</td><td id="requested_by_date-entry-chg_req">

Date and time when the change is requested to be implemented by.Data type: String

</td></tr><tr><td>

review\_comments

</td><td id="review_comments-entry-chg_req">

Comments entered when the change request was reviewed.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

review\_date

</td><td id="review_date-entry-chg_req">

Date that the change request was reviewed.Data type: String

</td></tr><tr><td>

review\_status

</td><td id="review_status-entry-chg_req">

Current status of the requested change request review.Data type: String

</td></tr><tr><td>

risk

</td><td id="risk-entry-chg_req">

Level of risk associated with the change request.Valid values:

-   1: High
-   2: Moderate
-   3: Low

Data type: Number

Default: 3

</td></tr><tr><td>

risk\_impact\_analysis

</td><td id="risk_impact_analysis-entry-chg_req">

Description of the risk and analysis of implementing the change request.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

route\_reason

</td><td id="route_reason-entry-chg_req">

Not currently used by Change Management. Reason that the change request was transferred.Possible values:

-   1: Transfer with Resolution
-   9: Transfer without Resolutions

Data type: Number

</td></tr><tr><td>

scope

</td><td id="scope-entry-chg_req">

Size of the change request.Possible values:

-   1: Massive
-   2: Large
-   3: Medium
-   4: Small
-   5: Tiny

Data type: Number

Default: 3

</td></tr><tr><td>

service\_offering

</td><td id="sevice_offering-entry-chg_req">

Sys\_id of the service offering associated with the change request. Service offerings uniquely define the level of service in terms of availability, scope, pricing, and packaging options.Data type: String

Table: Offering \[service\_offering\]

</td></tr><tr><td>

short\_description

</td><td id="short_desc-entry-chg_req">

Description of the change request.Data type: String

Maximum length: 40

</td></tr><tr><td>

skills

</td><td id="skills-entry-chg_req">

List of the sys\_ids of all of the skills required to implement the change request.Data type: Array

Table: Skill \[cmn\_skill\]

</td></tr><tr><td>

sla\_due

</td><td id="sla_due-entry-chg_req">

No longer in use. Date and time that the change request must be completed based on the associated service level agreement.Data type: String

</td></tr><tr><td>

sn\_esign\_document

</td><td>

Sys\_id of any E-signed document attached to the change request.Data type: String

Table: Attachment \[sys\_attachment\]

</td></tr><tr><td>

sn\_esign\_esignature\_configuration

</td><td>

Sys\_id of the E-signed signature template used for the associated document.Data type: String

Table: E-signature Template \[sn\_esign\_configuration\]

</td></tr><tr><td>

start\_date

</td><td id="start_date-entry-chg_req">

Date and time that the change request is planned to start implementation.Data type: String

</td></tr><tr><td>

state

</td><td id="state-entry-chg_req">

Current state of the change request. Possible values are defined in the change model.Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

std\_change\_producer\_version

</td><td id="std_chg_prodversion-entry-chg_req">

Sys\_id of the record producer and change proposal associated with the change request. It also includes the number and percentage of successful and unsuccessful change requests created from the proposal.Data type: String

Table: Standard Change Template Version \[std\_change\_producer\_version\]

</td></tr><tr><td>

sys\_class\_name

</td><td id="sys_class_name-entry-chg_req">

Name of the table in which the change request is located.Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td id="sys_create_by-entry-chg_req">

Name of the user that initially created the change request.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_created\_on

</td><td id="sys_created_on-entry-chg_req">

Date and time that the associated change request record was originally created.Data type: String

</td></tr><tr><td>

sys\_domain

</td><td id="sys_domain-entry-chg_req">

If using domains in the instance, the name of the domain to which the change module record is associated.Data type: String

</td></tr><tr><td>

sys\_domain\_path

</td><td id="sys_domain_path-entry-chg_req">

If using domains in the instance, the domain path in which the associated change module record resides.Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="sys_id-entry-chg_req">

Unique identifier of the associated change request record.Data type: String

</td></tr><tr id="casetable-sys_mod_count-row"><td>

sys\_mod\_count

</td><td id="sys_mod_count-entry-chg_req">

Number of updates to the case since it was initially created.Data type: Number \(Integer\)

</td></tr><tr id="casetable-sys_updated_by-row"><td>

sys\_updated\_by

</td><td id="sys_updated_by-entry-chg_req">

Person that last updated the case.Data type: String

Maximum length: 40

</td></tr><tr id="casetable-sys_updated_on-row"><td>

sys\_updated\_on

</td><td id="sys_updated_on-entry-chg_req">

Date and time when the case was last updated.Data type: String

</td></tr><tr><td>

task\_effective\_number

</td><td id="task_eff_number-entry-chg_req">

Universal request number.Data type: String

Maximum length: 40

</td></tr><tr><td>

task\_for

</td><td id="task_for-entry-chg_req">

Not used by Change Management. Sys\_id of the user that the task was created for.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

test\_plan

</td><td id="test_plan-entry-chg_req">

Description of the associated test plan for the change.Data type: String

Maximum length: 4,000

</td></tr><tr id="casetable-time_worked-row"><td>

time\_worked

</td><td id="time_worked-entry-chg_req">

Total amount of time worked on the change request.Data type: String

</td></tr><tr><td>

type

</td><td id="type-entry-chg_req">

Change request type.Possible values:

-   emergency
-   normal
-   standard

Data type: String

Maximum length: 40

</td></tr><tr><td>

unauthorized

</td><td id="unauthorized-entry-chg_req">

Flag that indicates whether the change request is unauthorizedPossible values:

-   true: Unauthorized
-   false: Authorized

Data type: Boolean

</td></tr><tr><td>

universal\_request

</td><td id="universal_request-entry-chg_req">

Sys\_id of the Parent Universal request to which this change request is a part of.Data type: String

Table: Task \[task\]

</td></tr><tr id="casetable-upon_approval-row"><td>

upon\_approval

</td><td id="upon_approval-entry-chg_req">

Action to take if the change request is approved.Possible values:

-   do\_nothing
-   proceed

Data type: String

Maximum length: 40

Default: proceed

</td></tr><tr id="casetable-upon_reject-row"><td>

upon\_reject

</td><td id="upon_reject-entry-chg_req">

Action to take if the change request is rejected.Possible values:

-   cancel
-   goto

Data type: String

Maximum length: 40

Default: cancel

</td></tr><tr id="casetable-urgency-row"><td>

urgency

</td><td id="urgency-entry-chg_req">

Urgency of the change request.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr id="casetable-user_input-row"><td>

user\_input

</td><td id="user_input-entry-chg_req">

Additional user input.Data type: String

Maximum length: 4,000

</td></tr><tr id="casetable-variables-row"><td>

variables

</td><td id="variables-entry-chg_req">

Name-value pairs of variables associated with the change request.Data type: String

Maximum length: 40

</td></tr><tr id="casetable-watch_list-row"><td>

watch\_list

</td><td id="watch_list-entry-chg_req">

List of sys\_ids of the users who receive notifications about this change request when additional comments are added or if the state of a change request is changed to Resolved or Closed.Data type: Array

Table: User \[sys\_user\]

</td></tr><tr id="casetable-wf_activity-row"><td>

wf\_activity

</td><td id="wf_activity-entry-chg_req">

Sys\_id of the workflow activity record associated with the change request.Data type: String

Table: Workflow Activity \[wf\_activity\]

</td></tr><tr id="casetable-work_end-row"><td>

work\_end

</td><td id="work_end-entry-chg_req">

Date and time work ended on the change request.Data type: String

</td></tr><tr id="casetable-work_notes-row"><td>

work\_notes

</td><td id="work_notes-entry-chg_req">

Information about how to resolve the change request, or steps taken to resolve it.Data type: String

Maximum length: 4,000

</td></tr><tr id="casetable-work_notes_list-row"><td>

work\_notes\_list

</td><td id="work_notes_list-entry-chg_req">

List of sys\_ids of the internal users who receive notifications about this change request when work notes are added. Data type: Array

Table: User \[sys\_user\]

</td></tr><tr id="casetable-work_start-row"><td>

work\_start

</td><td id="work_start-entry-chg_req">

Date and time that work started on the change request.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change?sysparm_query=active=true^ORDERBYnumber" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

For brevity, the results only contain a single change request record.

```
{
  "result": [
    {
      "reason": {
        "display_value": "",
        "value": ""
      },
      "parent": {
        "display_value": "",
        "value": ""
      },
      "watch_list": {
        "display_value": "",
        "value": ""
       },
       "proposed_change": {
         "display_value": "",
         "value": ""
       },
       "upon_reject": {
         "display_value": "Cancel all future Tasks",
         "value": "cancel"
       },
       "sys_updated_on": {
         "display_value": "2015-07-06 11:59:27",
         "value": "2015-07-06 18:59:27",
         "display_value_internal": "2015-07-06 11:59:27"
      },
      "type": {
        "display_value": "Standard",
        "value": "standard"
      },
      "approval_history": {
        "display_value": "",
        "value": ""
      },
      "skills": {
        "display_value": "",
        "value": ""
      },
      "test_plan": {
        "display_value": "--Confirm that there are no monitoring alerts for the router",
        "value": "--Confirm that there are no monitoring alerts for the router"
      },
      "number": {
        "display_value": "CHG0000024",
        "value": "CHG0000024"
      },
      "is_bulk": {
        "display_value": "false",
        "value": false
      },
      "cab_delegate": {
        "display_value": "",
        "value": ""
      },
      "requested_by_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "ci_class": {
        "display_value": "cmdb_ci",
        "value": "cmdb_ci"
      },
      "state": {
        "display_value": "Closed",
        "value": 3.0
      },
      "sys_created_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "knowledge": {
        "display_value": "false",
        "value": false
      },
      "order": {
        "display_value": "",
        "value": ""
      },
      "phase": {
        "display_value": "Requested",
        "value": "requested"
      },
      "cmdb_ci": {
        "display_value": "",
        "value": ""
      },
      "delivery_plan": {
        "display_value": "",
        "value": ""
      },
      "impact": {
        "display_value": "3 - Low",
        "value": 3.0
      },
      "contract": {
        "display_value": "",
        "value": ""
      },
      "active": {
        "display_value": "false",
        "value": false
      },
      "work_notes_list": {
        "display_value": "",
        "value": ""
      },
      "priority": {
        "display_value": "4 - Low",
        "value": 4.0
      },
      "sys_domain_path": {
        "display_value": "/",
        "value": "/"
      },
      "cab_recommendation": {
        "display_value": "",
        "value": ""
      },
      "production_system": {
        "display_value": "false",
        "value": false
      },
      "rejection_goto": {
        "display_value": "",
        "value": ""
      },
      "review_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "requested_by": {
        "display_value": "System Administrator",
        "value": "6816f79cc0a8016401c5a33be04be441"
      },
      "business_duration": {
        "display_value": "",
        "value": ""
      },
      "group_list": {
        "display_value": "",
        "value": ""
      },
      "change_plan": {
        "display_value": "",
        "value": ""
      },
      "approval_set": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "wf_activity": {
        "display_value": "",
        "value": ""
      },
      "implementation_plan": {
        "display_value": "-- Place router into maintenance mode in the monitoring platform\r\n-- Logon to router through SSH\r\n-- Run the following command\r\n\r\nrouter(config-router)#router bgp 12345\r\nrouter(config-router)#neighbor {neighbor ip} soft-reconfig [inbound]\r\nrouter#clear ip bgp {neighbor ip} soft in\r\n\r\n-- Confirm the sessions have been cleared\r\n-- Place router back into operational mode in the monitoring platform",
        "value": "-- Place router into maintenance mode in the monitoring platform\r\n-- Logon to router through SSH\r\n-- Run the following command\r\n\r\nrouter(config-router)#router bgp 12345\r\nrouter(config-router)#neighbor {neighbor ip} soft-reconfig [inbound]\r\nrouter#clear ip bgp {neighbor ip} soft in\r\n\r\n-- Confirm the sessions have been cleared\r\n-- Place router back into operational mode in the monitoring platform"
      },
      "universal_request": {
        "display_value": "",
        "value": ""
      },
      "end_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "short_description": {
        "display_value": "Clear BGP sessions on a Cisco router",
        "value": "Clear BGP sessions on a Cisco router"
      },
      "correlation_display": {
        "display_value": "",
        "value": ""
      },
      "work_start": {
        "display_value": "2015-07-06 11:56:04",
        "value": "2015-07-06 18:56:04",
        "display_value_internal": "2015-07-06 11:56:04"
      },
      "delivery_task": {
        "display_value": "",
        "value": ""
      },
      "outside_maintenance_schedule": {
        "display_value": "false",
        "value": false
      },
      "additional_assignee_list": {
        "display_value": "",
        "value": ""
      },
      "std_change_producer_version": {
        "display_value": "Clear BGP sessions on a Cisco router - 1",
        "value": "16c2273c47010200e90d87e8dee49006"
      },
      "sys_class_name": {
        "display_value": "Change Request",
        "value": "change_request"
      },
      "service_offering": {
        "display_value": "",
        "value": ""
      },
      "closed_by": {
        "display_value": "System Administrator",
        "value": "6816f79cc0a8016401c5a33be04be441"
      },
      "follow_up": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "review_status": {
        "display_value": "",
        "value": ""
      },
      "reassignment_count": {
        "display_value": "2",
        "value": 2.0
      },
      "start_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "assigned_to": {
        "display_value": "",
        "value": ""
      },
      "variables": {
        "display_value": "variable_pool",
        "value": "variable_pool"
      },
      "sla_due": {
        "display_value": "UNKNOWN",
        "value": "",
        "display_value_internal": ""
      },
      "comments_and_work_notes": {
        "display_value": "",
        "value": ""
      },
      "escalation": {
        "display_value": "Normal",
        "value": 0.0
      },
      "upon_approval": {
        "display_value": "Proceed to Next Task",
        "value": "proceed"
      },
      "correlation_id": {
        "display_value": "",
        "value": ""
      },
      "made_sla": {
        "display_value": "true",
        "value": true
      },
      "backout_plan": {
        "display_value": "Due to the limited number of commands in the implementation plan it is not possible to backout the change.\r\n\r\nIf required you are authorized to reboot the router if BGP fails to work",
        "value": "Due to the limited number of commands in the implementation plan it is not possible to backout the change.\r\n\r\nIf required you are authorized to reboot the router if BGP fails to work"
      },
      "conflict_status": {
        "display_value": "Not Run",
        "value": "Not Run"
      },
      "task_effective_number": {
        "display_value": "CHG0000024",
        "value": "CHG0000024"
      },
      "sys_updated_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "opened_by": {
        "display_value": "System Administrator",
        "value": "6816f79cc0a8016401c5a33be04be441"
      },
      "user_input": {
        "display_value": "",
        "value": ""
      },
      "sys_created_on": {
        "display_value": "2015-07-06 11:55:46",
        "value": "2015-07-06 18:55:46",
        "display_value_internal": "2015-07-06 11:55:46"
      },
      "on_hold_task": {
        "display_value": "",
        "value": ""
      },
      "sys_domain": {
        "display_value": "global",
        "value": "global"
      },
      "route_reason": {
        "display_value": "",
        "value": ""
      },
      "closed_at": {
        "display_value": "2015-07-06 11:56:23",
        "value": "2015-07-06 18:56:23",
        "display_value_internal": "2015-07-06 11:56:23"
      },
      "review_comments": {
        "display_value": "",
        "value": ""
      },
      "business_service": {
        "display_value": "",
        "value": ""
      },
      "time_worked": {
        "display_value": "",
        "value": ""
      },
      "chg_model": {
        "display_value": "",
        "value": ""
      },
      "expected_start": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "opened_at": {
        "display_value": "2015-06-09 11:55:46",
        "value": "2015-06-09 18:55:46",
        "display_value_internal": "2015-06-09 11:55:46"
      },
      "work_end": {
        "display_value": "2015-07-06 11:56:10",
        "value": "2015-07-06 18:56:10",
        "display_value_internal": "2015-07-06 11:56:10"
      },
      "phase_state": {
        "display_value": "Open",
        "value": "open"
      },
      "cab_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "work_notes": {
        "display_value": "",
        "value": ""
      },
      "close_code": {
        "display_value": "Successful",
        "value": "successful"
      },
      "assignment_group": {
        "display_value": "Network",
        "value": "287ebd7da9fe198100f92cc8d1d2154e"
      },
      "description": {
        "display_value": "Resend the complete BGP table to neighboring routers\r\n\r\n--Both neighbors need to support soft reset route refresh capability.\r\n--Stores complete BGP table of you neighbor in router memory.\r\n--Not a good idea on a peering router with full feed, due to the memory requirements.\r\n",
        "value": "Resend the complete BGP table to neighboring routers\r\n\r\n--Both neighbors need to support soft reset route refresh capability.\r\n--Stores complete BGP table of you neighbor in router memory.\r\n--Not a good idea on a peering router with full feed, due to the memory requirements.\r\n"
      },
      "on_hold_reason": {
        "display_value": "",
        "value": ""
      },
      "calendar_duration": {
        "display_value": "",
        "value": ""
      },
      "close_notes": {
        "display_value": "Completed without issues",
        "value": "Completed without issues"
      },
      "sys_id": {
        "display_value": "1766f1de47410200e90d87e8dee490f6",
        "value": "1766f1de47410200e90d87e8dee490f6"
      },
      "contact_type": {
        "display_value": "Phone",
        "value": "phone"
      },
      "cab_required": {
        "display_value": "false",
        "value": false
      },
      "urgency": {
        "display_value": "3 - Low",
        "value": 3.0
      },
      "scope": {
        "display_value": "Medium",
        "value": 3.0
      },
      "company": {
        "display_value": "",
        "value": ""
      },
      "justification": {
        "display_value": "",
        "value": ""
      },
      "activity_due": {
        "display_value": "UNKNOWN",
        "value": "",
        "display_value_internal": ""
      },
      "comments": {
        "display_value": "",
        "value": ""
      },
      "approval": {
        "display_value": "Approved",
        "value": "approved"
      },
      "due_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "sys_mod_count": {
        "display_value": "10",
        "value": 10.0
      },
      "on_hold": {
        "display_value": "false",
        "value": false
      },
      "sys_tags": {
        "display_value": "",
        "value": ""
      },
      "conflict_last_run": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "risk_value": {
        "display_value": "",
        "value": ""
      },
      "unauthorized": {
        "display_value": "false",
        "value": false
      },
      "risk": {
        "display_value": "Moderate",
        "value": 3.0
      },
      "location": {
        "display_value": "",
        "value": ""
      },
      "category": {
        "display_value": "Other",
        "value": "Other"
      },
      "risk_impact_analysis": {
        "display_value": "",
        "value": ""
      }
    }
  ]
}
```

## Change Management - GET /sn\_chg\_rest/change/\{change\_sys\_id\}/nextstates

Retrieves a list of available states for the specified change request, including the current state.

If available, it also provides how to transition to the next state based on the version of the implemented Change Management. If the changes are change model driven, the endpoint returns conditions which have passed or not. It also provides information on whether all conditions have passed for a given transition. This information is not available for type driven and legacy change requests.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{change_sys_id}/nextstates`

Default URL: `/api/sn_chg_rest/change/{change_sys_id}/nextstates`

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

change\_sys\_id

</td><td>

Sys\_id of the change request. Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

available\_states

</td><td>

Values for the states that are available for the specified change request, including the current state.Data type: Array

</td></tr><tr><td>

state\_label

</td><td>

Key-value pairs that associate labels with the available states.Data type: Object

</td></tr><tr><td>

state\_transitions

</td><td>

Information on what is required to transition to each available state. Each distinct available "to state" is in its own Array with each differing set of conditions for that to state being in its own Object.Data type: Array

 ```
"state_transitions": [
  {
    "automatic_transition": Boolean,
    "conditions": [Array],
    "display_value": "String",
    "from_state": "String",
    "sys_id": "String",
    "to_state": "String",
    "transition_available": Boolean
  }
]
```

</td></tr><tr><td>

state\_transitions.automatic\_transition

</td><td>

Flag that indicates whether to automatically transition to this state.

 Valid values:

-   true: Change request automatically transitions to this state.
-   false: Change request does not automatically transition to this state.

 Data type: Boolean

</td></tr><tr><td>

state\_transitions.conditions

</td><td>

List of the conditions associated with the state.Data type: Array of Objects

 ```
"conditions": [
  {
    "condition": {Object},
    "passed": Boolean
  }
]
```

</td></tr><tr><td>

state\_transitions.conditions.condition

</td><td>

Values of a specific condition.Data type: Object

 ```
"condition": {
  "description": "String",
  "name": "String",
  "sys_id": "String"
}
```

</td></tr><tr><td>

state\_transitions.conditions.condition.description

</td><td>

Description of the condition.Data type: String

</td></tr><tr><td>

state\_transitions.conditions.condition.name

</td><td>

Name of the condition.Data type: String

</td></tr><tr><td>

state\_transitions.conditions.condition.sys\_id

</td><td>

Sys\_id of the condition.Data type: String

</td></tr><tr><td>

state\_transitions.conditions.passed

</td><td>

Flag that indicates whether the change request met the associated condition.

 Valid values:

-   true: Met the condition.
-   false: Did not meet the condition.

</td></tr><tr><td>

state\_transitions.display\_value

</td><td>

Displayed description of the state.Data type: String

</td></tr><tr><td>

state\_transitions.from\_state

</td><td>

Value of the state that the change request is transitioning from.Data type: String

</td></tr><tr><td>

state\_transitions.sys\_id

</td><td>

Sys\_id of the transition state.Data type: String

</td></tr><tr><td>

state\_transitions.to\_state

</td><td>

Value of the state that the change request is transitioning to.Data type: String

</td></tr><tr><td>

state\_transitions.transition\_available

</td><td>

Flag that indicates whether the change request can transition from its current state to this state.

 Valid values:

-   true: Can transition to this state.
-   false: Cannot transition to this state.

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint.

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/b0dbda5347c12200e0ef563dbb9a718f"/nextstates \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

Return results:

```
{
  "result": {
    "available_states": [ "0", "4", "-1" ], // State values
    "state_transitions": [
      [
        {
          "sys_id": "7a0d2ccdc343101035ae3f52c1d3ae2e", // sttrm_state_transition sys id
          "display_value": "Implement to Review",
          "from_state": "-1",
          "to_state": "0",
          "transition_available": false, // If true, can move to this state
          "automatic_transition": true, // If true, automatically moves to this state
          "conditions": [
            {
              "passed": false, // If true, change request met this condition
              "condition": {
                "name": "No active Change Tasks",
                "description": null,
                "sys_id": "3c1d2ccdc343101035ae3f52c1d3aea4"
              }
            }
          ]
        },
        {
          "sys_id": "db401481c343101035ae3f52c1d3aedd",
          "display_value": "Implement to Review",
          "from_state": "-1",
          "to_state": "0",
          "transition_available": true,
          "automatic_transition": false,
          "conditions": [
            {
              "passed": true,
              "condition": {
                "name": "Not On hold",
                "description": null,
                "sys_id": "2132deb6c303101035ae3f52c1d3ae8c"
              }
            }
          ]
        }
      ],
      [
        {
          "sys_id": "5327c551c343101035ae3f52c1d3aeec",
          "display_value": "Implement to Canceled",
          "from_state": "-1",
          "to_state": "4",
          "transition_available": true,
          "automatic_transition": false,
          "conditions": []
        }
      ]
    ],
    "state_label": { // state value to label pairs
      "0": "Review",
      "4": "Canceled",
      "-1": "Implement"
    }
  }
}
```

## Change Management - GET /sn\_chg\_rest/change/\{change\_sys\_id\}/schedule

Enables retrieving the available time slots for a change request.

Role required: sn\_change\_writer.

**Note:** Running this endpoint doesn't list the available start and end times. Use the link provided in the response body **worker.link** property to get the schedule data.

See also:

-   [GET /sn\_chg\_rest/change/ci/\{cmdb\_ci\_sys\_id\}/schedule](change-management-api.md#)
-   [PATCH /sn\_chg\_rest/change/\{change\_sys\_id\}/schedule/first\_available](change-management-api.md#)

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{change_sys_id}/schedule`

Default URL: `/api/sn_chg_rest/change/{change_sys_id}/schedule`

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

change\_sys\_id

</td><td>

Sys\_id of the change request on which to find the next available time slot.The selected change request must have a configuration item \(cmdb\_ci\) with planned start and planned end times.

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

202

</td><td>

System accepted the request.

</td></tr><tr><td>

400

</td><td>

Bad Request. A bad request type or malformed request was detected. Possible issues:

-   The specified change request is missing the planned start and end times.
-   The specified change request doesn't have an associated configuration item \(cmdb\_ci\).
-   User doesn't have read access to the fields of the change request.

</td></tr><tr><td>

404

</td><td>

Not Found. The specified record couldn't be found. Possible issues:

-   System can't find the change request based on information provided.
-   User doesn't have read access to the record.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_is2_n4s_jpb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-result-error-cmdb"><td>

error

</td><td>

Information on any errors encountered while processing the endpoint request. Data type: Object

 ```
"error": {
  "detail": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr id="row-result-error_detail-cmdb"><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr id="row-result-error_message-cmdb"><td>

error.message

</td><td>

Message that identifies the error.Data type: String

</td></tr><tr><td>

messages

</td><td>

Message information.Data type: Object

```
"messages": {
  "errorMessages": [Array],
  "infoMessages": [Array],
  "warningMessages": [Array]
}
```

</td></tr><tr><td>

messages.errorMessages

</td><td>

Error messages encountered while processing the request. Data type: Array

</td></tr><tr><td>

messages.infoMessages

</td><td>

Information messages encountered while processing the request. Data type: Array

</td></tr><tr><td>

messages.warningMessages

</td><td>

Warning messages encountered while processing the request. Data type: Array

</td></tr><tr><td>

request

</td><td>

Original endpoint request.Data type: String

</td></tr><tr><td>

state

</td><td>

Information on the current state of the worker.Data type: Object

```
state: {
  display_value: "String", 
  value: Number
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

Display value of the state of the worker. These values directly correlate to the **state.value** parameter.Possible values:

-   Complete
-   Error
-   In-Progress
-   Waiting

Data type: String

</td></tr><tr><td>

state.value

</td><td>

Numeric value of the state of the worker.Possible values:

-   1
-   2
-   3
-   4

Data type: Number

</td></tr><tr><td>

type

</td><td>

Type of request.Valid value: schedule

Data type: String

</td></tr><tr><td>

worker

</td><td>

Information about the associated worker.Data type: Object

```
"worker": {
  "link": "String",
  "sysId": "String"
}
```

</td></tr><tr><td>

worker.link

</td><td>

Link for retrieving time slot data. Use the sys\_id in [GET /sn\_chg\_rest/change/worker/\{sys\_id\}](change-management-api.md#) to view results.Data type: String

</td></tr><tr><td>

worker.sysId

</td><td>

Sys\_id of the worker associated with the change request.Data type: String

</td></tr><tr><td>

status

</td><td>

Only appears if an error is encountered. Status of the endpoint processing.Possible value: failure

Data type: String

</td></tr></tbody>
</table>### Get available time slots

Use the value provided in the **worker.link** to get schedule window details. The value is in the following format:

`https://instance.service-now.com/api/sn_chg_rest/change/worker/<worker_sys_id>`

Use the worker\_sys\_id in [GET /sn\_chg\_rest/change/worker/\{worker\_sys\_id\}](change-management-api.md#) to view results.

The response body contains the status and provides results when processing is complete.

Worker response body parameter results vary depending on time slot availability.

-   If the provided time slot is available for the change request within the schedule time slot, the worker API lists the available time slots in the **payload.spans** property. The **payload.spans** property isn't listed in the results otherwise.
-   If there are no time slots available for change request duration provided within the defined scheduling time slot, the **messages.infoMessages** states the following: `D`

    **Note:** The change request scheduling time slot default value is 90 days. To change this value, modify the **change.conflict.next\_available.schedule\_window** property. For more information, see [Configure conflict analysis properties](https://www.servicenow.com/docs/access?context=configure-conflict-properties&version=australia&pubname=australia-it-service-management&ft:locale=en-US).


The following GET /sn\_chg\_rest/change/worker/\{sys\_id\} example shows output provided using the ID provided in the worker.link detail. The results list open time spans available for the task duration.

```
{
  "result": {
    "worker": {
      "sysId": "9b3f62e0a4c87010f87712198fe9cad1",
      "link": "https://instance.service-now.com/api/sn_chg_rest/change/worker/9b3f62e0a4c87010f87712198fe9cad1"
    },
    "request": "{\"change_sys_id\":\"87ae5e900a0a2c3e263e8304e727c646\",\"timezone\":\"America/Los_Angeles\"}",
    "state": {
      "value": 3,
      "display_value": "Complete"
    },
    "type": "schedule",
    "messages": {
      "errorMessages": [],
      "warningMessages": [],
      "infoMessages": []
    },
    "payload": {
      "spans": [
        {
          "start": {
            "value": "2021-05-08 08:00:00",
            "display_value": "2021-05-08 01:00:00"
          },
          "end": {
            "value": "2021-05-08 11:00:00",
            "display_value": "2021-05-08 04:00:00"
          }
        },
        {
          "start": {
            "value": "2021-05-15 08:00:00",
            "display_value": "2021-05-15 01:00:00"
          },
          "end": {
            "value": "2021-05-15 11:00:00",
            "display_value": "2021-05-15 04:00:00"
          }
        },
        ...
      ]
    }
  }
}
```

### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/change/{change_sys_id}/schedule" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

Results include worker.link details you can use to run the provided sys\_id in the GET /sn\_chg\_rest/change/worker/ endpoint.

```
{
  "result": {
    "worker": {
      "sysId": "9b3f62e0a4c87010f87712198fe9cad1",
      "link": "https://instance.service-now.com/api/sn_chg_rest/change/worker/9b3f62e0a4c87010f87712198fe9cad1"
    },
    "request": "{\"change_sys_id\":\"87ae5e900a0a2c3e263e8304e727c646\",\"timezone\":\"America/Los_Angeles\"}",
    "state": {
      "value": 1,
      "display_value": "Waiting"
    },
    "type": "schedule",
    "messages": {
      "errorMessages": [],
      "warningMessages": [],
      "infoMessages": []
    }
  }
}
```

## Change Management - GET /sn\_chg\_rest/change/\{change\_sys\_id\}/task

Retrieves one or more tasks associated with a specified change request based on the specified criteria.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{change_sys_id}/task`

Default URL: `/api/sn_chg_rest/change/{change_sys_id}/task`

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

change\_sys\_id

</td><td>

Sys\_id of the change request whose tasks are to be retrieved.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table><table id="table_tnj_bxm_ylb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

key-value pairs

</td><td>

Fields to modify when creating the request. The key is the field name within the template and the value is the information to populate in the field. Fields that cannot be modified and are ignored if passed in:

-   Business rules
-   Read-only fields as defined in ACLs
-   Fields that do not exist

Data type: String

</td></tr><tr><td>

order

</td><td>

Field by which to sort the returned change requests. Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. Data type: Number

Default: 500

</td></tr><tr><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td>

[Encoded query](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) used to filter the result set. You can use a UI filter to obtain a properly encoded query.Syntax: `sysparm_query=<col_name><operator><value>`. Column names, operators, and values are case-sensitive.

-   &lt;col\_name&gt;: Name of the table column to filter on.
-   &lt;operator&gt;: Supports the following values:
    -   `=`: &lt;col\_name&gt; exactly matches &lt;value&gt;.
    -   `!=`: &lt;col\_name&gt; does not match &lt;value&gt;.
    -   `LIKE`: &lt;col\_name&gt; contains the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `STARTSWITH`: &lt;col\_name&gt; starts with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `ENDSWITH`: &lt;col\_name&gt; ends with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `^`: AND operator to add an additional query condition. Records included in the result set match both conditions.
    -   `^OR`: OR operator to add an additional query condition. Records included in the result set match at least one of the conditions.
-   &lt;value&gt;: Value to filter on.

For more information about operators, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Queries can contain multiple conditions. For example, the following query returns records where the caller is the current user and the record is active.

`sysparm_query=caller_id=javascript:gs.getUserID()^active=true`

Encoded queries also support order by ascending and descending functionality. To sort responses based on certain fields, use the `ORDERBY` and `ORDERBYDESC` clauses in **sysparm\_query**.

Syntax:

-   `ORDERBY<col_name>`
-   `ORDERBYDESC<col_name>`

For example, the following query gets all active records and orders the results in ascending order by number, and then in descending order by category.

`sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory`

By default, if part of a query is invalid, such as an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. Set the property **glide.invalid\_query.returns\_no\_rows** to `true` to instead return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

</td></tr><tr><td>

textSearch

</td><td>

String to use to search all change task record fields. This search uses ServiceNow full text search platform functionality and defaults to `IR_AND_OR_QUERY`.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

All fields \(key\) with their associated values for the identified change request task prior to the delete.Data type: Object

</td></tr><tr><td>

parent

</td><td>

Information for the change request associated to the task.Data type: Object

```
parent: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

parent.display\_value

</td><td>

Change request information to display in a UI.Data type: String

</td></tr><tr><td>

parent.value

</td><td>

Sys\_id of the change request associated to the task.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id information for the change request task.Data type: Object

```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the change request task to display in a UI.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the change request task.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/0f4ac6c4b750230096c3e4f6ee11a9fe/task?sysparm_query=active=true^ORDERBYnumber" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'

```

```
{
    result: [
        {
            sys_id: {
                value: "12629ec4b750230096c3e4f6ee11a9d5",
                display_value: "12629ec4b750230096c3e4f6ee11a9d5"
            },
            parent: {
                value: "0f4ac6c4b750230096c3e4f6ee11a9fe ", 
                display_value: "CHG0033046 "
            },
            ..., // all valid fields in record, example below
            short_description: {
                value: "Retire node",
                display_value: "Retire node"
            }
        }, 
        { // next record found }, ... // and so on
    ]
}

```

## Change Management - GET /sn\_chg\_rest/change/\{sys\_id\}

Retrieves the change request identified by the specified sys\_id.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{sys_id}`

Default URL: `/api/sn_chg_rest/change/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the change request record.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

List containing one or more change request record objects. Each object describes a change request. Each element in the change request object corresponds to a field in its associated record in the Change Request \[change\_request\] table.All elements contain value and display\_value name-value pairs. Date fields also contain display\_value\_internal name-value pairs.

Data type: Array

</td></tr><tr><td>

action\_status

</td><td id="action_status-entry-chg_req">

Current action status of the associated change request.Possible values:

-   1: Blocked internally
-   2: Blocked by customer
-   3: Blocked internally and by customer
-   4: Needs attention

Data type: Number

</td></tr><tr><td>

active

</td><td id="active-entry-chg_req">

Flag that indicates whether the change request is active.Possible values:

-   true: Change request is active
-   false: Change request isn't active

Data type: Boolean

Default: true

</td></tr><tr><td>

activity\_due

</td><td id="activity_due-entry-chg_req">

Date and time for which the associated case is expected to be completed.Data type: String

</td></tr><tr><td>

additional\_assignee\_list

</td><td id="add_assignee_list-entry-chg_req">

List of sys\_ids of additional persons assigned to work on the change request.Data type: Array

</td></tr><tr><td>

approval

</td><td id="approval-entry-chg_req">

Type of approval process required.Data type: String

Default: not requested

</td></tr><tr><td>

approval\_history

</td><td id="approval_history-entry-chg_req">

Most recent approval history journal entry.Data type: String

</td></tr><tr><td>

approval\_set

</td><td id="approval_set-entry-chg_req">

Date and time that the associated action was approved.Data type: String

</td></tr><tr><td>

assigned\_to

</td><td id="assigned_to-entry-chg_req">

Sys\_id of the user assigned to the change request.Data type: String

</td></tr><tr><td>

assignment\_group

</td><td id="assign_group-entry-chg_req">

Sys\_id of the group assigned to the change request.Data type: String

</td></tr><tr><td>

backout\_plan

</td><td id="backout_plan-entry-chg_req">

Description of the plan to execute if the change must be reversed.Data type: String

</td></tr><tr><td>

business\_duration

</td><td id="business_dur-entry-chg_req">

Length in scheduled work hours, work days, and work weeks that it took to complete the change.Data type: String

</td></tr><tr><td>

business\_service

</td><td id="business_service-entry-chg_req">

Sys\_id of the business service associated with the change request. Located in the Service \[cmdb\_ci\_service\] table.Data type: String

</td></tr><tr><td>

cab\_date

</td><td id="cab_date-entry-chg_req">

Date on which the Change Advisory Board \(CAB\) meets.Data type: String

</td></tr><tr><td>

cab\_delegate

</td><td id="cab_delegate-entry-chg_req">

Sys\_id of the user that can substitute for the CAB manager during a CAB meeting. Located in the User \[sys\_user\] tableData type: String

</td></tr><tr><td>

cab\_recommendation

</td><td id="cab_rec-entry-chg_req">

Description of the CAB recommendations for the change request.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

cab\_required

</td><td id="cab_req-entry-chg_req">

Flag that indicates whether the CAB is required.Possible values:

-   true: Change Advisory Board is required.
-   false: Change Advisory Board isn't required.

Data type: Boolean

Default: false

</td></tr><tr><td>

calendar\_duration

</td><td id="cal_dur-entry-chg_req">

Not currently used by Change Management.Data type: String

</td></tr><tr><td>

category

</td><td id="category-entry-chg_req">

Category of the change, for example hardware, network, or software.Data type: String

Default: Other

</td></tr><tr><td>

change\_plan

</td><td id="change_plan-entry-chg_req">

Activities and roles for managing and controlling the change request.Data type: String

</td></tr><tr><td>

chg\_model

</td><td id="chg_model-entry-chg_req">

Sys\_id of the change model that the associated change request was based on. The Change Model defines the state flow, transitions, and process activities that must be completed for the change request.Data type: String

Table: Change Model \[chg\_model\]

</td></tr><tr><td>

closed\_at

</td><td id="closed_at-entry-chg_req">

Date and time that the associated change request was closed.Data type: String

</td></tr><tr><td>

closed\_by

</td><td id="closed_by-entry-chg_req">

Sys\_id of the person that closed the change request.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

close\_code

</td><td id="close_code-entry-chg_req">

Code assigned to the change request when it was closed. For example, Successful, Successful with issues, and Unsuccessful.Data type: String

</td></tr><tr><td>

close\_notes

</td><td id="close_notes-entry-chg_req">

Notes that the person entered when closing the change request.Data type: String

</td></tr><tr><td>

cmdb\_ci

</td><td id="cmdb_ci-entry-chg_req">

Sys\_id of the configuration item associated with the change request.Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr><td>

comments

</td><td id="comments-entry-chg_req">

List of customer-facing work notes entered in the associated change request.Data type: Array

</td></tr><tr><td>

comments\_and\_work\_notes

</td><td id="comments_work_notes-entry-chg_req">

List of both internal and customer-facing work notes entered for the associated change request.Data type: Array

Maximum length: 4,000

</td></tr><tr><td>

company

</td><td id="company-entry-chg_req">

Sys\_id of the company associated with the change request.Data type: String

Table: Company \[core\_company\]

</td></tr><tr><td>

conflict\_last\_run

</td><td id="conflict_last_run-entry-chg_req">

Date and time that the conflict detection script was last run on the change request.Data type: String

</td></tr><tr><td>

conflict\_status

</td><td id="conflict_status-entry-chg_req">

Current conflict status as detected by the conflict detection script, such as Conflict and Not Run.Data type: String

Maximum length: 40

Default: Not Run

</td></tr><tr><td>

contact\_type

</td><td id="contact_type-entry-chg_req">

Method in which the change request was initially requested.Possible values:

-   chat
-   email
-   phone
-   social
-   web

Data type: String

</td></tr><tr><td>

contract

</td><td id="contract-entry-chg_req">

Sys\_id of the contract associated with the change request.Data type: String

Table: Contract \[ast\_contract\]

</td></tr><tr><td>

correlation\_display

</td><td id="corr_display-entry-chg_req">

User-friendly name for the **correlation\_id**.Data type: String

Maximum length: 100

</td></tr><tr><td>

correlation\_id

</td><td id="corr_id-entry-chg_req">

Globally unique ID \(GUID\) of a matching change request record in a third-party system.Data type: String

Maximum length: 100

</td></tr><tr><td>

delivery\_plan

</td><td id="delivery_plan-entry-chg_req">

No longer in use. Sys\_id of the delivery plan associated with the change request.Data type: String

Table: Execution Plan \[sc\_cat\_item\_delivery\_plan\]

</td></tr><tr><td>

delivery\_task

</td><td id="delivery_task-entry-chg_req">

No longer in use. Sys\_id of the delivery task associated with the change request.Data type: String

Table: Execution Plan Task \[sc\_cat\_item\_delivery\_task\]

</td></tr><tr><td>

description

</td><td id="description-entry-chg_req">

Detailed description of the change request.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

due\_date

</td><td>

Task due date. Not used by change request process.Data type: String

</td></tr><tr><td>

end\_date

</td><td id="end_date-entry-chg_req">

Date and time when the change request is to be completed.Data type: String

</td></tr><tr><td>

escalation

</td><td id="escalation-entry-chg_req">

Current escalation level.Possible values:

-   0: Normal
-   1: Moderate
-   2: High
-   3: Overdue

Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

expected\_start

</td><td id="expected_start-entry-chg_req">

Date and time when the task is to start. Not used by the change request process.Data type: String

</td></tr><tr><td>

follow\_up

</td><td id="follow_up-entry-chg_req">

Date and time when a user followed-up with the person requesting the change request.Data type: String

</td></tr><tr><td>

group\_list

</td><td id="group_list-entry-chg_req">

List of sys\_ids and names of the groups associated with the change request.Data type: Array

Maximum length: 4,000

</td></tr><tr><td>

impact

</td><td id="impact-entry-chg_req">

Impact on the change request will have on the customer.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr><td>

implementation\_plan

</td><td id="imp_plan-entry-chg_req">

Sequential steps to execute to implement this change. It also contains any dependencies between steps and assignee details for each step.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

justification

</td><td id="justification-entry-chg_req">

Benefits of implementing this change and the impact if this change is not implemented.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

knowledge

</td><td id="knowledge-entry-chg_req">

Flag that indicates whether there are any knowledge base \(\)KB\) articles associated with the change request.Possible values:

-   true: Associated KB articles
-   false: No associated KB articles

Data type: Boolean

</td></tr><tr><td>

location

</td><td id="location-entry-chg_req">

Sys\_id and name of the location of the equipment referenced in the change request.Data type: String

Table: Location \[cmn\_location\]

</td></tr><tr><td>

made\_sla

</td><td id="made_sla-entry-chg_req">

No longer used. Flag that indicates whether the change request was implemented in alignment with the associated service level agreement.Data type: Boolean

</td></tr><tr><td>

needs\_attention

</td><td id="needs_attention-entry-chg_req">

Flag that indicates whether the change request needs attention.Possible values:

-   true: Change request needs additional attention.
-   false: Change request doesn't need additional attention.

Data type: Boolean

Default: false

</td></tr><tr><td>

number

</td><td id="number-entry-chg_req">

Change number assigned to the change request by the system, such as CHG0040007.Data type: String

</td></tr><tr><td>

on\_hold

</td><td id="on_hold-entry-chg_req">

Flag that indicates whether the change request is currently on hold.Possible values:

-   true: On hold
-   false: Not on hold

Data type: Boolean

Default: false

</td></tr><tr><td>

on\_hold\_reason

</td><td id="on_hold_reason-entry-chg_req">

If the **on\_hold** parameter is "true", description of the reason why the change request is being held up.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

on\_hold\_task

</td><td id="on_hold_task-entry-chg_req">

If the **on\_hold** parameter is "true", list of the sys\_ids of the tasks that must be completed before the hold is released.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

opened\_at

</td><td id="opened_at-entry-chg_req">

Date and time that the change release was created.Data type: String

</td></tr><tr><td>

opened\_by

</td><td id="opened_by-entry-chg_req">

Sys\_id and name of the user that created the change release.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

order

</td><td id="order-entry-chg_req">

Not used by Change Management. Optional numeric field by which to order records, such as when retrieving them from a database.Data type: Number \(Integer\)

</td></tr><tr><td>

outside\_maintenance\_schedule

</td><td id="outside_maint_sched-entry-chg_req">

Flag that indicates whether maintenance by an outside company has been schedule for the change request.Possible values:

-   true: Outside maintenance scheduled
-   false: No outside maintenance scheduled

Data type: Boolean

Default: false

</td></tr><tr><td>

parent

</td><td id="parent-entry-chg_req">

Sys\_id and name of the parent task to this change request, if any.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

phase

</td><td id="phase-entry-chg_req">

Current phase of the change request. This defines what the change is doing in greater detail.Possible values:

-   accept
-   build
-   plan
-   requested

Data type: String

</td></tr><tr><td>

phase\_state

</td><td id="phase_state-entry-chg_req">

Change\_phase records that should be created for a change. They are dependent on the category, such that each type of change may have different change\_phase records. The change\_phase records provide an opportunity to control the approval process as each change\_phase can have a schedule and a set of approvers.Possible values:

-   complete
-   on hold
-   open
-   rejected
-   requested
-   work in progress

Data type: String

</td></tr><tr><td>

priority

</td><td id="priority-entry-chg_req">

Priority of the change request.Possible values:

-   1: Critical
-   2: High
-   3: Moderate
-   4: Low

Data type: Number \(Integer\)

Default: 4

</td></tr><tr><td>

production\_system

</td><td id="prod_system-entry-chg_req">

Flag that indicates whether the change request is for a ServiceNow instance that is in a production environment.Possible values:

-   true: Production environment
-   false: Non-production environment

Data type: Boolean

</td></tr><tr><td>

reason

</td><td id="reason-entry-chg_req">

Description of why the change request was initiated.Possible values:

-   Business requirements
-   Hardware upgrade
-   Legislation
-   Location change
-   Network requirements
-   New or removed CI
-   Other
-   Problem resolved
-   Product or service changed
-   Software upgrade
-   User requested

Data type: String

Maximum length: 40

</td></tr><tr><td>

reassignment\_count

</td><td id="reassign_count-entry-chg_req">

Number of times that the change request has been reassigned to a new owner.Data type: Number \(Integer\)

Default: 0

</td></tr><tr><td>

rejection\_goto

</td><td id="rejection_goto-entry-chg_req">

Sys\_id of the task to perform if the change request is rejected.Data type: String

Table: Task \[task\]

</td></tr><tr><td>

requested\_by

</td><td id="requested_by-entry-chg_req">

Sys\_id of the user that requested the change.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

requested\_by\_date

</td><td id="requested_by_date-entry-chg_req">

Date and time when the change is requested to be implemented by.Data type: String

</td></tr><tr><td>

review\_comments

</td><td id="review_comments-entry-chg_req">

Comments entered when the change request was reviewed.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

review\_date

</td><td id="review_date-entry-chg_req">

Date that the change request was reviewed.Data type: String

</td></tr><tr><td>

review\_status

</td><td id="review_status-entry-chg_req">

Current status of the requested change request review.Data type: String

</td></tr><tr><td>

risk

</td><td id="risk-entry-chg_req">

Level of risk associated with the change request.Valid values:

-   1: High
-   2: Moderate
-   3: Low

Data type: Number

Default: 3

</td></tr><tr><td>

risk\_impact\_analysis

</td><td id="risk_impact_analysis-entry-chg_req">

Description of the risk and analysis of implementing the change request.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

route\_reason

</td><td id="route_reason-entry-chg_req">

Not currently used by Change Management. Reason that the change request was transferred.Possible values:

-   1: Transfer with Resolution
-   9: Transfer without Resolutions

Data type: Number

</td></tr><tr><td>

scope

</td><td id="scope-entry-chg_req">

Size of the change request.Possible values:

-   1: Massive
-   2: Large
-   3: Medium
-   4: Small
-   5: Tiny

Data type: Number

Default: 3

</td></tr><tr><td>

service\_offering

</td><td id="sevice_offering-entry-chg_req">

Sys\_id of the service offering associated with the change request. Service offerings uniquely define the level of service in terms of availability, scope, pricing, and packaging options.Data type: String

Table: Offering \[service\_offering\]

</td></tr><tr><td>

short\_description

</td><td id="short_desc-entry-chg_req">

Description of the change request.Data type: String

Maximum length: 40

</td></tr><tr><td>

skills

</td><td id="skills-entry-chg_req">

List of the sys\_ids of all of the skills required to implement the change request.Data type: Array

Table: Skill \[cmn\_skill\]

</td></tr><tr><td>

sla\_due

</td><td id="sla_due-entry-chg_req">

No longer in use. Date and time that the change request must be completed based on the associated service level agreement.Data type: String

</td></tr><tr><td>

sn\_esign\_document

</td><td>

Sys\_id of any E-signed document attached to the change request.Data type: String

Table: Attachment \[sys\_attachment\]

</td></tr><tr><td>

sn\_esign\_esignature\_configuration

</td><td>

Sys\_id of the E-signed signature template used for the associated document.Data type: String

Table: E-signature Template \[sn\_esign\_configuration\]

</td></tr><tr><td>

start\_date

</td><td id="start_date-entry-chg_req">

Date and time that the change request is planned to start implementation.Data type: String

</td></tr><tr><td>

state

</td><td id="state-entry-chg_req">

Current state of the change request. Possible values are defined in the change model.Data type: Number \(Integer\)

Default: 1

</td></tr><tr><td>

std\_change\_producer\_version

</td><td id="std_chg_prodversion-entry-chg_req">

Sys\_id of the record producer and change proposal associated with the change request. It also includes the number and percentage of successful and unsuccessful change requests created from the proposal.Data type: String

Table: Standard Change Template Version \[std\_change\_producer\_version\]

</td></tr><tr><td>

sys\_class\_name

</td><td id="sys_class_name-entry-chg_req">

Name of the table in which the change request is located.Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td id="sys_create_by-entry-chg_req">

Name of the user that initially created the change request.Data type: String

Maximum length: 40

</td></tr><tr><td>

sys\_created\_on

</td><td id="sys_created_on-entry-chg_req">

Date and time that the associated change request record was originally created.Data type: String

</td></tr><tr><td>

sys\_domain

</td><td id="sys_domain-entry-chg_req">

If using domains in the instance, the name of the domain to which the change module record is associated.Data type: String

</td></tr><tr><td>

sys\_domain\_path

</td><td id="sys_domain_path-entry-chg_req">

If using domains in the instance, the domain path in which the associated change module record resides.Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="sys_id-entry-chg_req">

Unique identifier of the associated change request record.Data type: String

</td></tr><tr id="casetable-sys_mod_count-row"><td>

sys\_mod\_count

</td><td id="sys_mod_count-entry-chg_req">

Number of updates to the case since it was initially created.Data type: Number \(Integer\)

</td></tr><tr id="casetable-sys_updated_by-row"><td>

sys\_updated\_by

</td><td id="sys_updated_by-entry-chg_req">

Person that last updated the case.Data type: String

Maximum length: 40

</td></tr><tr id="casetable-sys_updated_on-row"><td>

sys\_updated\_on

</td><td id="sys_updated_on-entry-chg_req">

Date and time when the case was last updated.Data type: String

</td></tr><tr><td>

task\_effective\_number

</td><td id="task_eff_number-entry-chg_req">

Universal request number.Data type: String

Maximum length: 40

</td></tr><tr><td>

task\_for

</td><td id="task_for-entry-chg_req">

Not used by Change Management. Sys\_id of the user that the task was created for.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

test\_plan

</td><td id="test_plan-entry-chg_req">

Description of the associated test plan for the change.Data type: String

Maximum length: 4,000

</td></tr><tr id="casetable-time_worked-row"><td>

time\_worked

</td><td id="time_worked-entry-chg_req">

Total amount of time worked on the change request.Data type: String

</td></tr><tr><td>

type

</td><td id="type-entry-chg_req">

Change request type.Possible values:

-   emergency
-   normal
-   standard

Data type: String

Maximum length: 40

</td></tr><tr><td>

unauthorized

</td><td id="unauthorized-entry-chg_req">

Flag that indicates whether the change request is unauthorizedPossible values:

-   true: Unauthorized
-   false: Authorized

Data type: Boolean

</td></tr><tr><td>

universal\_request

</td><td id="universal_request-entry-chg_req">

Sys\_id of the Parent Universal request to which this change request is a part of.Data type: String

Table: Task \[task\]

</td></tr><tr id="casetable-upon_approval-row"><td>

upon\_approval

</td><td id="upon_approval-entry-chg_req">

Action to take if the change request is approved.Possible values:

-   do\_nothing
-   proceed

Data type: String

Maximum length: 40

Default: proceed

</td></tr><tr id="casetable-upon_reject-row"><td>

upon\_reject

</td><td id="upon_reject-entry-chg_req">

Action to take if the change request is rejected.Possible values:

-   cancel
-   goto

Data type: String

Maximum length: 40

Default: cancel

</td></tr><tr id="casetable-urgency-row"><td>

urgency

</td><td id="urgency-entry-chg_req">

Urgency of the change request.Possible values:

-   1: High
-   2: Medium
-   3: Low

Data type: Number \(Integer\)

Default: 3

</td></tr><tr id="casetable-user_input-row"><td>

user\_input

</td><td id="user_input-entry-chg_req">

Additional user input.Data type: String

Maximum length: 4,000

</td></tr><tr id="casetable-variables-row"><td>

variables

</td><td id="variables-entry-chg_req">

Name-value pairs of variables associated with the change request.Data type: String

Maximum length: 40

</td></tr><tr id="casetable-watch_list-row"><td>

watch\_list

</td><td id="watch_list-entry-chg_req">

List of sys\_ids of the users who receive notifications about this change request when additional comments are added or if the state of a change request is changed to Resolved or Closed.Data type: Array

Table: User \[sys\_user\]

</td></tr><tr id="casetable-wf_activity-row"><td>

wf\_activity

</td><td id="wf_activity-entry-chg_req">

Sys\_id of the workflow activity record associated with the change request.Data type: String

Table: Workflow Activity \[wf\_activity\]

</td></tr><tr id="casetable-work_end-row"><td>

work\_end

</td><td id="work_end-entry-chg_req">

Date and time work ended on the change request.Data type: String

</td></tr><tr id="casetable-work_notes-row"><td>

work\_notes

</td><td id="work_notes-entry-chg_req">

Information about how to resolve the change request, or steps taken to resolve it.Data type: String

Maximum length: 4,000

</td></tr><tr id="casetable-work_notes_list-row"><td>

work\_notes\_list

</td><td id="work_notes_list-entry-chg_req">

List of sys\_ids of the internal users who receive notifications about this change request when work notes are added. Data type: Array

Table: User \[sys\_user\]

</td></tr><tr id="casetable-work_start-row"><td>

work\_start

</td><td id="work_start-entry-chg_req">

Date and time that work started on the change request.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/b0dbda5347c12200e0ef563dbb9a718f" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result":
    {
      "reason": {
        "display_value": "",
        "value": ""
      },
      "parent": {
        "display_value": "",
        "value": ""
      },
      "watch_list": {
        "display_value": "",
        "value": ""
       },
       "proposed_change": {
         "display_value": "",
         "value": ""
       },
       "upon_reject": {
         "display_value": "Cancel all future Tasks",
         "value": "cancel"
       },
       "sys_updated_on": {
         "display_value": "2015-07-06 11:59:27",
         "value": "2015-07-06 18:59:27",
         "display_value_internal": "2015-07-06 11:59:27"
      },
      "type": {
        "display_value": "Standard",
        "value": "standard"
      },
      "approval_history": {
        "display_value": "",
        "value": ""
      },
      "skills": {
        "display_value": "",
        "value": ""
      },
      "test_plan": {
        "display_value": "--Confirm that there are no monitoring alerts for the router",
        "value": "--Confirm that there are no monitoring alerts for the router"
      },
      "number": {
        "display_value": "CHG0000024",
        "value": "CHG0000024"
      },
      "is_bulk": {
        "display_value": "false",
        "value": false
      },
      "cab_delegate": {
        "display_value": "",
        "value": ""
      },
      "requested_by_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "ci_class": {
        "display_value": "cmdb_ci",
        "value": "cmdb_ci"
      },
      "state": {
        "display_value": "Closed",
        "value": 3.0
      },
      "sys_created_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "knowledge": {
        "display_value": "false",
        "value": false
      },
      "order": {
        "display_value": "",
        "value": ""
      },
      "phase": {
        "display_value": "Requested",
        "value": "requested"
      },
      "cmdb_ci": {
        "display_value": "",
        "value": ""
      },
      "delivery_plan": {
        "display_value": "",
        "value": ""
      },
      "impact": {
        "display_value": "3 - Low",
        "value": 3.0
      },
      "contract": {
        "display_value": "",
        "value": ""
      },
      "active": {
        "display_value": "false",
        "value": false
      },
      "work_notes_list": {
        "display_value": "",
        "value": ""
      },
      "priority": {
        "display_value": "4 - Low",
        "value": 4.0
      },
      "sys_domain_path": {
        "display_value": "/",
        "value": "/"
      },
      "cab_recommendation": {
        "display_value": "",
        "value": ""
      },
      "production_system": {
        "display_value": "false",
        "value": false
      },
      "rejection_goto": {
        "display_value": "",
        "value": ""
      },
      "review_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "requested_by": {
        "display_value": "System Administrator",
        "value": "6816f79cc0a8016401c5a33be04be441"
      },
      "business_duration": {
        "display_value": "",
        "value": ""
      },
      "group_list": {
        "display_value": "",
        "value": ""
      },
      "change_plan": {
        "display_value": "",
        "value": ""
      },
      "approval_set": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "wf_activity": {
        "display_value": "",
        "value": ""
      },
      "implementation_plan": {
        "display_value": "-- Place router into maintenance mode in the monitoring platform\r\n-- Logon to router through SSH\r\n-- Run the following command\r\n\r\nrouter(config-router)#router bgp 12345\r\nrouter(config-router)#neighbor {neighbor ip} soft-reconfig [inbound]\r\nrouter#clear ip bgp {neighbor ip} soft in\r\n\r\n-- Confirm the sessions have been cleared\r\n-- Place router back into operational mode in the monitoring platform",
        "value": "-- Place router into maintenance mode in the monitoring platform\r\n-- Logon to router through SSH\r\n-- Run the following command\r\n\r\nrouter(config-router)#router bgp 12345\r\nrouter(config-router)#neighbor {neighbor ip} soft-reconfig [inbound]\r\nrouter#clear ip bgp {neighbor ip} soft in\r\n\r\n-- Confirm the sessions have been cleared\r\n-- Place router back into operational mode in the monitoring platform"
      },
      "universal_request": {
        "display_value": "",
        "value": ""
      },
      "end_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "short_description": {
        "display_value": "Clear BGP sessions on a Cisco router",
        "value": "Clear BGP sessions on a Cisco router"
      },
      "correlation_display": {
        "display_value": "",
        "value": ""
      },
      "work_start": {
        "display_value": "2015-07-06 11:56:04",
        "value": "2015-07-06 18:56:04",
        "display_value_internal": "2015-07-06 11:56:04"
      },
      "delivery_task": {
        "display_value": "",
        "value": ""
      },
      "outside_maintenance_schedule": {
        "display_value": "false",
        "value": false
      },
      "additional_assignee_list": {
        "display_value": "",
        "value": ""
      },
      "std_change_producer_version": {
        "display_value": "Clear BGP sessions on a Cisco router - 1",
        "value": "16c2273c47010200e90d87e8dee49006"
      },
      "sys_class_name": {
        "display_value": "Change Request",
        "value": "change_request"
      },
      "service_offering": {
        "display_value": "",
        "value": ""
      },
      "closed_by": {
        "display_value": "System Administrator",
        "value": "6816f79cc0a8016401c5a33be04be441"
      },
      "follow_up": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "review_status": {
        "display_value": "",
        "value": ""
      },
      "reassignment_count": {
        "display_value": "2",
        "value": 2.0
      },
      "start_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "assigned_to": {
        "display_value": "",
        "value": ""
      },
      "variables": {
        "display_value": "variable_pool",
        "value": "variable_pool"
      },
      "sla_due": {
        "display_value": "UNKNOWN",
        "value": "",
        "display_value_internal": ""
      },
      "comments_and_work_notes": {
        "display_value": "",
        "value": ""
      },
      "escalation": {
        "display_value": "Normal",
        "value": 0.0
      },
      "upon_approval": {
        "display_value": "Proceed to Next Task",
        "value": "proceed"
      },
      "correlation_id": {
        "display_value": "",
        "value": ""
      },
      "made_sla": {
        "display_value": "true",
        "value": true
      },
      "backout_plan": {
        "display_value": "Due to the limited number of commands in the implementation plan it is not possible to backout the change.\r\n\r\nIf required you are authorized to reboot the router if BGP fails to work",
        "value": "Due to the limited number of commands in the implementation plan it is not possible to backout the change.\r\n\r\nIf required you are authorized to reboot the router if BGP fails to work"
      },
      "conflict_status": {
        "display_value": "Not Run",
        "value": "Not Run"
      },
      "task_effective_number": {
        "display_value": "CHG0000024",
        "value": "CHG0000024"
      },
      "sys_updated_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "opened_by": {
        "display_value": "System Administrator",
        "value": "6816f79cc0a8016401c5a33be04be441"
      },
      "user_input": {
        "display_value": "",
        "value": ""
      },
      "sys_created_on": {
        "display_value": "2015-07-06 11:55:46",
        "value": "2015-07-06 18:55:46",
        "display_value_internal": "2015-07-06 11:55:46"
      },
      "on_hold_task": {
        "display_value": "",
        "value": ""
      },
      "sys_domain": {
        "display_value": "global",
        "value": "global"
      },
      "route_reason": {
        "display_value": "",
        "value": ""
      },
      "closed_at": {
        "display_value": "2015-07-06 11:56:23",
        "value": "2015-07-06 18:56:23",
        "display_value_internal": "2015-07-06 11:56:23"
      },
      "review_comments": {
        "display_value": "",
        "value": ""
      },
      "business_service": {
        "display_value": "",
        "value": ""
      },
      "time_worked": {
        "display_value": "",
        "value": ""
      },
      "chg_model": {
        "display_value": "",
        "value": ""
      },
      "expected_start": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "opened_at": {
        "display_value": "2015-06-09 11:55:46",
        "value": "2015-06-09 18:55:46",
        "display_value_internal": "2015-06-09 11:55:46"
      },
      "work_end": {
        "display_value": "2015-07-06 11:56:10",
        "value": "2015-07-06 18:56:10",
        "display_value_internal": "2015-07-06 11:56:10"
      },
      "phase_state": {
        "display_value": "Open",
        "value": "open"
      },
      "cab_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "work_notes": {
        "display_value": "",
        "value": ""
      },
      "close_code": {
        "display_value": "Successful",
        "value": "successful"
      },
      "assignment_group": {
        "display_value": "Network",
        "value": "287ebd7da9fe198100f92cc8d1d2154e"
      },
      "description": {
        "display_value": "Resend the complete BGP table to neighboring routers\r\n\r\n--Both neighbors need to support soft reset route refresh capability.\r\n--Stores complete BGP table of you neighbor in router memory.\r\n--Not a good idea on a peering router with full feed, due to the memory requirements.\r\n",
        "value": "Resend the complete BGP table to neighboring routers\r\n\r\n--Both neighbors need to support soft reset route refresh capability.\r\n--Stores complete BGP table of you neighbor in router memory.\r\n--Not a good idea on a peering router with full feed, due to the memory requirements.\r\n"
      },
      "on_hold_reason": {
        "display_value": "",
        "value": ""
      },
      "calendar_duration": {
        "display_value": "",
        "value": ""
      },
      "close_notes": {
        "display_value": "Completed without issues",
        "value": "Completed without issues"
      },
      "sys_id": {
        "display_value": "1766f1de47410200e90d87e8dee490f6",
        "value": "1766f1de47410200e90d87e8dee490f6"
      },
      "contact_type": {
        "display_value": "Phone",
        "value": "phone"
      },
      "cab_required": {
        "display_value": "false",
        "value": false
      },
      "urgency": {
        "display_value": "3 - Low",
        "value": 3.0
      },
      "scope": {
        "display_value": "Medium",
        "value": 3.0
      },
      "company": {
        "display_value": "",
        "value": ""
      },
      "justification": {
        "display_value": "",
        "value": ""
      },
      "activity_due": {
        "display_value": "UNKNOWN",
        "value": "",
        "display_value_internal": ""
      },
      "comments": {
        "display_value": "",
        "value": ""
      },
      "approval": {
        "display_value": "Approved",
        "value": "approved"
      },
      "due_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "sys_mod_count": {
        "display_value": "10",
        "value": 10.0
      },
      "on_hold": {
        "display_value": "false",
        "value": false
      },
      "sys_tags": {
        "display_value": "",
        "value": ""
      },
      "conflict_last_run": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "risk_value": {
        "display_value": "",
        "value": ""
      },
      "unauthorized": {
        "display_value": "false",
        "value": false
      },
      "risk": {
        "display_value": "Moderate",
        "value": 3.0
      },
      "location": {
        "display_value": "",
        "value": ""
      },
      "category": {
        "display_value": "Other",
        "value": "Other"
      },
      "risk_impact_analysis": {
        "display_value": "",
        "value": ""
      }
    }
}
```

## Change Management - GET /sn\_chg\_rest/change/\{sys\_id\}/ci

Retrieves multiple configuration items \(CIs\) associated to a specified change request based on the specified association type.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{sys_id}/ci`

Default URL: `/api/sn_chg_rest/change/{sys_id}/ci`

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

sys\_id

</td><td>

Sys\_id of the change request for which to return the associated CMDB CIs.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

association\_type

</td><td>

Required. Type of association between the CMDB CI and the change request. Valid values:

-   affected: CIs that are affected by the change request
-   impacted: Services impacted by the change request
-   offering: Impacted service offerings

Data type: String

</td></tr><tr><td>

name-value pairs

</td><td>

Name-value pairs to use to filter the result set. The name is the field on which the specified value is filtered. This parameter is mutually exclusive with **sysparm\_query**. For example, instead of using `&sysparm_query=active=true`, you can simplify the calling statement by using `&active=true`. You can also use the display value when the field is a choice or reference type field, such as `&state=closed` instead of `&state=7`. To specify multiple key-value pairs, separate each with an ampersand, such as `&active=true&assigned_to=john.smith`. Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. Data type: Number

Default: 500

</td></tr><tr><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td>

[Encoded query](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) used to filter the result set. You can use a UI filter to obtain a properly encoded query.Syntax: `sysparm_query=<col_name><operator><value>`. Column names, operators, and values are case-sensitive.

-   &lt;col\_name&gt;: Name of the table column to filter on.
-   &lt;operator&gt;: Supports the following values:
    -   `=`: &lt;col\_name&gt; exactly matches &lt;value&gt;.
    -   `!=`: &lt;col\_name&gt; does not match &lt;value&gt;.
    -   `LIKE`: &lt;col\_name&gt; contains the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `STARTSWITH`: &lt;col\_name&gt; starts with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `ENDSWITH`: &lt;col\_name&gt; ends with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `^`: AND operator to add an additional query condition. Records included in the result set match both conditions.
    -   `^OR`: OR operator to add an additional query condition. Records included in the result set match at least one of the conditions.
-   &lt;value&gt;: Value to filter on.

For more information about operators, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Queries can contain multiple conditions. For example, the following query returns records where the caller is the current user and the record is active.

`sysparm_query=caller_id=javascript:gs.getUserID()^active=true`

Encoded queries also support order by ascending and descending functionality. To sort responses based on certain fields, use the `ORDERBY` and `ORDERBYDESC` clauses in **sysparm\_query**.

Syntax:

-   `ORDERBY<col_name>`
-   `ORDERBYDESC<col_name>`

For example, the following query gets all active records and orders the results in ascending order by number, and then in descending order by category.

`sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory`

By default, if part of a query is invalid, such as an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. Set the property **glide.invalid\_query.returns\_no\_rows** to `true` to instead return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. A bad request type or malformed request was detected. The error response contains pertinent messages to help troubleshoot the problem.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ci\_item\|cmdb\_ci\_service

</td><td>

Either the ci\_item or cmdb\_ci\_service variables, depending upon the association type.Data type: Array

```
ci_item|cmdb_ci_service : {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

ci\_item\|cmdb\_ci\_service.value

</td><td>

Sys\_id of the ci\_item or cmdb\_ci\_service.Data type: String

</td></tr><tr><td>

ci\_item\|cmdb\_ci\_service.display\_value

</td><td>

Display value of the ci\_item or cmdb\_ci\_service.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Change request sys\_id information.Data type: Object

```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the change request.Data type: String

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the change request to display in a UI.Data type: String

</td></tr><tr><td>

&lt;record\_fields&gt;

</td><td>

All valid fields in the ci\_item or cmdb\_ci\_service record; table based on association type.Data type: Object

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/c286d61347c12200e0ef563dbb9a71df/ci?association_type=affected" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'

```

```
{
  result: [
    {
      sys_id: {
        value: "92b8544047810200e90d87e8dee490b0",
        display_value: "92b8544047810200e90d87e8dee490b0"
      },
      ci_item|cmdb_ci_service : {
        value: "3a27d4370a0a0bb4006316812bf45439", 
        display_value: "PS Apache01"
      },
      ..., // all valid fields in record, table based on association type
    }, 
    { // next record found }, ... // and so on
  ]
}
```

## Change Management - GET /sn\_chg\_rest/change/\{sys\_id\}/conflict

Retrieves the status of the currently running change request conflict checking process or the results of the last completed conflict checking process for the specified change request.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{sys_id}/conflict`

Default URL: `/api/sn_chg_rest/change/{sys_id}/conflict`

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

sys\_id

</td><td>

Sys\_id of the change request for which to return the status of the running/completed conflict checking process.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Current status of the conflict checking process; including conflicts if any are detected.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

conflicts

</td><td>

List of conflicts found for the change request. An empty object indicates that no conflicts were detected.Data type: Array

</td></tr><tr><td>

job\_status

</td><td>

Status of the actual conflict checking job.Data type: String

</td></tr><tr><td>

last\_run

</td><td>

Date and time the last conflict checking process started.Data type: String

</td></tr><tr><td>

record\_count

</td><td>

Number of records checked.Data type: String

</td></tr><tr><td>

status

</td><td>

Outcome of the conflict checking process, such as "Conflict" or "Not run". **Note:** Even if the change request does not have any conflicts, this field is set to "Conflict." However, the **conflicts** object is empty.

 Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/0f4ac6c4b750230096c3e4f6ee11a9fe/conflict" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

Successful response - no conflicts

```
{
  result: {
    status: "Conflict",
    last_run": "2018-08-30 12:58:05",
    record_count: "1",
    job_status: "2",
    conflicts: []
  }
}
```

### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/0f4ac6c4b750230096c3e4f6ee11a9fe/conflict" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

Successful response - with conflicts

```
{
  result: {
    status: "Conflict",
    last_run": "2018-08-30 12:58:05",
    record_count: "1",
    job_status: "2",
    conflicts: [
      {
        change: {
          display_value: "CHG0030001",
          value: "afbffb24b758230096c3e4f6ee11a972"
        },
        type: {
          display_value: "Not In Maintenance Window",
          value: "not_in_maintenance_window"
        }
        ..., // all valid fields in record, example below
      }
    ]
  }
}
```

## Change Management - GET /sn\_chg\_rest/change/emergency

Retrieves one or more emergency change requests based on the specified criteria.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/emergency`

Default URL: `/api/sn_chg_rest/change/emergency`

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

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

order

</td><td>

Field by which to sort the returned change requests. Data type: String

Default: *number*

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. Data type: Number

Default: 500

</td></tr><tr><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td>

[Encoded query](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) used to filter the result set. You can use a UI filter to obtain a properly encoded query.Syntax: `sysparm_query=<col_name><operator><value>`. Column names, operators, and values are case-sensitive.

-   &lt;col\_name&gt;: Name of the table column to filter on.
-   &lt;operator&gt;: Supports the following values:
    -   `=`: &lt;col\_name&gt; exactly matches &lt;value&gt;.
    -   `!=`: &lt;col\_name&gt; does not match &lt;value&gt;.
    -   `LIKE`: &lt;col\_name&gt; contains the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `STARTSWITH`: &lt;col\_name&gt; starts with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `ENDSWITH`: &lt;col\_name&gt; ends with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `^`: AND operator to add an additional query condition. Records included in the result set match both conditions.
    -   `^OR`: OR operator to add an additional query condition. Records included in the result set match at least one of the conditions.
-   &lt;value&gt;: Value to filter on.

For more information about operators, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Queries can contain multiple conditions. For example, the following query returns records where the caller is the current user and the record is active.

`sysparm_query=caller_id=javascript:gs.getUserID()^active=true`

Encoded queries also support order by ascending and descending functionality. To sort responses based on certain fields, use the `ORDERBY` and `ORDERBYDESC` clauses in **sysparm\_query**.

Syntax:

-   `ORDERBY<col_name>`
-   `ORDERBYDESC<col_name>`

For example, the following query gets all active records and orders the results in ascending order by number, and then in descending order by category.

`sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory`

By default, if part of a query is invalid, such as an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. Set the property **glide.invalid\_query.returns\_no\_rows** to `true` to instead return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

</td></tr><tr><td>

key-value pairs

</td><td>

Name-value pairs to use to filter the result set. The name is the field on which the specified value is filtered. This parameter is mutually exclusive with **sysparm\_query**. For example, instead of using `&sysparm_query=active=true`, you can simplify the calling statement by using `&active=true`. You can also use the display value when the field is a choice or reference type field, such as `&state=closed` instead of `&state=7`. To specify multiple key-value pairs, separate each with an ampersand, such as `&active=true&assigned_to=john.smith`. Data type: String

</td></tr><tr><td>

textSearch

</td><td>

String to use to search all emergency change request record fields. This search uses ServiceNow full text search platform functionality and defaults to `IR_AND_OR_QUERY`.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Values for all fields in the associated change request.Data type: Object

</td></tr><tr><td>

state

</td><td>

State of the change request.Data type: Object

```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in a UI.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id information for the change request.Data type: Object

```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the change request to display in a UI.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the change request.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of change request.Data type: Object

```
type: {
  display_value: "String",
  value: "String"
}
```

</td></tr><tr><td>

type.display\_value

</td><td>

Change type to display in a UI.Value is always "Emergency".

Data type: String

</td></tr><tr><td>

type.value

</td><td>

Internal type value.Value is always "emergency".

Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/emergency?sysparm_query=active=true^ORDERBYnumber" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  result: [
    {
      sys_id: {
        value: "1c87925347c12200e0ef563dbb9a7177",
        display_value: "1c87925347c12200e0ef563dbb9a7177"
      },
      state: {
        value: "-5", 
        display_value: "New"
      },
      type: {
        value: "emergency",
        display_value: "Emergency"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Reboot server",
        display_value: "Reboot server"
      },
    }, 
    { // next record found }, ... // and so on
  ]
}
```

## Change Management - GET /sn\_chg\_rest/change/emergency/\{sys\_id\}

Retrieves the emergency change request identified by the specified sys\_id.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/emergency/{sys_id}`

Default URL: `/api/sn_chg_rest/change/emergency/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the emergency change request to retrieve.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Values for all fields in the associated change request.Data type: Object

</td></tr><tr><td>

state

</td><td>

State of the change request.Data type: Object

```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in a UI.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id information for the change request.Data type: Object

```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the change request to display in a UI.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the change request.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of change request.Data type: Object

```
type: {
  display_value: "String",
  value: "String"
}
```

</td></tr><tr><td>

type.display\_value

</td><td>

Change type to display in a UI.Value is always "Emergency".

Data type: String

</td></tr><tr><td>

type.value

</td><td>

Internal type value.Value is always "emergency".

Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/emergency/b0dbda5347c12200e0ef563dbb9a718f" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  result: [
    {
      sys_id: {
        value: "b0dbda5347c12200e0ef563dbb9a718f", 
        display_value: "b0dbda5347c12200e0ef563dbb9a718f"
      },
      state: {
        value: "-5", 
        display_value: "New"
      },
      type: {
        value: "emergency",
        display_value: "Emergency"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Reboot server",
        display_value: "Reboot server"
      },
    },
  ]
}
```

## Change Management - GET /sn\_chg\_rest/change/model

Retrieves one or more change models based on the specified criteria.

Use this endpoint to find a change model that best fits the change request that you are trying to create. For additional information, see [Change Models](https://www.servicenow.com/docs/access?context=change-models&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/model`

Default URL: `/api/sn_chg_rest/change/model`

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

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Name-value pairs to use to filter the result set. The name is the field on which the specified value is filtered. This parameter is mutually exclusive with **sysparm\_query**. For example, instead of using `&sysparm_query=active=true`, you can simplify the calling statement by using `&active=true`. You can also use the display value when the field is a choice or reference type field, such as `&state=closed` instead of `&state=7`. To specify multiple key-value pairs, separate each with an ampersand, such as `&active=true&assigned_to=john.smith`. Data type: String

</td></tr><tr><td>

order

</td><td>

Field by which to sort the returned change models.Data type: String

Default: *name*

</td></tr><tr><td>

sysparm\_offset

</td><td id="sysparm_offset-entry-RESTAPI">

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td id="sysparm-query-RESTAPI">

[Encoded query](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) used to filter the result set. You can use a UI filter to obtain a properly encoded query.Syntax: `sysparm_query=<col_name><operator><value>`. Column names, operators, and values are case-sensitive.

-   &lt;col\_name&gt;: Name of the table column to filter on.
-   &lt;operator&gt;: Supports the following values:
    -   `=`: &lt;col\_name&gt; exactly matches &lt;value&gt;.
    -   `!=`: &lt;col\_name&gt; does not match &lt;value&gt;.
    -   `LIKE`: &lt;col\_name&gt; contains the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `STARTSWITH`: &lt;col\_name&gt; starts with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `ENDSWITH`: &lt;col\_name&gt; ends with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `^`: AND operator to add an additional query condition. Records included in the result set match both conditions.
    -   `^OR`: OR operator to add an additional query condition. Records included in the result set match at least one of the conditions.
-   &lt;value&gt;: Value to filter on.

For more information about operators, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Queries can contain multiple conditions. For example, the following query returns records where the caller is the current user and the record is active.

`sysparm_query=caller_id=javascript:gs.getUserID()^active=true`

Encoded queries also support order by ascending and descending functionality. To sort responses based on certain fields, use the `ORDERBY` and `ORDERBYDESC` clauses in **sysparm\_query**.

Syntax:

-   `ORDERBY<col_name>`
-   `ORDERBYDESC<col_name>`

For example, the following query gets all active records and orders the results in ascending order by number, and then in descending order by category.

`sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory`

By default, if part of a query is invalid, such as an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. Set the property **glide.invalid\_query.returns\_no\_rows** to `true` to instead return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

</td></tr><tr><td>

textSearch

</td><td>

String to use to search all change model record fields. This search uses ServiceNow full text search platform functionality. For more information on ServiceNow search capabilities, see [Search administration](https://www.servicenow.com/docs/access?context=search-administration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).Data type: String

Default: `IR_AND_OR_QUERY`

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

List containing one or more change model record objects. Each object describes a change model. Each element in the change model object corresponds to a field in its associated record in the Change Model \[chg\_model\] table.All elements contain value and display\_value name-value pairs. Some contain display\_value\_internal name-value pairs.

Data type: Array

</td></tr><tr><td>

result.active

</td><td>

Flag that indicates whether the associated change model record is active and available within the instance.Valid values:

-   true: Change model is active.
-   false: Change model isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

result.available\_in\_ui

</td><td>

Flag that indicates whether the associated change model record is available within the user interface.Valid values:

-   true: Change model is available in the user interface.
-   false: Change model isn't available in the user interface.

Data type: Boolean

Default: true

</td></tr><tr><td>

result.color

</td><td>

Color of the associated change model on the change request landing page.Data type: String

Default: \#cbcbcb

</td></tr><tr><td>

result.default\_change\_model

</td><td>

Flag that indicates whether the associated change model record is the default change model.Valid values:

-   true: Default
-   false: Not the default

Data type: Boolean

Default: false

</td></tr><tr><td>

result.description

</td><td>

Short description of the purpose of the change model.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

result.name

</td><td>

Name of the change model.Data type: String

Maximum length: 200

</td></tr><tr><td>

result.record\_preset

</td><td>

Name-value pairs of the fields that should automatically be populated, with their associated values, when a new change request record is created. Values are separated by caret symbols.For example:

`"type=normal^assignment_group=a715cd759f2002002920bde8132e7018^short_description=Automated : Change^EQ"`

Data type: String

</td></tr><tr><td>

result.state\_field

</td><td>

Choice list field from which to collect choices, based on the provided in **table\_name**. For change models, this is always set to "state".Data type: String

</td></tr><tr><td>

result.sys\_class\_name

</td><td>

Change module table name. Always Change Model/chg\_model.Data type: String

</td></tr><tr><td>

result.sys\_created\_by

</td><td>

Name of the user that initially created the associated change module record. Data type: String

</td></tr><tr><td>

result.sys\_created\_on

</td><td>

Date and time that the change module record was originally created.Data type: String

</td></tr><tr><td>

result.sys\_domain

</td><td>

If using domains in the instance, the name of the domain to which the change module record is associated.Data type: String

</td></tr><tr><td>

result.sys\_domain\_path

</td><td>

If using domains in the instance, the domain path in which the associated change module record resides.Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Unique identifier of the associated change model record.Data type: String

</td></tr><tr><td>

result.sys\_mod\_count

</td><td>

Number of times that the associated change model record has been modified.Data type: Number

</td></tr><tr><td>

result.sys\_name

</td><td>

Name of the change model. Always the same as the **name** parameter.Data type: String

</td></tr><tr><td>

result.sys\_tags

</td><td>

System tags associated with the change model record.Data type: String

</td></tr><tr><td>

result.sys\_updated\_by

</td><td>

Name of the user that last updated the associated change model record.Data type: String

Maximum length: 40

</td></tr><tr><td>

result.sys\_updated\_on

</td><td>

Date and time the associated change model record was last updated.Data type: String

</td></tr><tr><td>

result.table\_name

</td><td>

Table that defines the Choice list field from which to collect choices. For change models this is always set to "change\_request".Data type: String

Maximum length: 80

</td></tr></tbody>
</table>### cURL request

This example shows a request for obtaining all change model records.

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/model \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

For brevity, this response only shows a single change model object.

```
{
  "result": [
    {
      "record_preset": {
        "display_value": "type=normal^assignment_group=a715cd759f2002002920bde8132e7018^short_description=Automated : Change^EQ",
        "value": "type=normal^assignment_group=a715cd759f2002002920bde8132e7018^short_description=Automated : Change^EQ"
      },
      "color": {
        "display_value": "#488df4",
        "value": "#488df4"
      },
      "default_change_model": {
        "display_value": "false",
        "value": false
      },
      "sys_mod_count": {
        "display_value": "6",
        "value": 6.0
      },
      "description": {
        "display_value": "This model is intended to capture  a record of an automated change.  There are no approvals associated with this change model.\r\n",
        "value": "This model is intended to capture  a record of an automated change.  There are no approvals associated with this change model.\r\n"
      },
      "active": {
        "display_value": "true",
        "value": true
      },
      "sys_updated_on": {
        "display_value": "2020-10-02 06:24:24",
        "value": "2020-10-02 13:24:24",
        "display_value_internal": "2020-10-02 06:24:24"
      },
      "sys_tags": {
        "display_value": "",
        "value": ""
      },
        "table_name": {
        "display_value": "change_request",
        "value": "change_request"
      },
      "sys_class_name": {
        "display_value": "Change Model",
        "value": "chg_model"
      },
      "sys_id": {
        "display_value": "7840d2515323101034d1ddeeff7b12a6",
        "value": "7840d2515323101034d1ddeeff7b12a6"
      },
      "sys_updated_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "available_in_ui": {
        "display_value": "false",
        "value": false
      },
      "state_field": {
        "display_value": "state",
        "value": "state"
      },
      "sys_created_on": {
        "display_value": "2020-09-28 07:33:25",
        "value": "2020-09-28 14:33:25",
        "display_value_internal": "2020-09-28 07:33:25"
      },
      "name": {
        "display_value": "Change Registration",
        "value": "Change Registration"
      },
      "sys_name": {
        "display_value": "Change Registration",
        "value": "Change Registration"
      },
      "sys_created_by": {
        "display_value": "admin",
        "value": "admin"
      }
    }
  ]
}
```

## Change Management - GET /sn\_chg\_rest/change/model/\{sys\_id\}

Retrieves the change model identified by the specified sys\_id.

You can then use this change model to create the desired change request. For additional information on change models, see [Change Models](https://www.servicenow.com/docs/access?context=change-models&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/model/{sys_id}`

Default URL: `/api/sn_chg_rest/change/model/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the change model record to retrieve from the Change Model \[chg\_model\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Requested change model record object. Each element in this object corresponds to a field in the record in the Change Model \[chg\_model\] table.All elements contain **value** and **display\_value** name-value pairs. Some contain **display\_value\_internal** name-value pairs.

Data type: Object

</td></tr><tr><td>

result.active

</td><td>

Flag that indicates whether the associated change model record is active and available within the instance.Valid values:

-   true: Change model is active.
-   false: Change model isn't active.

Data type: Boolean

Default: true

</td></tr><tr><td>

result.available\_in\_ui

</td><td>

Flag that indicates whether the associated change model record is available within the user interface.Valid values:

-   true: Change model is available in the user interface.
-   false: Change model isn't available in the user interface.

Data type: Boolean

Default: true

</td></tr><tr><td>

result.color

</td><td>

Color of the associated change model on the change request landing page.Data type: String

Default: \#cbcbcb

</td></tr><tr><td>

result.default\_change\_model

</td><td>

Flag that indicates whether the associated change model record is the default change model.Valid values:

-   true: Default
-   false: Not the default

Data type: Boolean

Default: false

</td></tr><tr><td>

result.description

</td><td>

Short description of the purpose of the change model.Data type: String

Maximum length: 4,000

</td></tr><tr><td>

result.name

</td><td>

Name of the change model.Data type: String

Maximum length: 200

</td></tr><tr><td>

result.record\_preset

</td><td>

Name-value pairs of the fields that should automatically be populated, with their associated values, when a new change request record is created. Values are separated by caret symbols.For example:

`"type=normal^assignment_group=a715cd759f2002002920bde8132e7018^short_description=Automated : Change^EQ"`

Data type: String

</td></tr><tr><td>

result.state\_field

</td><td>

Choice list field from which to collect choices, based on the provided in **table\_name**. For change models, this is always set to "state".Data type: String

</td></tr><tr><td>

result.sys\_class\_name

</td><td>

Change module table name. Always Change Model/chg\_model.Data type: String

</td></tr><tr><td>

result.sys\_created\_by

</td><td>

Name of the user that initially created the associated change module record. Data type: String

</td></tr><tr><td>

result.sys\_created\_on

</td><td>

Date and time that the change module record was originally created.Data type: String

</td></tr><tr><td>

result.sys\_domain

</td><td>

If using domains in the instance, the name of the domain to which the change module record is associated.Data type: String

</td></tr><tr><td>

result.sys\_domain\_path

</td><td>

If using domains in the instance, the domain path in which the associated change module record resides.Data type: String

</td></tr><tr><td>

result.sys\_id

</td><td>

Unique identifier of the associated change model record.Data type: String

</td></tr><tr><td>

result.sys\_mod\_count

</td><td>

Number of times that the associated change model record has been modified.Data type: Number

</td></tr><tr><td>

result.sys\_name

</td><td>

Name of the change model. Always the same as the **name** parameter.Data type: String

</td></tr><tr><td>

result.sys\_tags

</td><td>

System tags associated with the change model record.Data type: String

</td></tr><tr><td>

result.sys\_updated\_by

</td><td>

Name of the user that last updated the associated change model record.Data type: String

Maximum length: 40

</td></tr><tr><td>

result.sys\_updated\_on

</td><td>

Date and time the associated change model record was last updated.Data type: String

</td></tr><tr><td>

result.table\_name

</td><td>

Table that defines the Choice list field from which to collect choices. For change models this is always set to "change\_request".Data type: String

Maximum length: 80

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/model/c0efda5347c12200e0ef563dbb9a81e3" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": {
    "record_preset": {
      "display_value": "type=emergency^EQ",
      "value": "type=emergency^EQ"
    },
    "color": {
      "display_value": "#ea3423",
      "value": "#ea3423"
    },
    "default_change_model": {
      "display_value": "false",
      "value": false
    },
    "sys_mod_count": {
      "display_value": "2",
      "value": 2.0
    },
    "description": {
      "display_value": "ITIL Mode 1 Emergency Change",
      "value": "ITIL Mode 1 Emergency Change"
    },
    "active": {
      "display_value": "true",
      "value": true
    },
    "sys_updated_on": {
      "display_value": "2020-09-28 08:53:12",
      "value": "2020-09-28 15:53:12",
      "display_value_internal": "2020-09-28 08:53:12"
    },
    "sys_tags": {
      "display_value": "",
      "value": ""
    },
    "table_name": {
      "display_value": "change_request",
      "value": "change_request"
    },
    "sys_class_name": {
      "display_value": "Change Model",
      "value": "chg_model"
    },
    "sys_id": {
      "display_value": "c0efda5347c12200e0ef563dbb9a81e3",
      "value": "c0efda5347c12200e0ef563dbb9a81e3"
    },
    "sys_updated_by": {
      "display_value": "admin",
      "value": "admin"
    },
    "available_in_ui": {
      "display_value": "true",
      "value": true
    },
    "state_field": {
      "display_value": "state",
      "value": "state"
    },
    "sys_created_on": {
      "display_value": "2020-09-04 09:16:03",
      "value": "2020-09-04 16:16:03",
      "display_value_internal": "2020-09-04 09:16:03"
    },
    "name": {
      "display_value": "Emergency",
      "value": "Emergency"
    },
    "sys_name": {
      "display_value": "Emergency",
      "value": "Emergency"
    },
    "sys_created_by": {
      "display_value": "admin",
      "value": "admin"
    }
  }
}
```

## Change Management - GET /sn\_chg\_rest/change/normal

Retrieves one or more normal change requests based on the specified criteria.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/normal`

Default URL: `/api/sn_chg_rest/change/normal`

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

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Name-value pairs to use to filter the result set. The name is the field on which the specified value is filtered. This parameter is mutually exclusive with **sysparm\_query**. For example, instead of using `&sysparm_query=active=true`, you can simplify the calling statement by using `&active=true`. You can also use the display value when the field is a choice or reference type field, such as `&state=closed` instead of `&state=7`. To specify multiple key-value pairs, separate each with an ampersand, such as `&active=true&assigned_to=john.smith`. Data type: String

</td></tr><tr><td>

order

</td><td>

Field by which to sort the returned change requests. Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. Data type: Number

Default: 500

</td></tr><tr><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td>

[Encoded query](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) used to filter the result set. You can use a UI filter to obtain a properly encoded query.Syntax: `sysparm_query=<col_name><operator><value>`. Column names, operators, and values are case-sensitive.

-   &lt;col\_name&gt;: Name of the table column to filter on.
-   &lt;operator&gt;: Supports the following values:
    -   `=`: &lt;col\_name&gt; exactly matches &lt;value&gt;.
    -   `!=`: &lt;col\_name&gt; does not match &lt;value&gt;.
    -   `LIKE`: &lt;col\_name&gt; contains the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `STARTSWITH`: &lt;col\_name&gt; starts with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `ENDSWITH`: &lt;col\_name&gt; ends with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `^`: AND operator to add an additional query condition. Records included in the result set match both conditions.
    -   `^OR`: OR operator to add an additional query condition. Records included in the result set match at least one of the conditions.
-   &lt;value&gt;: Value to filter on.

For more information about operators, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Queries can contain multiple conditions. For example, the following query returns records where the caller is the current user and the record is active.

`sysparm_query=caller_id=javascript:gs.getUserID()^active=true`

Encoded queries also support order by ascending and descending functionality. To sort responses based on certain fields, use the `ORDERBY` and `ORDERBYDESC` clauses in **sysparm\_query**.

Syntax:

-   `ORDERBY<col_name>`
-   `ORDERBYDESC<col_name>`

For example, the following query gets all active records and orders the results in ascending order by number, and then in descending order by category.

`sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory`

By default, if part of a query is invalid, such as an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. Set the property **glide.invalid\_query.returns\_no\_rows** to `true` to instead return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

</td></tr><tr><td>

textSearch

</td><td>

String to use to search all normal change request record fields. This search uses ServiceNow full text search platform functionality and defaults to `IR_AND_OR_QUERY`.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Values for all fields in the associated change request.Data type: Object

</td></tr><tr><td>

state

</td><td>

State of the change request prior to the delete.Data type: Object

```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in a UI.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id information for the change request.Data type: Object

```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the change request to display in a UI.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the change request.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of change request.Data type: Object

```
type: {
  display_value: "String",
  value: "String"
}
```

</td></tr><tr><td>

type.display\_value

</td><td>

Change type to display in a UI.Value is always "Normal".

Data type: String

</td></tr><tr><td>

type.value

</td><td>

Internal type value.Value is always "normal".

Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/normal?sysparm_query=active=true^ORDERBYnumber" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  result: [
    {
      sys_id: {
        value: "1c87925347c12200e0ef563dbb9a7177",
        display_value: "1c87925347c12200e0ef563dbb9a7177"
      },
      state: {
        value: "-5", 
        display_value: "New"
      },
      type: {
        value: "normal",
        display_value: "Normal"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Add network switch to cabinet",
        display_value: "Add network switch to cabinet"
      },
    },
    { // next record found }, ... // and so on
  ]
}
```

## Change Management - GET /sn\_chg\_rest/change/normal/\{sys\_id\}

Retrieves the normal change request identified by the specified sys\_id.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/normal/{sys_id}`

Default URL: `/api/sn_chg_rest/change/normal/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the normal change request to retrieve.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Values for all fields in the associated change request.Data type: Object

</td></tr><tr><td>

state

</td><td>

State of the change request prior to the delete.Data type: Object

```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in a UI.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the change request.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of change request.Data type: Object

```
type: {
  display_value: "String",
  value: "String"
}
```

</td></tr><tr><td>

type.display\_value

</td><td>

Change type to display in a UI.Value is always "Normal".

Data type: String

</td></tr><tr><td>

type.value

</td><td>

Internal type value.Value is always "normal".

Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/normal/b0dbda5347c12200e0ef563dbb9a718f" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  result: [
    {
      sys_id: "b0dbda5347c12200e0ef563dbb9a718f",
      state: {
        value: "-5", 
        display_value: "New"
      },
      type: {
        value: "normal",
        display_value: "Normal"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Add network switch to cabinet",
        display_value: "Add network switch to cabinet"
      },
    },
  ]
}
```

## Change Management - GET /sn\_chg\_rest/change/standard

Retrieves one or more standard change requests based on the specified criteria.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/standard`

Default URL: `/api/sn_chg_rest/change/standard`

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

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Name-value pairs to use to filter the result set. The name is the field on which the specified value is filtered. This parameter is mutually exclusive with **sysparm\_query**. For example, instead of using `&sysparm_query=active=true`, you can simplify the calling statement by using `&active=true`. You can also use the display value when the field is a choice or reference type field, such as `&state=closed` instead of `&state=7`. To specify multiple key-value pairs, separate each with an ampersand, such as `&active=true&assigned_to=john.smith`. Data type: String

</td></tr><tr><td>

order

</td><td>

Field by which to sort the returned change requests. Data type: String

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. Data type: String

 Default: 500

</td></tr><tr><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td>

[Encoded query](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) used to filter the result set. You can use a UI filter to obtain a properly encoded query.Syntax: `sysparm_query=<col_name><operator><value>`. Column names, operators, and values are case-sensitive.

-   &lt;col\_name&gt;: Name of the table column to filter on.
-   &lt;operator&gt;: Supports the following values:
    -   `=`: &lt;col\_name&gt; exactly matches &lt;value&gt;.
    -   `!=`: &lt;col\_name&gt; does not match &lt;value&gt;.
    -   `LIKE`: &lt;col\_name&gt; contains the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `STARTSWITH`: &lt;col\_name&gt; starts with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `ENDSWITH`: &lt;col\_name&gt; ends with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `^`: AND operator to add an additional query condition. Records included in the result set match both conditions.
    -   `^OR`: OR operator to add an additional query condition. Records included in the result set match at least one of the conditions.
-   &lt;value&gt;: Value to filter on.

For more information about operators, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Queries can contain multiple conditions. For example, the following query returns records where the caller is the current user and the record is active.

`sysparm_query=caller_id=javascript:gs.getUserID()^active=true`

Encoded queries also support order by ascending and descending functionality. To sort responses based on certain fields, use the `ORDERBY` and `ORDERBYDESC` clauses in **sysparm\_query**.

Syntax:

-   `ORDERBY<col_name>`
-   `ORDERBYDESC<col_name>`

For example, the following query gets all active records and orders the results in ascending order by number, and then in descending order by category.

`sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory`

By default, if part of a query is invalid, such as an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. Set the property **glide.invalid\_query.returns\_no\_rows** to `true` to instead return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

</td></tr><tr><td>

textSearch

</td><td>

String to use to search all standard change request record fields. This search uses ServiceNow full text search platform functionality and defaults to `IR_AND_OR_QUERY`.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

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
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

All fields \(key\) with their associated values for the identified change request.Data type: Object

</td></tr><tr><td>

state

</td><td>

State of the change request prior to the delete.Data type: Object

 ```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in a UI.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id information for the change request.Data type: Object

 ```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the change request to display in a UI.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the change request.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of change request.Data type: Object

 ```
type: {
  display_value: "String",
  value: "String"
}
```

</td></tr><tr><td>

type.display\_value

</td><td>

Change type to display in a UI.Value is always "Standard".

 Data type: String

</td></tr><tr><td>

type.value

</td><td>

Internal type value.Value is always "standard".

 Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.service-now.com/api/sn_chg_rest/v1/change/standard?sysparm_query=active=true^ORDERBYnumber" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  result: [
    {
      sys_id: {
        value: "1c87925347c12200e0ef563dbb9a7177",
        display_value: "1c87925347c12200e0ef563dbb9a7177"
      },
      state: {
        value: "-5", 
        display_value: "New"
      },
      type: {
        value: "standard",
        display_value: "Standard"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Add network switch to cabinet",
        display_value: "Add network switch to cabinet"
      },
    }, 
    { // next record found }, ... // and so on
  ]
}
```

## Change Management - GET /sn\_chg\_rest/change/standard/\{sys\_id\}

Retrieves the standard change request identified by the specified sys\_id.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/standard/{sys_id}`

Default URL: `/api/sn_chg_rest/change/standard/{sys_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table id="table_cgs_31k_xlb" class="rest_api_request_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the standard change request to retrieve.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_ubj_gbk_xlb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table id="table_mc1_pr1_tx"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

All fields \(key\) with their associated values for the identified change request.Data type: Object

</td></tr><tr><td>

state

</td><td>

State of the change request prior to the delete.Data type: Object

```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in a UI.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id information for the change request.Data type: Object

```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the change request to display in a UI.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the change request.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://https://instance.servicenow.com/api/sn_chg_rest/v1/change/standard/b0dbda5347c12200e0ef563dbb9a718f" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  result: [
    {
      sys_id: {
        value: "1c87925347c12200e0ef563dbb9a7177",
        display_value: "1c87925347c12200e0ef563dbb9a7177"
      },
      state: {
        value: "-5", 
        display_value: "New"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Add network switch to cabinet",
        display_value: "Add network switch to cabinet"
      },
    }, 
  ]
}
```

## Change Management - GET /sn\_chg\_rest/change/standard/template

Retrieves one or more standard change templates based on the specified criteria.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/standard/template`

Default URL: `/api/sn_chg_rest/change/standard/template`

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

</td></tr></tbody>
</table><table id="table_gdg_b4l_xlb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Name-value pairs to use to filter the result set. The name is the field on which the specified value is filtered. This parameter is mutually exclusive with **sysparm\_query**. For example, instead of using `&sysparm_query=active=true`, you can simplify the calling statement by using `&active=true`. You can also use the display value when the field is a choice or reference type field, such as `&state=closed` instead of `&state=7`. To specify multiple key-value pairs, separate each with an ampersand, such as `&active=true&assigned_to=john.smith`. Data type: String

</td></tr><tr><td>

order

</td><td>

Field by which to sort the returned standard change templates. Data type: String

Default: Number

</td></tr><tr><td>

sysparm\_limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **sysparm\_offset** parameter to paginate record retrieval. Data type: Number

Default: 500

</td></tr><tr><td>

sysparm\_offset

</td><td>

Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks. For example, the first time you call this endpoint, **sysparm\_offset** is set to "0". To simply page through all available records, use `sysparm_offset=sysparm_offset+sysparm_limit`, until you reach the end of all records.

Don't pass a negative number in the **sysparm\_offset** parameter.Data type: Number

Default: 0

</td></tr><tr><td>

sysparm\_query

</td><td>

[Encoded query](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) used to filter the result set. You can use a UI filter to obtain a properly encoded query.Syntax: `sysparm_query=<col_name><operator><value>`. Column names, operators, and values are case-sensitive.

-   &lt;col\_name&gt;: Name of the table column to filter on.
-   &lt;operator&gt;: Supports the following values:
    -   `=`: &lt;col\_name&gt; exactly matches &lt;value&gt;.
    -   `!=`: &lt;col\_name&gt; does not match &lt;value&gt;.
    -   `LIKE`: &lt;col\_name&gt; contains the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `STARTSWITH`: &lt;col\_name&gt; starts with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `ENDSWITH`: &lt;col\_name&gt; ends with the specified string &lt;value&gt;. Only works for &lt;col\_name&gt; fields whose data type is string.
    -   `^`: AND operator to add an additional query condition. Records included in the result set match both conditions.
    -   `^OR`: OR operator to add an additional query condition. Records included in the result set match at least one of the conditions.
-   &lt;value&gt;: Value to filter on.

For more information about operators, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

Queries can contain multiple conditions. For example, the following query returns records where the caller is the current user and the record is active.

`sysparm_query=caller_id=javascript:gs.getUserID()^active=true`

Encoded queries also support order by ascending and descending functionality. To sort responses based on certain fields, use the `ORDERBY` and `ORDERBYDESC` clauses in **sysparm\_query**.

Syntax:

-   `ORDERBY<col_name>`
-   `ORDERBYDESC<col_name>`

For example, the following query gets all active records and orders the results in ascending order by number, and then in descending order by category.

`sysparm_query=active=true^ORDERBYnumber^ORDERBYDESCcategory`

By default, if part of a query is invalid, such as an invalid field name, the instance ignores the invalid part. It then returns rows using only the valid portion of the query. Set the property **glide.invalid\_query.returns\_no\_rows** to `true` to instead return no rows on an invalid query.

**Note:** The **glide.invalid\_query.returns\_no\_rows** property controls the behavior of all queries across the instance, such as in lists, scripts \(GlideRecord.query\(\)\), and web service APIs.

Data type: String

</td></tr><tr><td>

textSearch

</td><td>

String to use to search all standard change request record fields. This search uses ServiceNow full text search platform functionality and defaults to `IR_AND_OR_QUERY`.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

All fields with their associated values for the identified standard change template.Data type: Object

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id information for the change request.Data type: Object

 ```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the change request to display in a UI.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the change request.Data type: String

</td></tr><tr><td>

template

</td><td>

Information about the standard change template.Data type: Object

 ```
template: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

template.display\_value

</td><td>

Template information to display in the UI.Data type: String

</td></tr><tr><td>

template.value

</td><td>

Template sys\_id.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/standard/template?sysparm_query=active=true^ORDERBYnumber" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  result: [
    {
      sys_id: {
        value: "92b8544047810200e90d87e8dee490b0",
        display_value: "92b8544047810200e90d87e8dee490b0"
      },
      template : {
        value: "1c8e02ec47410200e90d87e8dee49057", 
        display_value: "Add network switch to datacenter cabinet"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Standard change template to add network switch to cabinet",
        display_value: "Standard change template to add network switch to cabinet"
      },
    }, 
    { // next record found }, ... // and so on
  ]
}
```

## Change Management - GET /sn\_chg\_rest/change/standard/template/\{sys\_id\}

Retrieves the standard change template identified by the specified sys\_id.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/standard/template/{sys_id}`

Default URL: `/api/sn_chg_rest/change/standard/template/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the standard change template to retrieve.Data type: String

Table: Standard Change Template \[std\_change\_record\_producer\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

All fields with their associated values for the identified standard change template.Data type: Object

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the change request.Data type: String

</td></tr><tr><td>

template

</td><td>

Information about the standard change template.Data type: Object

```
template: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

template.display\_value

</td><td>

Template information to display in a UI.Data type: String

</td></tr><tr><td>

template.value

</td><td>

Template sys\_id.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/standard/template/92b8544047810200e90d87e8dee490b0" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  result: [
    {
      sys_id: "92b8544047810200e90d87e8dee490b0",
      template : {
        value: "1c8e02ec47410200e90d87e8dee49057", 
        display_value: "Add network switch to datacenter cabinet"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Standard change template to add network switch to cabinet",
        display_value: "Standard change template to add network switch to cabinet"
      },
    }, 
  ]
}

```

## Change Management - GET /sn\_chg\_rest/change/worker/\{sys\_id\}

Retrieves the current status, information, and errors for the specified asynchronous worker.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/worker/{sys_id}`

Default URL: `/api/sn_chg_rest/{change/worker/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the change management asynchronous worker.Data type: String

Table: Change Management Worker \[chg\_mgt\_worker\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

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
|404|Not Found. The specified record couldn't be found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table id="table_is2_n4s_jpb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

messages

</td><td>

Message information.Data type: Object

```
"messages": {
  "errorMessages": [Array],
  "infoMessages": [Array],
  "warningMessages": [Array]
}
```

</td></tr><tr><td>

messages.errorMessages

</td><td>

Error messages encountered while processing the request. For example: ```
Invalid CMDB_CI sys_id provided
```

Data type: Array

</td></tr><tr><td>

messages.infoMessages

</td><td>

Information messages encountered while processing the request. For example: ```
CMDB_CI sys_id already associated to provided.
```

Data type: Array

</td></tr><tr><td>

messages.warningMessages

</td><td>

Warning messages encountered while processing the request. For example: ```
Invalid CMDB_CI sys_id provided.
```

Data type: Array

</td></tr><tr><td>

payload

</td><td>

Unique payload provided when using a worker sys\_id from the successful response body of a scheduling endpoint.-   [GET /ci/\{cmdb\_ci\_sys\_id\}/schedule](change-management-api.md#)
-   [GET /sn\_chg\_rest/change/\{change\_sys\_id\}/schedule](change-management-api.md#)

```
"payload": {
  "spans": [Array]
}
```

Data type: Object

</td></tr><tr><td>

payload.spans

</td><td>

If a timespan is available within the duration provided in the schedule endpoint, the worker API lists the available time spans.```
"payload": {
  "spans": [
   {
    "end": {Object}, 
    "start": {Object}
   }
  ]
}
```

Data type: Array

</td></tr><tr><td>

payload.spans.start

</td><td>

```
"start": {
  "display_value": "String",
  "value": "String"
}
```

 Data type: Object

</td></tr><tr><td>

payload.spans.start.value

</td><td>

Date and time that the change request is planned to start implementation.Data type: String

</td></tr><tr><td>

payload.spans.start.display\_value

</td><td>

Displays the value of the change request start time.Time format: yyyy-mm-dd hh:mm:ss

Data type: String

</td></tr><tr><td>

payload.spans.end

</td><td>

```
"end": {
  "display_value": "String",
  "value": "String"
}
```

 Data type: Object

</td></tr><tr><td>

payload.spans.end.value

</td><td>

Date and time that the change request is planned for completion.Time format: yyyy-mm-dd hh:mm:ss

Data type: String

</td></tr><tr><td>

payload.spans.end.display\_value

</td><td>

Displays the value of the change request completion time.Data type: String

</td></tr><tr><td>

request

</td><td>

Original endpoint request.Data type: String

</td></tr><tr><td>

state

</td><td>

Information on the current state of the worker.Data type: Object

```
state: {
  display_value: "String", 
  value: Number
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

Display value of the state of the worker. These values directly correlate to the **state.value** parameter.Possible values:

-   Complete
-   Error
-   In-Progress
-   Waiting

Data type: String

</td></tr><tr><td>

state.value

</td><td>

Numeric value of the state of the worker.Possible values:

-   1
-   2
-   3
-   4

Data type: Number

</td></tr><tr><td>

type

</td><td>

Type of association between the CMDB CI and the change request. Data type: String

</td></tr><tr><td>

worker

</td><td>

Information about the associated worker.Data type: Object

```
"worker": {
  "link": "String",
  "sysId": "String"
}
```

</td></tr><tr><td>

worker.link

</td><td>

URL to retrieve the status of the associated worker and other worker pertinent information.Data type: String

</td></tr><tr><td>

worker.sysId

</td><td>

Sys\_id of the worker associated with the change request.Data type: String

</td></tr><tr><td>

&lt;other\_params&gt;

</td><td>

Other parameters that are process-specific, such as **ignored\_cmdb\_ci\_sys\_ids**.

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/worker/0644cd02dbec330084f07ffdbf9619c1" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": {
    "worker": {
      "sysId": "0644cd02dbec330084f07ffdbf9619c1",
      "link": "https://instance.service-now.com/api/sn_chg_rest/change/worker/0644cd02dbec330084f07ffdbf9619c1"
    },
    "request": "{\"task\":\"c286d61347c12200e0ef563dbb9a71df\"}",
    "state": {
      "value": 3,
      "display_value": "Complete"
    },
    "type": "impacted",
    "messages": {
      "errorMessages": [],
      "warningMessages": [],
      "infoMessages": []
    }
  }
}
```

## Change Management - PATCH /sn\_chg\_rest/change/\{sys\_id\}

Updates the change request identified by the specified sys\_id with the key-value pairs in the request body or URL.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{sys_id}`

Default URL: `/api/sn_chg_rest/change/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the change request to modify.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Name-value pairs representing the fields to update. Request body parameters override URL parameters. However, required parameters must be specified in the URL. Data type: String

</td></tr><tr><td>

encrypted\_fields

</td><td id="encrypted_fields-chgmng-entry">

List of comma-separated fields to encrypt. These fields are encrypted before they are stored in the associated record. When specified, the endpoint calls the GlideRecord setDisplayValue\(\) method, instead of calling the setValue\(\) method.Because of this, you can also use this parameter to pass display values for non-encrypted fields, such as reference or choice fields, instead of passing sys\_ids or values.

Data type: String

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Name-value pairs representing the field\(s\) to update in the associated change request. For example, to update the short description file, enter a name-value pair similar to the following: `--data "{\"short_description\": \"my short desc\" }" \`. Data type: String

</td></tr><tr><td>

encrypted\_fields

</td><td id="d3088e945">

List of comma-separated fields to encrypt. These fields are encrypted before they are stored in the associated record. When specified, the endpoint calls the GlideRecord setDisplayValue\(\) method, instead of calling the setValue\(\) method.Because of this, you can also use this parameter to pass display values for non-encrypted fields, such as reference or choice fields, instead of passing sys\_ids or values.

Data type: String

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

</td><td>

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Updated change request record. Each element in this object corresponds to a field in the record in the Change Request \[change\_request\] table.All elements contain **value** and **display\_value** name-value pairs. Some contain **display\_value\_internal** name-value pairs.

Data type: Object

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/b0dbda5347c12200e0ef563dbb9a718f" \
--request PATCH \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--data "{\"short_desription\": \"Reboot the server at 6 am\" }" \
--user "username":"password"
```

```
{
  "result":
    {
      "reason": {
        "display_value": "",
        "value": ""
      },
      "parent": {
        "display_value": "",
        "value": ""
      },
      "watch_list": {
        "display_value": "",
        "value": ""
       },
       "proposed_change": {
         "display_value": "",
         "value": ""
       },
       "upon_reject": {
         "display_value": "Cancel all future Tasks",
         "value": "cancel"
       },
       "sys_updated_on": {
         "display_value": "2015-07-06 11:59:27",
         "value": "2015-07-06 18:59:27",
         "display_value_internal": "2015-07-06 11:59:27"
      },
      "type": {
        "display_value": "Standard",
        "value": "standard"
      },
      "approval_history": {
        "display_value": "",
        "value": ""
      },
      "skills": {
        "display_value": "",
        "value": ""
      },
      "test_plan": {
        "display_value": "--Confirm that there are no monitoring alerts for the router",
        "value": "--Confirm that there are no monitoring alerts for the router"
      },
      "number": {
        "display_value": "CHG0000024",
        "value": "CHG0000024"
      },
      "is_bulk": {
        "display_value": "false",
        "value": false
      },
      "cab_delegate": {
        "display_value": "",
        "value": ""
      },
      "requested_by_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "ci_class": {
        "display_value": "cmdb_ci",
        "value": "cmdb_ci"
      },
      "state": {
        "display_value": "Closed",
        "value": 3.0
      },
      "sys_created_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "knowledge": {
        "display_value": "false",
        "value": false
      },
      "order": {
        "display_value": "",
        "value": ""
      },
      "phase": {
        "display_value": "Requested",
        "value": "requested"
      },
      "cmdb_ci": {
        "display_value": "",
        "value": ""
      },
      "delivery_plan": {
        "display_value": "",
        "value": ""
      },
      "impact": {
        "display_value": "3 - Low",
        "value": 3.0
      },
      "contract": {
        "display_value": "",
        "value": ""
      },
      "active": {
        "display_value": "false",
        "value": false
      },
      "work_notes_list": {
        "display_value": "",
        "value": ""
      },
      "priority": {
        "display_value": "4 - Low",
        "value": 4.0
      },
      "sys_domain_path": {
        "display_value": "/",
        "value": "/"
      },
      "cab_recommendation": {
        "display_value": "",
        "value": ""
      },
      "production_system": {
        "display_value": "false",
        "value": false
      },
      "rejection_goto": {
        "display_value": "",
        "value": ""
      },
      "review_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "requested_by": {
        "display_value": "System Administrator",
        "value": "6816f79cc0a8016401c5a33be04be441"
      },
      "business_duration": {
        "display_value": "",
        "value": ""
      },
      "group_list": {
        "display_value": "",
        "value": ""
      },
      "change_plan": {
        "display_value": "",
        "value": ""
      },
      "approval_set": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "wf_activity": {
        "display_value": "",
        "value": ""
      },
      "implementation_plan": {
        "display_value": "-- Place router into maintenance mode in the monitoring platform\r\n-- Logon to router through SSH\r\n-- Run the following command\r\n\r\nrouter(config-router)#router bgp 12345\r\nrouter(config-router)#neighbor {neighbor ip} soft-reconfig [inbound]\r\nrouter#clear ip bgp {neighbor ip} soft in\r\n\r\n-- Confirm the sessions have been cleared\r\n-- Place router back into operational mode in the monitoring platform",
        "value": "-- Place router into maintenance mode in the monitoring platform\r\n-- Logon to router through SSH\r\n-- Run the following command\r\n\r\nrouter(config-router)#router bgp 12345\r\nrouter(config-router)#neighbor {neighbor ip} soft-reconfig [inbound]\r\nrouter#clear ip bgp {neighbor ip} soft in\r\n\r\n-- Confirm the sessions have been cleared\r\n-- Place router back into operational mode in the monitoring platform"
      },
      "universal_request": {
        "display_value": "",
        "value": ""
      },
      "end_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "short_description": {
        "display_value": "Reboot the server at 6 am",
        "value": "Reboot the server at 6 am"
      },
      "correlation_display": {
        "display_value": "",
        "value": ""
      },
      "work_start": {
        "display_value": "2015-07-06 11:56:04",
        "value": "2015-07-06 18:56:04",
        "display_value_internal": "2015-07-06 11:56:04"
      },
      "delivery_task": {
        "display_value": "",
        "value": ""
      },
      "outside_maintenance_schedule": {
        "display_value": "false",
        "value": false
      },
      "additional_assignee_list": {
        "display_value": "",
        "value": ""
      },
      "std_change_producer_version": {
        "display_value": "Clear BGP sessions on a Cisco router - 1",
        "value": "16c2273c47010200e90d87e8dee49006"
      },
      "sys_class_name": {
        "display_value": "Change Request",
        "value": "change_request"
      },
      "service_offering": {
        "display_value": "",
        "value": ""
      },
      "closed_by": {
        "display_value": "System Administrator",
        "value": "6816f79cc0a8016401c5a33be04be441"
      },
      "follow_up": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "review_status": {
        "display_value": "",
        "value": ""
      },
      "reassignment_count": {
        "display_value": "2",
        "value": 2.0
      },
      "start_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "assigned_to": {
        "display_value": "",
        "value": ""
      },
      "variables": {
        "display_value": "variable_pool",
        "value": "variable_pool"
      },
      "sla_due": {
        "display_value": "UNKNOWN",
        "value": "",
        "display_value_internal": ""
      },
      "comments_and_work_notes": {
        "display_value": "",
        "value": ""
      },
      "escalation": {
        "display_value": "Normal",
        "value": 0.0
      },
      "upon_approval": {
        "display_value": "Proceed to Next Task",
        "value": "proceed"
      },
      "correlation_id": {
        "display_value": "",
        "value": ""
      },
      "made_sla": {
        "display_value": "true",
        "value": true
      },
      "backout_plan": {
        "display_value": "Due to the limited number of commands in the implementation plan it is not possible to backout the change.\r\n\r\nIf required you are authorized to reboot the router if BGP fails to work",
        "value": "Due to the limited number of commands in the implementation plan it is not possible to backout the change.\r\n\r\nIf required you are authorized to reboot the router if BGP fails to work"
      },
      "conflict_status": {
        "display_value": "Not Run",
        "value": "Not Run"
      },
      "task_effective_number": {
        "display_value": "CHG0000024",
        "value": "CHG0000024"
      },
      "sys_updated_by": {
        "display_value": "admin",
        "value": "admin"
      },
      "opened_by": {
        "display_value": "System Administrator",
        "value": "6816f79cc0a8016401c5a33be04be441"
      },
      "user_input": {
        "display_value": "",
        "value": ""
      },
      "sys_created_on": {
        "display_value": "2015-07-06 11:55:46",
        "value": "2015-07-06 18:55:46",
        "display_value_internal": "2015-07-06 11:55:46"
      },
      "on_hold_task": {
        "display_value": "",
        "value": ""
      },
      "sys_domain": {
        "display_value": "global",
        "value": "global"
      },
      "route_reason": {
        "display_value": "",
        "value": ""
      },
      "closed_at": {
        "display_value": "2015-07-06 11:56:23",
        "value": "2015-07-06 18:56:23",
        "display_value_internal": "2015-07-06 11:56:23"
      },
      "review_comments": {
        "display_value": "",
        "value": ""
      },
      "business_service": {
        "display_value": "",
        "value": ""
      },
      "time_worked": {
        "display_value": "",
        "value": ""
      },
      "chg_model": {
        "display_value": "",
        "value": ""
      },
      "expected_start": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "opened_at": {
        "display_value": "2015-06-09 11:55:46",
        "value": "2015-06-09 18:55:46",
        "display_value_internal": "2015-06-09 11:55:46"
      },
      "work_end": {
        "display_value": "2015-07-06 11:56:10",
        "value": "2015-07-06 18:56:10",
        "display_value_internal": "2015-07-06 11:56:10"
      },
      "phase_state": {
        "display_value": "Open",
        "value": "open"
      },
      "cab_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "work_notes": {
        "display_value": "",
        "value": ""
      },
      "close_code": {
        "display_value": "Successful",
        "value": "successful"
      },
      "assignment_group": {
        "display_value": "Network",
        "value": "287ebd7da9fe198100f92cc8d1d2154e"
      },
      "description": {
        "display_value": "Resend the complete BGP table to neighboring routers\r\n\r\n--Both neighbors need to support soft reset route refresh capability.\r\n--Stores complete BGP table of you neighbor in router memory.\r\n--Not a good idea on a peering router with full feed, due to the memory requirements.\r\n",
        "value": "Resend the complete BGP table to neighboring routers\r\n\r\n--Both neighbors need to support soft reset route refresh capability.\r\n--Stores complete BGP table of you neighbor in router memory.\r\n--Not a good idea on a peering router with full feed, due to the memory requirements.\r\n"
      },
      "on_hold_reason": {
        "display_value": "",
        "value": ""
      },
      "calendar_duration": {
        "display_value": "",
        "value": ""
      },
      "close_notes": {
        "display_value": "Completed without issues",
        "value": "Completed without issues"
      },
      "sys_id": {
        "display_value": "b0dbda5347c12200e0ef563dbb9a718f",
        "value": "b0dbda5347c12200e0ef563dbb9a718f"
      },
      "contact_type": {
        "display_value": "Phone",
        "value": "phone"
      },
      "cab_required": {
        "display_value": "false",
        "value": false
      },
      "urgency": {
        "display_value": "3 - Low",
        "value": 3.0
      },
      "scope": {
        "display_value": "Medium",
        "value": 3.0
      },
      "company": {
        "display_value": "",
        "value": ""
      },
      "justification": {
        "display_value": "",
        "value": ""
      },
      "activity_due": {
        "display_value": "UNKNOWN",
        "value": "",
        "display_value_internal": ""
      },
      "comments": {
        "display_value": "",
        "value": ""
      },
      "approval": {
        "display_value": "Approved",
        "value": "approved"
      },
      "due_date": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "sys_mod_count": {
        "display_value": "10",
        "value": 10.0
      },
      "on_hold": {
        "display_value": "false",
        "value": false
      },
      "sys_tags": {
        "display_value": "",
        "value": ""
      },
      "conflict_last_run": {
        "display_value": "",
        "value": "",
        "display_value_internal": ""
      },
      "risk_value": {
        "display_value": "",
        "value": ""
      },
      "unauthorized": {
        "display_value": "false",
        "value": false
      },
      "risk": {
        "display_value": "Moderate",
        "value": 3.0
      },
      "location": {
        "display_value": "",
        "value": ""
      },
      "category": {
        "display_value": "Other",
        "value": "Other"
      },
      "risk_impact_analysis": {
        "display_value": "",
        "value": ""
      }
    }
}
```

### cURL request

The following example shows how to pass encrypted fields in the request body.

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/b0dbda5347c12200e0ef563dbb9a718f" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"encrypted_fields\":\"short_description,description\",
    \"short_description\":\"my short desc\",
    \"description\":\"my desc\"
}" \
--user "username":"password"
```

### cURL request

The following example shows how to pass encrypted fields as query parameters.

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/b0dbda5347c12200e0ef563dbb9a718f?encrypted_fields=short_description%2Cdescription&short_description=my%20short%20desc&description=my%20desc" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{}" \
--user "username":"password"
```

## Change Management - PATCH /sn\_chg\_rest/change/\{sys\_id\}/approvals

Allows the current user to approve or reject a change request approval record for the specified change request.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{sys_id}/approvals`

Default URL: `/api/sn_chg_rest/change/{sys_id}/approvals`

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

sys\_id

</td><td>

Sys\_id of the change request for which the approval/rejection applies.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

comments

</td><td>

Required if **state** is `rejected`. Reason that the change was rejected.Data type: String

</td></tr><tr><td>

state

</td><td>

Required. Approval state. For example: `--data "{\"state\": \"approved\"}"`

Valid values:

-   approved
-   rejected

Data type: String

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

</td><td>

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
|400|Bad request. Indicates a bad request type such as the user not having the authority to approve or reject the change request.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Values for all fields in the associated change request.Data type: Object

</td></tr><tr><td>

state

</td><td>

Current state of the change request.Data type: Object

```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in a UI.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the change request being approved/rejected.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of change request.Data type: Object

```
type: {
  display_value: "String",
  value: "String"
}
```

</td></tr><tr><td>

type.display\_value

</td><td>

Change type to display in a UI.Possible values:

-   Emergency
-   Normal
-   Standard

Data type: String

</td></tr><tr><td>

type.value

</td><td>

Internal type value.Possible values:

-   emergency
-   normal
-   standard

Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/0f4ac6c4b750230096c3e4f6ee11a9fe/approvals" \
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--data "{\"state\": \"approved\"}" \
--user "username":"password"

```

```
{
  result: [
    {
      sys_id: "0f4ac6c4b750230096c3e4f6ee11a9fe",
      state: {
        value: "-2", 
        display_value: "Scheduled"
      },
      type: {
        value: "normal",
        display_value: "Normal"
      },
      ..., // all valid fields in record, single parameter example below
      short_description: {
        value: "Remove server",
        display_value: "Remove server"
      }
    }
  ]
}
```

## Change Management - PATCH /sn\_chg\_rest/change/\{change\_sys\_id\}/schedule/first\_available

Updates the planned start and end times of a change request using the first available time slot found.

Role required: sn\_change\_writer.

**Note:** Use the link provided in the response body **worker.link** property to view the schedule status.

See also:

-   [GET /sn\_chg\_rest/change/ci/\{cmdb\_ci\_sys\_id\}/schedule](change-management-api.md#)
-   [GET /sn\_chg\_rest/change/\{change\_sys\_id\}/schedule](change-management-api.md#)

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{change_sys_id}/schedule/first_available`

Default URL: `/api/sn_chg_rest/change/{change_sys_id}/schedule/first_available`

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

change\_sys\_id

</td><td>

Sys\_id of the change request on which to update with the next available time slot. The selected change request must have a configuration item \(cmdb\_ci\).Data type: String

Table: Change Requests \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

duration\_in\_seconds

</td><td>

Duration of change in seconds, that is, how much time is required to complete the change request task.Data type: Integer

</td></tr><tr><td>

planned\_start\_time

</td><td>

Optional. Date and time that the change request is planned to start implementation in UTC.Retrieve the available time slot start at or later than this time. If not provided, the system uses the current time as the start time.

Format: yyyy-mm-dd hh:mm:ss

Data type: String

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

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

202

</td><td>

System accepted the request.

</td></tr><tr><td>

400

</td><td>

Bad Request. A bad request type or malformed request was detected. Possible issues:

-   The duration\_in\_seconds body parameter value is invalid or was not provided.
-   Invalid planned\_start\_time body parameter value provided.
-   The specified change request doesn't have an associated configuration item \(cmdb\_ci\).
-   User doesn't have read access to the fields of the change request.

</td></tr><tr><td>

403

</td><td>

Forbidden. User does not have write access to the planned start and end date values of the change request.

</td></tr><tr><td>

404

</td><td>

Not Found. The specified record couldn't be found. Possible issues:

-   System can't find the change request based on information provided.
-   User doesn't have read access to the record.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_is2_n4s_jpb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="row-result-error-cmdb"><td>

error

</td><td>

Information on any errors encountered while processing the endpoint request. Data type: Object

```
"error": {
  "detail": "String",
  "message": "String",
  "status": "String"
}
```

</td></tr><tr id="row-result-error_detail-cmdb"><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr id="row-result-error_message-cmdb"><td>

error.message

</td><td>

Message that identifies the error.Data type: String

</td></tr><tr><td>

messages

</td><td>

Message information.Data type: Object

```
"messages": {
  "errorMessages": [Array],
  "infoMessages": [Array],
  "warningMessages": [Array]
}
```

</td></tr><tr><td>

messages.errorMessages

</td><td>

Error messages encountered while processing the request. Data type: Array

</td></tr><tr><td>

messages.infoMessages

</td><td>

Information messages encountered while processing the request. Data type: Array

</td></tr><tr><td>

messages.warningMessages

</td><td>

Warning messages encountered while processing the request. Data type: Array

</td></tr><tr><td>

request

</td><td>

Original endpoint request.Data type: String

</td></tr><tr><td>

state

</td><td>

Information on the current state of the worker.Data type: Object

```
state: {
  display_value: "String", 
  value: Number
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

Display value of the state of the worker. These values directly correlate to the **state.value** parameter.Possible values:

-   Complete
-   Error
-   In-Progress
-   Waiting

Data type: String

</td></tr><tr><td>

state.value

</td><td>

Numeric value of the state of the worker.Possible values:

-   1
-   2
-   3
-   4

Data type: Number

</td></tr><tr><td>

type

</td><td>

Type of request.Valid value: schedule

Data type: String

</td></tr><tr><td>

worker

</td><td>

Information about the associated worker.Data type: Object

```
"worker": {
  "link": "String",
  "sysId": "String"
}
```

</td></tr><tr><td>

worker.link

</td><td>

Link for retrieving change request schedule status. Use the sys\_id in [GET /sn\_chg\_rest/change/worker/\{sys\_id\}](change-management-api.md#) to view results.Data type: String

</td></tr><tr><td>

worker.sysId

</td><td>

Sys\_id of the worker associated with the change request.Data type: String

</td></tr><tr><td>

status

</td><td>

Only appears if an error is encountered. Status of the endpoint processing.Possible value: failure

Data type: String

</td></tr></tbody>
</table>### Get change request schedule status

Use the value provided in the **worker.link** to determine if the change record has been successfully scheduled for the first available time slot. The value is in the following format:

`https://instance.service-now.com/api/sn_chg_rest/change/worker/<worker_sys_id>`

Use the worker.link details to run the provided sys\_id in [GET /sn\_chg\_rest/change/worker/\{sys\_id\}](change-management-api.md#) to view results.

The response body contains the status and provides results when processing is complete.

If an available time slot is found, the system updates the change request with the first available slot. When the state is complete, the **messages.infoMessages** reveals that the first available time slot has been set.

One of the following scheduling response values for **messages.infoMessages** are provided in the response body:

-   `Change has been updated` – Change requested has been updated for time slot.
-   `No slots found for <number> days from now` – No time slots available for change request duration provided within the number of days defined in the schedule window.

    **Note:** The change request scheduling time slot default value is 90 days. To change this value, modify the **change.conflict.next\_available.schedule\_window** property. For more information, see [Configure conflict analysis properties](https://www.servicenow.com/docs/access?context=configure-conflict-properties&version=australia&pubname=australia-it-service-management&ft:locale=en-US).


The following GET /sn\_chg\_rest/change/worker/\{sys\_id\} example shows output provided using the ID provided in the worker.link detail. The results indicate that processing is complete and the change request has been updated with the first available time slot.

```
{
  "result": {
    "worker": {
      "sysId": "355c62e0a4c87010f87712198fe9cacf",
      "link": "https://instance.service-now.com/api/sn_chg_rest/change/worker/355c62e0a4c87010f87712198fe9cacf"
    },
    "request": "{\"change_sys_id\":\"87ae5e900a0a2c3e263e8304e727c646\",\"duration_in_seconds\":10800,\"timezone\":\"America/Los_Angeles\"}",
    "state": {
      "value": 3,
      "display_value": "Complete"
    },
    "type": "schedule",
    "messages": {
      "errorMessages": [],
      "warningMessages": [],
      "infoMessages": [
        "Change has been updated"
      ]
    }
  }
}
```

### cURL request

```
curl "https://instance.service-now.com/api/sn_chg_rest/change/87ae5e900a0a2c3e263e8304e727c646/schedule/first_available" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"duration_in_seconds\":\"10800\"}" \
--user "username":"password"

```

Results include worker.link details you can use to run the provided sys\_id in the GET /sn\_chg\_rest/change/worker/ endpoint.

```
{
  "result": {
    "worker": {
      "sysId": "355c62e0a4c87010f87712198fe9cacf",
      "link": "https://instance.service-now.com/api/sn_chg_rest/change/worker/355c62e0a4c87010f87712198fe9cacf"
    },
    "request": "{\"change_sys_id\":\"87ae5e900a0a2c3e263e8304e727c646\",\"duration_in_seconds\":10800,\"timezone\":\"America/Los_Angeles\"}",
    "state": {
      "value": 1,
      "display_value": "Waiting"
    },
    "type": "schedule",
    "messages": {
      "errorMessages": [],
      "warningMessages": [],
      "infoMessages": []
    }
  }
}
```

## Change Management - PATCH /sn\_chg\_rest/change/\{change\_sys\_id\}/task/\{task\_sys\_id\}

Updates the change request task identified by the specified sys\_ids with the key-value pairs in the request body or the URL.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{change_sys_id}/task/{task_sys_id}`

Default URL: `/api/sn_chg_rest/change/{change_sys_id}/task/{task_sys_id}`

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

change\_sys\_id

</td><td>

Sys\_id of the change request to which the task is associated. Verifies whether the specified task is associated with the specified change request.Data type: String

Table: Change Request \[change\_request\]

</td></tr><tr><td>

task\_sys\_id

</td><td>

Sys\_id of the task to modify.Data type: String

Table: Change Task \[change\_task\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

key-value pairs

</td><td>

Name-value pairs representing the fields to update. Request body parameters override URL parameters. However, required parameters must be specified in the URL. Data type: String

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Name-value pairs representing the field\(s\) to update in the associated change request. For example, to update the short description file, enter a name-value pair similar to the following: `--data "{\"short_description\": \"my short desc\" }" \`. Data type: String

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

</td><td>

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
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

All fields \(key\) with their associated values for the identified change request task prior to the delete.Data type: Object

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id information for the change request task.Data type: Object

```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the change request task to display in a UI.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the change request task.Data type: String

</td></tr><tr><td>

parent

</td><td>

Unique identifier information for the change request associated to this task.Data type: Object

```
parent: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

parent.display\_value

</td><td>

Task information to display in a UI.Data type: String

</td></tr><tr><td>

parent.value

</td><td>

Sys\_id of the parent task.Data type: String

</td></tr><tr><td>

\_\_meta.ignoredFields

</td><td>

Key-value pairs that were passed in the call, but weren't applied to the change request as they either don't exist in the base record or the fields are read-only. Data type: Array

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/0f4ac6c4b750230096c3e4f6ee11a9fe/task/12629ec4b750230096c3e4f6ee11a9d5?short_description=Retire both nodes" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type: application/json" \
--data "{\"state\": \"assess\", \"no_such_field\": \"this will be ignored\" }" \
--user "username":"password"
```

```
{
  result: [
    {
      sys_id: {
        value: "12629ec4b750230096c3e4f6ee11a9d5",
        display_value: "12629ec4b750230096c3e4f6ee11a9d5"
      },
      parent: {
        value: "0f4ac6c4b750230096c3e4f6ee11a9fe", 
        display_value: "CHG0033046 "
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Retire both nodes",
        display_value: "Retire both nodes"
      }
      __meta: {
        ignoredFields: ["no_such_field"]
      }
    }
  ]
}
```

## Change Management - PATCH /sn\_chg\_rest/change/emergency/\{sys\_id\}

Updates the emergency change request identified by the specified sys\_id with the key-value pairs in the request body or the URL.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/emergency/{sys_id}`

Default URL: `/api/sn_chg_rest/change/emergency/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the change request to modify.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Name-value pairs representing the fields to update. Request body parameters override URL parameters. However, required parameters must be specified in the URL. Data type: String

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Name-value pairs representing the field\(s\) to update in the associated change request. For example, to update the short description file, enter a name-value pair similar to the following: `--data "{\"short_description\": \"my short desc\" }" \`. Data type: String

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

</td><td>

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Values for all fields in the associated change request.Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the change request.Data type: Object

```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in a UI.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the change request.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of change request.Data type: Object

```
type: {
  display_value: "String",
  value: "String"
}
```

</td></tr><tr><td>

type.display\_value

</td><td>

Change type to display in a UI.Value is always "Emergency".

Data type: String

</td></tr><tr><td>

type.value

</td><td>

Internal type value.Value is always "emergency".

Data type: String

</td></tr><tr><td>

\_\_meta.ignoredFields

</td><td>

Name-value pairs that were passed in the call, but were not applied to the change request as they either do not exist in the base record or the fields are read-only.Data type: Array

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/emergency/b0dbda5347c12200e0ef563dbb9a718f" \
--request PATCH \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--data "{\"no_such_field\": \"this will be ignored\", }" \
--user "username":"password"
```

```
{
  result: [
    {
      sys_id: "b0dbda5347c12200e0ef563dbb9a718f",    },
      state: {
        value: "-4", 
        display_value: "Assess"
      },
      type: {
        value: "emergency",
        display_value: "Emergency"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Reboot server",
        display_value: "Reboot server"
      }
      __meta: {
        ignoredFields: ["no_such_field"]
      }
    }
  ]
}
```

## Change Management - PATCH /sn\_chg\_rest/change/normal/\{sys\_id\}

Updates the normal change request identified by the specified sys\_id with the parameters in the request body or the URL.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/normal/{sys_id}`

Default URL: `/api/sn_chg_rest/change/normal/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the change request to modify.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Name-value pairs representing the fields to update. Request body parameters override URL parameters. However, required parameters must be specified in the URL. Data type: String

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Name-value pairs representing the field\(s\) to update in the associated change request. For example, to update the short description file, enter a name-value pair similar to the following: `--data "{\"short_description\": \"my short desc\" }" \`. Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr id="accept-row-RESTAPI"><td>

Accept

</td><td>

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Values for all fields in the associated change request.Data type: Object

</td></tr><tr><td>

state

</td><td>

Current state of the change request.Data type: Object

```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in a UI.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the change request.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of change request.Data type: Object

```
type: {
  display_value: "String",
  value: "String"
}
```

</td></tr><tr><td>

type.display\_value

</td><td>

Change type to display in a UI.Value is always "Normal".

Data type: String

</td></tr><tr><td>

type.value

</td><td>

Internal type value.Value is always "normal".

Data type: String

</td></tr><tr><td>

\_\_meta.ignoredFields

</td><td>

Name-value pairs that were passed in the call, but were not applied to the change request as they either do not exist in the base record or the fields are read-only.Data type: Array

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/normal/b0dbda5347c12200e0ef563dbb9a718f?state=assess" \
--request PATCH \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--data "{\"state\": \"assess\", \"no_such_field\": \"this will be ignored\" }" \
--user "username":"password"

```

```
{
  result: [
    {
      sys_id: "b0dbda5347c12200e0ef563dbb9a718f",
      state: {
        value: "-4", 
        display_value: "Assess"
      },
      type: {
        value: "normal",
        display_value: "Normal"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Remove server",
        display_value: "Remove server"
      }
      __meta: {
        ignoredFields: ["no_such_field"]
      }
    }
  ]
}
```

## Change Management - PATCH /sn\_chg\_rest/change/standard/\{sys\_id\}

Updates the standard change request identified by the specified sys\_id with the parameters in the request body or in the URL.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/standard/{sys_id}`

Default URL: `/api/sn_chg_rest/change/standard/{sys_id}`

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

sys\_id

</td><td>

Sys\_id of the change request to modify.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Name-value pairs representing the fields to update. Request body parameters override URL parameters. However, required parameters must be specified in the URL. Data type: String

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

data

</td><td>

Name-value pairs representing the field\(s\) to update in the associated change request. For example, to update the short description file, enter a name-value pair similar to the following: `--data "{\"short_description\": \"my short desc\" }" \`. Data type: String

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

</td><td>

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

All fields \(key\) with their associated values for the identified change request.Data type: Object

</td></tr><tr><td>

state

</td><td>

State of the change request.Data type: Object

```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in a UI.Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id information for the change request.Data type: Object

```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the change request to disply in a UI.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the change request.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/standard/1c87925347c12200e0ef563dbb9a7177?description=Reboot my email server" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"short_description\": \"my short desc\" }" \
--user "username":"password"

```

```
{
  result: [
    {
      sys_id: {
        value: "1c87925347c12200e0ef563dbb9a7177",
        display_value: "1c87925347c12200e0ef563dbb9a7177"
      },
      state: {
        value: "-5", 
        display_value: "New"
      },

      ..., // all valid fields in record, example below
      short_description: {
        value: "Reboot my email server",
        display_value: "Reboot my email server"
      },
    } 
  ]
}
```

## Change Management - PATCH /sn\_chg\_rest/change/standard/\{sys\_id\}/risk

Calculates the risk and impact of the specified standard change based on an evaluation of the risk conditions.

If the Change Risk Assessment plugin is installed, it also calculates the cumulative highest risk once the risk assessment is complete.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{sys_id}/risk`

Default URL: `/api/sn_chg_rest/change/{sys_id}/risk`

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

sys\_id

</td><td>

Sys\_id of the standard change to evaluate.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Risk assessment completed successfully.|
|400|Risk assessment failed. Details of the type of failure are included in the error data.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

impact

</td><td>

Impact associated with the specified standard change.Data type: Object

```
impact: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

impact.display\_value

</td><td>

Impact information to display in a UI.Data type: String

</td></tr><tr><td>

impact.value

</td><td>

Internal impact value.Data type: String

</td></tr><tr><td>

name-value pairs

</td><td>

All valid fields within the standard change record.Data type: Object

</td></tr><tr><td>

risk

</td><td>

Risk calculated for the specified standard change.Data type: Object

```
risk: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

risk.display\_value

</td><td>

Risk information to display in a UI.Data type: String

</td></tr><tr><td>

risk.value

</td><td>

Internal risk value.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id information for the standard change request.Data type: Object

```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the change request to display in a UI.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the change request.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/1c87925347c12200e0ef563dbb9a7177/risk" \
--request PATCH \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  sys_id: {
    value: "1c87925347c12200e0ef563dbb9a7177",
    display_value: "1c87925347c12200e0ef563dbb9a7177"
  },
  risk: {
    value: "4", 
    display_value: "Low"
  },
  impact: {
    value: "3",
    display_value: "3 - Low"
  }
  ..., // all valid fields in record
}
```

## Change Management - POST /sn\_chg\_rest/change

Creates a change request record based on the change request. Creating multiple change requests within a single call isn’t supported.

You can obtain the list of available change models using the [Change Management - GET /sn\_chg\_rest/change/model](change-management-api.md#) or [Change Management - GET /sn\_chg\_rest/change/model/\{sys\_id\}](change-management-api.md#) endpoints.

When creating a change request, set the change model \(**chg\_model**\) or **type**. If both **chg\_model**and **type** are set, the type is simply a categorization of the change. Not providing at least one of these values results in a default setting that is subject to change by release. It is strongly advised to set at least one of these values.

Values can be set either as a query parameter or request body parameter.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change`

Default URL: `/api/sn_chg_rest/change`

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

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Name-value pairs representing the fields to update. Request body parameters override URL parameters. However, required parameters must be specified in the URL. The same values can be set as request body parameters instead.**Note:** When creating a change request, set the change model \(**chg\_model**\) or **type**. If both **chg\_model**and **type** are set, the type is simply a categorization of the change. Not providing at least one of these values results in a default setting that is subject to change by release. It is strongly advised to set at least one of these values.

Data type: String

</td></tr><tr><td>

chg\_model

</td><td>

Name of a change model listed in the Change Model \[chg\_model\] table. Provided in the following format: `chg_model=Normal`.

For more information, see [Change models](https://www.servicenow.com/docs/access?context=change-models&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

**Note:** Not providing either the change model \(**chg\_model**\) or **type** value results in a default setting that is subject to change by release. It is strongly advised to set at least one of these values.

Data type: String

</td></tr><tr><td>

encrypted\_fields

</td><td id="encrypted_fields-chgmng-entry">

List of comma-separated fields to encrypt. These fields are encrypted before they are stored in the associated record. When specified, the endpoint calls the GlideRecord setDisplayValue\(\) method, instead of calling the setValue\(\) method.Because of this, you can also use this parameter to pass display values for non-encrypted fields, such as reference or choice fields, instead of passing sys\_ids or values.

Data type: String

</td></tr><tr><td>

type

</td><td>

Name of the change request type listed in the Choices \[sys\_choice\] table. If the **chg\_model** is also populated, this field is only used as a change categorization. Provided in the following format: `type=Normal`.

For more information, see [Add a new change request type](https://www.servicenow.com/docs/access?context=t_AddNewChangeType&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

**Note:** Not providing either the change model \(**chg\_model**\) or **type** value results in a default setting that is subject to change by release. It is strongly advised to set at least one of these values.

Data type: String

</td></tr></tbody>
</table><table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Name-value pairs representing the field\(s\) to update in the associated change request. For example, to update the short description file, enter a name-value pair similar to the following: `--data "{\"short_description\": \"my short desc\" }" \`. The same properties can be set as query parameters instead.Data type: String

</td></tr><tr><td>

Object.chg\_model

</td><td>

Name of a change model listed in the Change Model \[chg\_model\] table. Provided as a name-value pair in the following format: `{"chg_model" : "Cloud Infrastructure"}`

For more information, see [Change models](https://www.servicenow.com/docs/access?context=change-models&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

**Note:** Not providing either the change model \(**chg\_model**\) or **type** value results in a default setting that is subject to change by release. It is strongly advised to set at least one of these values.

Data type: String

</td></tr><tr><td>

Object.encrypted\_fields

</td><td>

List of comma-separated fields to encrypt. These fields are encrypted before they are stored in the associated record. When specified, the endpoint calls the GlideRecord setDisplayValue\(\) method, instead of calling the setValue\(\) method.Because of this, you can also use this parameter to pass display values for non-encrypted fields, such as reference or choice fields, instead of passing sys\_ids or values.

Data type: String

</td></tr><tr><td>

Object.type

</td><td>

Name of the change request type listed in the Choices \[sys\_choice\] table. If the **chg\_model** is also populated, this field is only used as a change categorization. Provided as a name-value pair in the following format: `{"type" : "emergency"}`

For more information, see [Add a new change request type](https://www.servicenow.com/docs/access?context=t_AddNewChangeType&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

**Note:** Not providing either the change model \(**chg\_model**\) or **type** value results in a default setting that is subject to change by release. It is strongly advised to set at least one of these values.

Data type: String

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

</td><td>

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

New change request record. The elements of this object correspond to the record format in the Change Request \[change\_request\] table. All values that are not specified in the request are set to their defaults or are empty/null.Data type: Object

</td></tr></tbody>
</table>### cURL request

The following example shows how to create a change request record based on the Standard change model and Standard type. In this example, the Change Request is driven by the model and the type field is only used as a categorization.

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"chg_model\" : \"Standard\",
    \"description\" : \"Describes the change request.\",
    \"short_description\" : \"My change request\",
    \"type\" : \"Standard\"
}" \
--user "username":"password"
```

Results show that the record was successfully added to the Change Request \[change\_request\] table with the value `CHG0030022`.

```
{
  "result": 
    "upon_reject": {
      "display_value": "Cancel all future Tasks",
      "value": "cancel"
    },
    "sys_updated_on": {
      "display_value": "2022-12-08 17:18:57",
      "value": "2022-12-09 01:18:57",
      "display_value_internal": "2022-12-08 17:18:57"
    },
    "type": {
      "display_value": "Standard",
      "value": "standard"
    }
    "number": {
      "display_value": "CHG0030022",
      "value": "CHG0030022"
    },
    "is_bulk": {
      "display_value": "false",
      "value": false
    }
    "ci_class": {
      "display_value": "cmdb_ci",
      "value": "cmdb_ci"
    },
    "state": {
      "display_value": "New",
      "value": -5
    },
    "sys_created_by": {
      "display_value": "admin",
      "value": "admin"
    },
    "knowledge": {
      "display_value": "false",
      "value": false
    },
    "phase": {
      "display_value": "Requested",
      "value": "requested"
    }
    "impact": {
      "display_value": "3 - Low",
      "value": 3
    },
    "active": {
      "display_value": "true",
      "value": true
    },
    "priority": {
      "display_value": "4 - Low",
      "value": 4
    },
    "sys_domain_path": {
      "display_value": "/",
      "value": "/"
    },
    "production_system": {
      "display_value": "false",
      "value": false
    },
    "requested_by": {
      "display_value": "System Administrator",
      "value": "6816f79cc0a8016401c5a33be04be441"
    }
    "short_description": {
      "display_value": "My change request",
      "value": "My change request"
    },
    "sys_class_name": {
      "display_value": "Change Request",
      "value": "change_request"
    },
    "reassignment_count": {
      "display_value": "0",
      "value": 0
    },
    "variables": {
      "display_value": "variable_pool",
      "value": "variable_pool"
    },
    "sla_due": {
      "display_value": "UNKNOWN",
      "value": "",
      "display_value_internal": ""
    },
    "escalation": {
      "display_value": "Normal",
      "value": 0
    },
    "upon_approval": {
      "display_value": "Proceed to Next Task",
      "value": "proceed"
    },
    "conflict_status": {
      "display_value": "Not Run",
      "value": "Not Run"
    },
    "task_effective_number": {
      "display_value": "CHG0030022",
      "value": "CHG0030022"
    },
    "sys_updated_by": {
      "display_value": "admin",
      "value": "admin"
    },
    "opened_by": {
      "display_value": "System Administrator",
      "value": "6816f79cc0a8016401c5a33be04be441"
    },
    "sys_created_on": {
      "display_value": "2022-12-08 17:18:57",
      "value": "2022-12-09 01:18:57",
      "display_value_internal": "2022-12-08 17:18:57"
    },
    "sys_domain": {
      "display_value": "global",
      "value": "global"
    },
    "chg_model": {
      "display_value": "Standard",
      "value": "e55d0bfec343101035ae3f52c1d3ae49"
    },
    "opened_at": {
      "display_value": "2022-12-08 17:18:57",
      "value": "2022-12-09 01:18:57",
      "display_value_internal": "2022-12-08 17:18:57"
    },
    "description": {
      "display_value": "Describes the change request.",
      "value": "Describes the change request."
    },
    "sys_id": {
      "display_value": "2ac52dd77c6b1510f877be3b096e64fe",
      "value": "2ac52dd77c6b1510f877be3b096e64fe"
    },
    "cab_required": {
      "display_value": "false",
      "value": false
    },
    "urgency": {
      "display_value": "3 - Low",
      "value": 3
    },
    "scope": {
      "display_value": "Medium",
      "value": 3
    },
    "activity_due": {
      "display_value": "UNKNOWN",
      "value": "",
      "display_value_internal": ""
    },
    "approval": {
      "display_value": "Not Yet Requested",
      "value": "not requested"
    },
  }
}
```

### cURL request

The following example shows how to pass encrypted fields in the request body.

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"encrypted_fields\":\"short_description,description\",
    \"short_description\":\"my short desc\",
    \"description\":\"my desc\"
}" \
--user "username":"password"
```

### cURL request

The following example shows how to pass encrypted fields as query parameters.

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change?encrypted_fields=short_description%2Cdescription&short_description=my%20short%20desc&description=my%20desc" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{}" \
--user "username":"password"
```

## Change Management - POST /sn\_chg\_rest/change/\{sys\_id\}/ci

Creates the association between a change request and Configuration Management Database \(CMDB\) configuration items \(CI\).

The creation of the association is done asynchronously, which means that a response is provided immediately and contains details for the worker. The worker does the actual work after the response.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{sys_id}/ci`

Default URL: `/api/sn_chg_rest/change/{sys_id}/ci`

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

sys\_id

</td><td>

Sys\_id of the change request to associate with the CMDB CI.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

association\_type

</td><td>

Required. Type of association between the CMDB CI and the change request. Valid values:

 -   affected: CIs that are affected by the change request
-   impacted: Services impacted by the change request
-   offering: Impacted service offerings

 Data type: String

</td></tr><tr><td>

cmdb\_ci\_sys\_ids

</td><td>

Required. List of CMDB CI sys\_ids to associate to the change request.Data type: Array or comma-separated string

</td></tr><tr><td>

refresh\_impacted\_services

</td><td>

Flag used when `association_type=affected` to populate impacted services based on the list of affected CIs.Valid values:

 -   true: Populate impacted services based on the list of affected CIs
-   false: Do not automatically populate impacted services

 Data type: Boolean

 Default: false

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

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

202

</td><td>

Accepted. The request was accepted for processing.

</td></tr><tr><td>

400

</td><td>

Bad Request. A bad request type or malformed request was detected. The error response contains pertinent messages to help troubleshoot the problem.

</td></tr><tr><td>

401

</td><td id="entry-401-status-code">

Unauthorized. The user credentials are incorrect or have not been passed.

</td></tr><tr><td>

404

</td><td id="entry-404-status-code">

Not found. The requested item wasn't found.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

messages

</td><td>

Message information.Data type: Object

```
"messages": {
  "errorMessages": [Array],
  "infoMessages": [Array],
  "warningMessages": [Array]
}
```

</td></tr><tr><td>

messages.errorMessages

</td><td>

Error messages encountered while processing the request. For example: ```
Invalid CMDB_CI sys_id provided
```

 Data type: Array

</td></tr><tr><td>

messages.infoMessages

</td><td>

Information messages encountered while processing the request. For example: ```
CMDB_CI sys_id already associated to provided.
```

 Data type: Array

</td></tr><tr><td>

messages.warningMessages

</td><td>

Warning messages encountered while processing the request. For example: ```
Invalid CMDB_CI sys_id provided.
```

 Data type: Array

</td></tr><tr><td>

request

</td><td>

Original endpoint request.Data type: String

</td></tr><tr><td>

state

</td><td>

Information on the current state of the worker.```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

Display value of the state of the worker. These values directly correlate to the **state.value** element.Possible values:

 -   Complete
-   Error
-   In-Progress
-   Waiting

 Data type: String

</td></tr><tr><td>

state.value

</td><td>

Numeric value of the state of the worker.Possible values:

 -   1
-   2
-   3
-   4

 Data type: Number

</td></tr><tr><td>

type

</td><td>

Type of association between the CMDB CI and the change request. Data type: String

</td></tr><tr><td>

worker

</td><td>

Information about the associated worker.Data type: Object

 ```
"worker": {
  "link": "String",
  "sysId": "String"
}
```

</td></tr><tr><td>

worker.link

</td><td>

URL to retrieve the status of the associated worker and other worker pertinent information.Data type: String

</td></tr><tr><td>

worker.sysId

</td><td>

Sys\_id of the worker associated with the change request.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/c286d61347c12200e0ef563dbb9a71df/ci" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{cmdb_ci_sys_ids:'caf043a3b7fb23000999e4f6ee11a9c0,06f043a3b7fb23000999e4f6ee11a9c1', association_type:'affected'}" \
--user "username":"password"

```

```
{
  "result": {
    "worker": {
      "sysId": "f490f4c6dbac330084f07ffdbf961952",
      "link": "instance.service-now.com/api/sn_chg_rest/change/worker/f490f4c6dbac330084f07ffdbf961952"
    },
    "request": "{\"cmdb_ci_sys_ids\":[\"caf043a3b7fb23000999e4f6ee11a9c0\",\"06f043a3b7fb23000999e4f6ee11a9c1\"],\"association_type\":\"affected\",\"task\":\"c286d61347c12200e0ef563dbb9a71df\"}",
    "state": {
      "value": 1,
      "display_value": "Waiting"
    },
    "type": "affected",
    "messages": {
      "errorMessages": [],
      "warningMessages": [],
      "infoMessages": []
    }
  }
}
```

## Change Management - POST /sn\_chg\_rest/change/\{sys\_id\}/conflict

Starts a change request conflict checking process for the specified change request \(sys\_id\).

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{sys_id}/conflict`

Default URL: `/api/sn_chg_rest/change/{sys_id}/conflict`

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

sys\_id

</td><td>

Sys\_id of the change management request for which to start the conflict checking process. For additional information on the conflict checking process, see [Conflict detection](https://www.servicenow.com/docs/access?context=c_ConflictDetection&version=australia&pubname=australia-it-service-management&ft:locale=en-US).Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. Request was unable to start due to unresolvable errors. The returned message may provide additional details.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Sys\_id of the change request conflict checking process.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/0f4ac6c4b750230096c3e4f6ee11a9fe/conflict" \
--request POST \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
    result: "c0b5afe4b710230096c3e4f6ee11a93f"
}
```

## Change Management - POST /sn\_chg\_rest/change/emergency

Creates one emergency change request based on the default emergency change request record. Multiple emergency change request creations within a single call is not supported.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/emergency`

Default URL: `/api/sn_chg_rest/change/emergency`

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

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

key-value pairs

</td><td>

Key-value pairs of fields to modify when creating the request. The key is the field name within the template and the value is the information to populate in the field.Fields that cannot be modified and are ignored if passed in:

-   Business rules
-   Read-only fields as defined in ACLs
-   Fields that do not exist

 Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Name-value pairs of the fields that were created in the emergency change request.Data type: Object

</td></tr><tr><td>

state

</td><td>

State of the change request prior to the delete.Data type: Object

 ```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in a UI. Value is always "New".

 Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value. Value is always "-5".

 Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the newly created emergency change request.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of change request.Data type: Object

 ```
type: {
  display_value: "String",
  value: "String"
}
```

</td></tr><tr><td>

type.display\_value

</td><td>

Change type to display in a UI.Value is always "Emergency".

 Data type: String

</td></tr><tr><td>

type.value

</td><td>

Internal type value.Value is always "emergency".

 Data type: String

</td></tr><tr><td>

\_\_meta.ignoredFields

</td><td>

Key-value pairs that were passed in the call, but weren't applied to the change request as they either don't exist in the base record or the fields are read-only. Data type: Array

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/emergency?no_such_field=something&description=test&short_description=Reboot server" \
--request POST \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  result: [
    {
      sys_id: "b0dbda5347c12200e0ef563dbb9a718f",
      state: {
        value: "-5", 
        display_value: "New"
      },
      type: {
        value: "emergency",
        display_value: "Emergency"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Reboot server",
        display_value: "Reboot server"
      }
      __meta: {
        ignoredFields: ["no_such_field"]
      }
    }
  ]
}
```

## Change Management - POST /sn\_chg\_rest/change/normal

Creates one normal change request based on the default normal change request record. Multiple normal change request creations within a single call is not supported.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/normal`

Default URL: `/api/sn_chg_rest/change/normal`

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

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

key-value pairs

</td><td>

Fields to modify when creating the request. The key is the field name within the template and the value is the information to populate in the field.Fields that cannot be modified and are ignored if passed in:

-   Business rules
-   Read-only fields as defined in ACLs
-   Fields that do not exist

 Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Values for all fields in the associated change request.Data type: Object

</td></tr><tr><td>

state

</td><td>

State of the newly created change request.Data type: Object

 ```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

State to display in a UI. Value is always "New".

 Data type: String

</td></tr><tr><td>

state.value

</td><td>

Internal state value. Value is always "-5".

 Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the newly created normal change request.Data type: String

</td></tr><tr><td>

type

</td><td>

Type of change request.Data type: Object

 ```
type: {
  display_value: "String",
  value: "String"
}
```

</td></tr><tr><td>

type.display\_value

</td><td>

Change type to display in a UI.Value is always "Normal".

 Data type: String

</td></tr><tr><td>

type.value

</td><td>

Internal type value.Value is always "normal".

 Data type: String

</td></tr><tr><td>

\_\_meta.ignoredFields

</td><td>

Key-value pairs that were passed in the call, but weren't applied to the change request as they either don't exist in the base record or the fields are read-only. Data type: Array

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/normal?no_such_field=something&description=test&short_description=Remove server" \
--request POST \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  result: [
    {
      sys_id: "b0dbda5347c12200e0ef563dbb9a718f",
      state: {
        value: "-5", 
        display_value: "New"
      },
      type: {
        value: "normal",
        display_value: "Normal"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Remove server",
        display_value: "Remove server"
      }
      __meta: {
        ignoredFields: ["no_such_field"]
      }
    }
  ]
}
```

## Change Management - POST /sn\_chg\_rest/change/\{sys\_id\}/refresh\_impacted\_services

Populates the impacted services/configuration items \(CIs\) related list based on the primary CI.

The primary CI appears on the change request form and affected CI related list.

**Note:** All work items for this endpoint are performed asynchronously.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{sys_id}/refresh_impacted_services`

Default URL: `/api/sn_chg_rest/change/{sys_id}/refresh_impacted_services`

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

sys\_id

</td><td>

Sys\_id of the change request to use to refresh the impacted services.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

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
|404|Not Found. The specified record couldn't be found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

messages

</td><td>

Message information.Data type: Object

```
"messages": {
  "errorMessages": [Array],
  "infoMessages": [Array],
  "warningMessages": [Array]
}
```

</td></tr><tr><td>

messages.errorMessages

</td><td>

Error messages encountered while processing the request. For example: ```
Invalid CMDB_CI sys_id provided
```

 Data type: Array

</td></tr><tr><td>

messages.infoMessages

</td><td>

Information messages encountered while processing the request. For example: ```
CMDB_CI sys_id already associated to provided.
```

 Data type: Array

</td></tr><tr><td>

messages.warningMessages

</td><td>

Warning messages encountered while processing the request. For example: ```
Invalid CMDB_CI sys_id provided.
```

 Data type: Array

</td></tr><tr><td>

request

</td><td>

Original endpoint request.Data type: String

</td></tr><tr><td>

state

</td><td>

Information on the current state of the worker.Data type: Object

 ```
state: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

state.display\_value

</td><td>

Display value of the state of the worker. These values directly correlate to the **state.value** element.Possible values:

 -   Complete
-   Error
-   In-Progress
-   Waiting

 Data type: String

</td></tr><tr><td>

state.value

</td><td>

Numeric value of the state of the worker.Possible values:

 -   1
-   2
-   3
-   4

 Data type: Number

</td></tr><tr><td>

type

</td><td>

Type of association between the CMDB CI and the change request. Data type: String

</td></tr><tr><td>

worker

</td><td>

Information about the associated worker.Data type: Object

 ```
"worker": {
  "link": "String",
  "sysId": "String"
}
```

</td></tr><tr><td>

worker.link

</td><td>

URL to retrieve the status of the associated worker and other worker pertinent information.Data type: String

</td></tr><tr><td>

worker.sysId

</td><td>

Sys\_id of the worker associated with the change request.Data type: String

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/sn_chg_rest/v1/change/c286d61347c12200e0ef563dbb9a71df/refresh_impacted_services" \ 
--request POST \ 
--header "Accept:application/json" \
--header "Content-Type:application/json" \ 
--user "username":"password"
```

```
{ 
  result: { 
    worker: { 
      sysId: "aa31c308b75033000999e4f6ee11a9c2", 
      link: "http://instance.service-now.com/api/sn_chg_rest/change/worker/aa31c308b75033000999e4f6ee11a9c2" 
    }, 
    request: "", 
    state: { 
      value: 1, 
      display_value: "Waiting" 
    }, 
    type: "impacted", 
    messages: { 
      errorMessages: [], 
      warningMessages: [], 
      infoMessages: [] 
    } 
  } 
} 
```

## Change Management - POST /sn\_chg\_rest/change/standard/\{standard\_change\_template\_id\}

Creates one standard change request based on an existing standard change template as specified by the passed-in template sys\_id. Multiple standard change request creations within a single call is not supported.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/standard/{standard_change_template_id}`

Default URL: `/api/sn_chg_rest/change/standard/{standard_change_template_id}`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table id="table_o5l_xk2_xlb" class="rest_api_request_parameters"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

standard\_change\_template\_id

</td><td>

Sys\_id of the standard change template on which to base the new standard change request.Data type: String

Table: Standard Change Template \[std\_change\_record\_producer\]

</td></tr></tbody>
</table><table id="table_i2g_hl2_xlb" class="rest_api_request_parameters"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Fields within the specified standard change template to modify when creating the request. The key is the field name within the template and the value is the information to populate in the field.Fields that cannot be modified and are ignored if passed in:

-   Description
-   Backout plan
-   Test plan
-   Implementation plan
-   Read-only fields as defined in ACLs
-   Fields that do not exist in the specified standard change template

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_ajc_wm2_xlb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body

The API returns these JSON or XML elements in the response body.

<table id="table_mc1_pr1_tx"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Name-value pairs of the fields that were created in the standard change request.Data type: Object

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id information of the newly created standard change request.Data type: Object

```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the standard change request to display in a UI.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the standard change request.Data type: String

</td></tr><tr><td>

\_\_meta.ignoredFields

</td><td>

Key-value pairs that were passed in the call, but weren't applied to the change request as they either don't exist in the base record or the fields are read-only. Data type: Array

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.servicenow.com" \
--request POST \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  result: [
    {
      sys_id: {
        value: "1c87925347c12200e0ef563dbb9a7177",
        display_value: "1c87925347c12200e0ef563dbb9a7177"
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Add network switch to cabinet",
        display_value: "Add network switch to cabinet"
      }
      __meta: {
        ignoredFields: ["no_such_field"]
      }
    }
  ]
}
```

## Change Management - POST /sn\_chg\_rest/change/\{change\_sys\_id\}/task

Creates one change request task based on the default change request task record and associates it with the specified change request. Multiple change request task creations within a single call is not supported.

### URL format

Versioned URL: `/api/sn_chg_rest/{api_version}/change/{change_sys_id}/task`

Default URL: `/api/sn_chg_rest/change/{change_sys_id}/task`

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

change\_sys\_id

</td><td>

Sys\_id of the change request to which to associate this task.Data type: String

Table: Change Request \[change\_request\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

key-value pairs

</td><td>

Fields to modify when creating the request. The key is the field name within the template and the value is the information to populate in the field. Fields that cannot be modified and are ignored if passed in:

-   Business rules
-   Read-only fields as defined in ACLs
-   Fields that do not exist

 Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Request completed successfully.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not Found. The specified record couldn't be found.|
|500|Internal Server Error. A logic error on the server-side code occurred.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name-value pairs

</td><td>

Name-value pairs of the fields that were created in the change request task.Data type: Object

</td></tr><tr><td>

parent

</td><td>

Information for the change request associated to the task.Data type: Object

 ```
parent: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

parent.display\_value

</td><td>

Information to display in the UI for the change request associated to the task.Data type: String

</td></tr><tr><td>

parent.value

</td><td>

Sys\_id of the change request associated to the task.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id information of the newly created change request task.Data type: Object

 ```
sys_id: {
  display_value: "String", 
  value: "String"
}
```

</td></tr><tr><td>

sys\_id.display\_value

</td><td>

Sys\_id of the change request task to display in a UI.Data type: String

</td></tr><tr><td>

sys\_id.value

</td><td>

Sys\_id of the change request task.Data type: String

</td></tr><tr><td>

\_\_meta.ignoredFields

</td><td>

Key-value pairs that were passed in the call, but weren't applied to the change request as they either don't exist in the base record or the fields are read-only. Data type: Array

</td></tr></tbody>
</table>### cURL request

```
curl "https://instance.servicenow.com/api/now/change/0f4ac6c4b750230096c3e4f6ee11a9fe/task?short_description=Retire node&no_such_field=test" \
--request POST \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  result: [
    {
      sys_id: {
        value: "12629ec4b750230096c3e4f6ee11a9d5",
        display_value: "12629ec4b750230096c3e4f6ee11a9d5"
      },
      parent: {
        value: "0f4ac6c4b750230096c3e4f6ee11a9fe ", 
        display_value: "CHG0033046 "
      },
      ..., // all valid fields in record, example below
      short_description: {
        value: "Retire node",
        display_value: "Retire node"
      }
      __meta.ignoredFields": ["no_such_field"]
    }
  ]
}
```


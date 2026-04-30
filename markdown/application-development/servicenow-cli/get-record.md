---
title: Get a record
description: Retrieves a single record based on the specified sys\_id from the specified table.
locale: en-US
release: zurich
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Perform record operations using ServiceNow CLI, ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Get a record

Retrieves a single record based on the specified sys\_id from the specified table.

## Before you begin

Role required: sn\_cli\_metadata.cli\_admin, sn\_cli\_metadata.cli\_user, or admin

## Procedure

1.  Open your system's command-line tool and execute this command.

    ```
    $ snc record get [--table table --sysid sys_id]
    ```

    Pass in values for these arguments.

    |Parameter|Description|
    |---------|-----------|
    |table|Required. Name of the table from which to retrieve the record.|
    |sysid|Required. Sys\_id of the record to retrieve.|


## Example

```
$ snc record get --table incident --sysid 552c48888c033300964f4932b03eb092
```

The system returns the record in JSON format.

```
{
   "result": {
      "active": "true",
      "activity_due": "",
      "additional_assignee_list": "",
      "approval": "not requested",
      "approval_history": "",
      "approval_set": "",
      "assigned_to": "",
      "assignment_group": "",
      "business_duration": "",
      "business_service": "",
      "business_stc": "",
      "calendar_duration": "",
      "calendar_stc": "",
      "caller_id": {
         "link": "https://my-instance.service-now.com/api/now/table/sys_user/005d500b536073005e0addeeff7b12f4",
         "value": "005d500b536073005e0addeeff7b12f4"
      },
      "category": "inquiry",
      "caused_by": "",
      "child_incidents": "0",
      "close_code": "",
      "close_notes": "",
      "closed_at": "",
      "closed_by": "",
      "cmdb_ci": "",
      "comments": "",
      "comments_and_work_notes": "",
      "company": "",
      "contact_type": "",
      "contract": "",
      "correlation_display": "",
      "correlation_id": "",
      "delivery_plan": "",
      "delivery_task": "",
      "description": "",
      "due_date": "",
      "escalation": "0",
      "expected_start": "",
      "follow_up": "",
      "group_list": "",
      "hold_reason": "",
      "impact": "3",
      "incident_state": "1",
      "knowledge": "false",
      "location": "",
      "made_sla": "true",
      "notify": "1",
      "number": "INC0010112",
      "opened_at": "2019-07-29 18:48:43",
      "opened_by": {
         "link": "https://my-instance.service-now.com/api/now/table/sys_user/6816f79cc0a8016401c5a33be04be441",
         "value": "6816f79cc0a8016401c5a33be04be441"
      },
      "order": "",
      "parent": "",
      "parent_incident": "",
      "priority": "5",
      "problem_id": "",
      "reassignment_count": "0",
      "reopen_count": "0",
      "reopened_by": "",
      "reopened_time": "",
      "resolved_at": "",
      "resolved_by": "",
      "rfc": "",
      "route_reason": "",
      "service_offering": "",
      "severity": "3",
      "short_description": "Assessment :  ATF Assessor",
      "sla_due": "",
      "state": "1",
      "subcategory": "",
      "sys_class_name": "incident",
      "sys_created_by": "admin",
      "sys_created_on": "2019-07-29 18:49:28",
      "sys_domain": {
         "link": "https://my-instance.service-now.com/api/now/table/sys_user_group/global",
         "value": "global"
      },
      "sys_domain_path": "/",
      "sys_id": "552c48888c033300964f4932b03eb092",
      "sys_mod_count": "0",
      "sys_tags": "",
      "sys_updated_by": "admin",
      "sys_updated_on": "2019-07-29 18:49:28",
      "task_effective_number": "INC0010112",
      "time_worked": "",
      "universal_request": "",
      "upon_approval": "proceed",
      "upon_reject": "cancel",
      "urgency": "3",
      "user_input": "",
      "watch_list": "",
      "work_end": "",
      "work_notes": "",
      "work_notes_list": "",
      "work_start": ""
   }
}
```

**Parent Topic:**[Perform record operations using ServiceNow CLI](manage-records.md)


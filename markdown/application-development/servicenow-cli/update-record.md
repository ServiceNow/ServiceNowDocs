---
title: Update a record
description: Updates the specified record with the given data attributes.
locale: en-US
release: xanadu
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Perform record operations using ServiceNow CLI, ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Update a record

Updates the specified record with the given data attributes.

## Before you begin

Role required: sn\_cli\_metadata.cli\_admin, sn\_cli\_metadata.cli\_user, or admin

## Procedure

1.  Open your system's command-line tool and execute this command.

    ```
    $ snc record update [--sysid sys_id --table table --data data]
    ```

    Pass in values for these arguments.

    |Parameter|Description|
    |---------|-----------|
    |table|Required. Name of the table in which to save the record.|
    |sysid|Required. Sys\_id of the record to update.|
    |data|Required. Field name and the associated value for each field to define in the specified record in JSON string format.|


## Example

```
$ snc record update --sysid 9ef81de2db0d6090d7055268dc961978 --table incident --data "{'short_description': 'Email servers down', 'urgency':'1'}"
```

The system returns field-value pairs for the updated record.

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
      "assignment_group": {
         "link": "https://my-instance.service-now.com/api/now/table/sys_user_group/287ebd7da9fe198100f92cc8d1d2154e",
         "value": "287ebd7da9fe198100f92cc8d1d2154e"
      },
      "business_duration": "",
      "business_service": "",
      "business_stc": "",
      "calendar_duration": "",
      "calendar_stc": "",
      "caller_id": "",
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
      "impact": "2",
      "incident_state": "1",
      "knowledge": "false",
      "location": "",
      "made_sla": "true",
      "notify": "1",
      "number": "INC0010003",
      "opened_at": "2020-12-15 21:17:05",
      "opened_by": {
         "link": "https://my-instance.service-now.com/api/now/table/sys_user/6816f79cc0a8016401c5a33be04be441",
         "value": "6816f79cc0a8016401c5a33be04be441"
      },
      "order": "",
      "parent": "",
      "parent_incident": "",
      "priority": "2",
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
      "short_description": "Email servers down",
      "sla_due": "",
      "state": "1",
      "subcategory": "",
      "sys_class_name": "incident",
      "sys_created_by": "admin",
      "sys_created_on": "2020-12-15 21:17:05",
      "sys_domain": {
         "link": "https://my-instance.service-now.com/api/now/table/sys_user_group/global",
         "value": "global"
      },
      "sys_domain_path": "/",
      "sys_id": "9ef81de2db0d6090d7055268dc961978",
      "sys_mod_count": "1",
      "sys_tags": "",
      "sys_updated_by": "admin",
      "sys_updated_on": "2021-01-27 22:56:33",
      "task_effective_number": "INC0010003",
      "time_worked": "",
      "universal_request": "",
      "upon_approval": "proceed",
      "upon_reject": "cancel",
      "urgency": "1",
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


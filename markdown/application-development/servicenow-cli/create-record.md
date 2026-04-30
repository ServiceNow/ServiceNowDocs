---
title: Create a record
description: Inserts a single record in a specified table.
locale: en-US
release: zurich
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Perform record operations using ServiceNow CLI, ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Create a record

Inserts a single record in a specified table.

## Before you begin

Role required: sn\_cli\_metadata.cli\_admin, sn\_cli\_metadata.cli\_user, or admin

## About this task

**Note:** You cannot insert multiple records using this command.

## Procedure

1.  Open your system's command-line tool and execute this command.

    ```
    $ snc record create [--table table --data data]
    ```

    Pass in values for these arguments.

    |Parameter|Description|
    |---------|-----------|
    |table|Required. Name of the table in which to save the record.|
    |data|Required. Field name and the associated value for each field to define in the specified record in JSON string format.|


## Result

The system creates a record in the designated table and returns field-value pairs of the new record.

## Example

```
$ snc record create --table incident, --data "{'short_description': 'Unable to open file', 'impact':'3'}"
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
      "impact": "3",
      "incident_state": "1",
      "knowledge": "false",
      "location": "",
      "made_sla": "true",
      "notify": "1",
      "number": "INC0010005",
      "opened_at": "2021-01-27 22:49:11",
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
      "short_description": "Unable to open file",
      "sla_due": "",
      "state": "1",
      "subcategory": "",
      "sys_class_name": "incident",
      "sys_created_by": "admin",
      "sys_created_on": "2021-01-27 22:49:11",
      "sys_domain": {
         "link": "https://my-instance.service-now.com/api/now/table/sys_user_group/global",
         "value": "global"
      },
      "sys_domain_path": "/",
      "sys_id": "6a6a4f5cdbcae850d7055268dc9619d4",
      "sys_mod_count": "0",
      "sys_tags": "",
      "sys_updated_by": "admin",
      "sys_updated_on": "2021-01-27 22:49:11",
      "task_effective_number": "INC0010005",
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


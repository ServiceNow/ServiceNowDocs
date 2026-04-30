---
title: JSON object format
description: The JSON object is built in two structures.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [JSONv2 web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# JSON object format

The JSON object is built in two structures.

-   A collection of name/value pairs. In various languages, this is realized as an object, record, struct, dictionary, hash table, keyed list, or associative array.
-   An ordered list of values. In most languages, this is realized as an array, vector, list, or sequence.

In its simplest form, a JSON object is just a comma delimited set of name/value pairs. For example:

```
{"name one":"value one","name two":"value two"}
```

The following is a sample of a single record array of incidents in JSON:

```
{"records":
  [{"closed_by":"",
    "__status": "success",
    "category":"inquiry",
    "escalation":"0",
    "state":"1",
    "location":"",
    "reassignment_count":"0",
    "time_worked":"",
    "order":"0",
    "due_date":"",
    "number":"INC0010180",
    "upon_approval":"proceed",
    "sla_due":"2010-03-04 22:51:49",
    "follow_up":"",
    "notify":"1",
    "business_stc":"0",
    "caused_by":"",
    "rejection_goto":"",
    "assignment_group":"d625dccec0a8016700a222a0f7900d06",
    "incident_state":"1",
    "opened_at":"2010-02-23 22:51:49",
    "wf_activity":"",
    "calendar_duration":"",
    "group_list":"",
    "caller_id":"",
    "comments":"",
    "priority":"3",
    "sys_id":"fd0774860a0a0b380061bab9094733ad",
    "sys_updated_by":"itil",
    "variables":"",
    "delivery_task":"",
    "sys_updated_on":"2010-02-23 22:51:49",
    "parent":"",
    "active":"true",
    "opened_by":"681b365ec0a80164000fb0b05854a0cd",
    "expected_start":"",
    "sys_meta":"System meta data",
    "watch_list":"",
    "company":"",
    "upon_reject":"cancel",
    "work_notes":"",
    "sys_created_by":"itil",
    "cmdb_ci":"",
    "approval_set":"",
    "user_input":"",
    "sys_created_on":"2010-02-23 22:51:49",
    "contact_type":"phone",
    "rfc":"",
    "approval_history":"",
    "activity_due":"",
    "severity":"3",
    "subcategory":"",
    "work_end":"",
    "closed_at":"",
    "close_notes":"",
    "variable_pool":"",
    "business_duration":"",
    "knowledge":"false",
    "approval":"not requested",
    "sys_mod_count":"0",
    "problem_id":"",
    "calendar_stc":"0",
    "work_start":"",
    "sys_domain":"global",
    "sys_response_variables":"",
    "correlation_id":"",
    "sys_class_name":"incident",
    "short_description":"this was inserted with python",
    "impact":"1",
    "description":"",
    "correlation_display":"",
    "urgency":"3",
    "assigned_to":"",
    "made_sla":"true",
    "delivery_plan":""}
  ]
}
```

The following is a record array of incident responses with an error.

```
{
    "records": [
        {
            "__error": {
                "message": "Invalid Insert into: incident",
                "reason": "Data Policy Exception:  Short description is mandatory "
            },
            "__status": "failure",
            "active": "true",
            "activity_due": "",
            "approval": "not requested",
            "approval_history": "",
            "approval_set": "",
            "assigned_to": "",
            "assignment_group": "d625dccec0a8016700a222a0f7900d06",
            "business_duration": "",
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
            "contact_type": "phone",
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
            "impact": "3",
            "incident_state": "1",
            "knowledge": "false",
            "location": "",
            "made_sla": "true",
            "notify": "1",
            "number": "INC0010001",
            "opened_at": "2013-07-23 18:01:17",
            "opened_by": "6816f79cc0a8016401c5a33be04be441",
            "order": "",
            "parent": "",
            "parent_incident": "",
            "priority": "5",
            "problem_id": "",
            "reassignment_count": "0",
            "reopen_count": "0",
            "resolved_at": "",
            "resolved_by": "",
            "rfc": "",
            "severity": "3",
            "short_description": "",
            "skills": "",
            "sla_due": "",
            "state": "1",
            "subcategory": "",
            "sys_class_name": "incident",
            "sys_created_by": "admin",
            "sys_created_on": "2013-07-23 18:01:17",
            "sys_domain": "global",
            "sys_id": "a96479343cb60100a92ec9a477ba9e45",
            "sys_mod_count": "0",
            "sys_updated_by": "admin",
            "sys_updated_on": "2013-07-23 18:01:17",
            "time_worked": "",
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
    ]
}
```

**Parent Topic:**[JSONv2 web service](c_JSONv2WebService.md)


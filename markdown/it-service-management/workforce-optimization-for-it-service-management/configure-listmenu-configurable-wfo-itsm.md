---
title: Configure a list menu to display in the Learning tab in Workforce Optimization for ITSM
description: Add a system property to add to or modify the list menu for Coaching with Learning in the Coaching application in Workforce Optimization for ITSM.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/workforce-optimization-for-it-service-management/configure-listmenu-configurable-wfo-itsm.html
release: zurich
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up, Coaching, Workforce Optimization for ITSM, IT Service Management]
---

# Configure a list menu to display in the Learning tab in Workforce Optimization for ITSM

Add a system property to add to or modify the list menu for Coaching with Learning in the Coaching application in Workforce Optimization for ITSM.

## Before you begin

**Important:** This feature is available with the Coaching with Learning plugin \(sn\_coach\_lrn\) from the ServiceNow Store. To enable this feature, see [Activate Workforce Optimization for ITSM for configurabe workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/workforce-optimization-for-it-service-management/activate-configurable-workforce-optimization-itsm.md).

Set the map application scope to **Coaching With Learning**. For information on how to set the scope, see [Set map application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-user-experiences/set-map-application-scope.md).

Role required: admin

## Procedure

1.  In the application navigator, enter `sys_properties.list`.

2.  Click **New**.

3.  Enter the following field values.

<table id="table_yfh_h3p_f4b"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Suffix

</td><td>

learning\_list\_menu\_props

</td></tr><tr><td>

Name

</td><td>

sn\_coach\_lrn.learning\_list\_menu\_props

</td></tr><tr><td>

Application

</td><td>

Coaching With Learning

</td></tr><tr><td>

Type

</td><td>

String

</td></tr><tr><td>

Value

</td><td>

```
[{
    “children”: [{
            “conditions”: “<filter condition on table>“,
            “label”: “<list name>“,
            “id”: “<unique identifier for the selection path>“,
            “selectionPath”: [
                “<list parent name>“,
                “<unique identifier for the selection path>”
            ],
            “table”: “<table name>”
        }
    ],
    “label”: “<list name>“,
    “id”: “<list parent name>“,
    “isExpanded”: true,
    “selectionPath”: [“<list parent name>“]
}]
```

 where:

-   &lt;children&gt; is an array of objects to create the list
-   &lt;conditions&gt; is the condition set on the selected table
-   &lt;label&gt; is the name of the list
-   &lt;id&gt; unique identifier for the selection path
-   &lt;selectionPath&gt; is the path to establish parent-child relationship in the menu
-   &lt;table&gt; is the name of the table for the menu item


</td></tr><tr><td>

Read roles

</td><td>

sn\_wfo\_cfg\_ws.user

</td></tr><tr><td>

Write roles

</td><td>

sn\_wfo\_cfg\_ws.admin

</td></tr></tbody>
</table>4.  Click **Submit**.

    The configured list displays in the Learning tab in Coaching in the Workforce Optimization for ITSM manager workspace.


## What to do next

You can copy the code below into the Value field in the system property and modify as required.

```
[{
    “children”: [{
            “conditions”: “assigned_toDYNAMICfdc474aab313001013a082c136a8dc15”,
            “label”: “All Tasks”,
            “id”: “all”,
            “selectionPath”: [
                “learning_tasks”,
                “all”
            ],
            “table”: “sn_lc_learning_task”
        },
        {
            “conditions”: “assigned_toDYNAMICfdc474aab313001013a082c136a8dc15^active=true”,
            “label”: “Active Tasks”,
            “id”: “active”,
            “selectionPath”: [
                “learning_tasks”,
                “active”
            ],
            “table”: “sn_lc_learning_task”
        },
        {
            “conditions”: “assigned_toDYNAMICfdc474aab313001013a082c136a8dc15^due_date<javascript:gs.beginningOfToday()^state!=3”,
            “label”: “Overdue Tasks”,
            “id”: “overdue”,
            “selectionPath”: [
                “learning_tasks”,
                “overdue”
            ],
            “table”: “sn_lc_learning_task”
        },
        {
            “conditions”: “assigned_toDYNAMICfdc474aab313001013a082c136a8dc15^state=3",
            “label”: “Completed Tasks”,
            “id”: “complete”,
            “selectionPath”: [
                “learning_tasks”,
                “complete”
            ],
            “table”: “sn_lc_learning_task”
        }
    ],
    “label”: “Learning Tasks”,
    “id”: “learning_tasks”,
    “isExpanded”: true,
    “selectionPath”: [“learning_tasks”]
}, {
    “children”: [{
            “conditions”: “”,
            “label”: “All Catalogs”,
            “id”: “all”,
            “selectionPath”: [
                “learning_catalogs”,
                “all”
            ],
            “table”: “sn_lc_catalog”
        },
        {
            “conditions”: “sys_created_by=javascript: gs.getUserName()“,
            “label”: “My Catalogs”,
            “id”: “my”,
            “selectionPath”: [
                “learning_catalogs”,
                “my”
            ],
            “table”: “sn_lc_catalog”
        }
    ],
    “label”: “Learning Catalogs”,
    “id”: “learning_catalogs”,
    “isExpanded”: true,
    “selectionPath”: [“learning_catalogs”]
}, {
    “children”: [{
            “conditions”: “active=true”,
            “label”: “All Courses”,
            “id”: “all”,
            “selectionPath”: [
                “learning_courses”,
                “all”
            ],
            “table”: “sn_lc_course_item”
        },
        {
            “conditions”: “authorDYNAMIC90d1921e5f510100a9ad2572f2b477fe^active=true”,
            “label”: “Internal Courses”,
            “id”: “internal”,
            “selectionPath”: [
                “learning_courses”,
                “internal”
            ],
            “table”: “sn_lc_content”
        },
        {
            “conditions”: “active=true”,
            “label”: “External Courses”,
            “id”: “external”,
            “selectionPath”: [
                “learning_courses”,
                “external”
            ],
            “table”: “sn_lc_external_content”
        }
    ],
    “label”: “Learning Courses”,
    “id”: “learning_courses”,
    “isExpanded”: true,
    “selectionPath”: [“learning_courses”]
}]
```

**Parent Topic:**[Setting up Coaching in Workforce Optimization for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/workforce-optimization-for-it-service-management/setup-coaching-configurable-workforce-optimization-itsm.md)


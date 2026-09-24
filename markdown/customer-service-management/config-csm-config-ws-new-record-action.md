---
title: Configure a new record action
description: The new record action at the main tab level in CRM Workspace enables agents to quickly create records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/config-csm-config-ws-new-record-action.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Set up CRM Workspace, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure a new record action

The new record action at the main tab level in CRM Workspace enables agents to quickly create records.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

The create record action appears as the **+** button on the main tab in CRM Workspace. Agents can select this tab to create records.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  From the list of UX applications, select CRM Workspace.

3.  Select the UX Page Properties related list on the UX Application \(CRM Workspace\) record.

4.  Select **chrome\_tab** in the Name column.

5.  In the **Value** field, add a new JSON object in the newTabMenu array.

    The default code passes an array of buttons with labels in JSON format that are configured to create a record in the Interaction or Incident tables. You can add, modify, or delete the elements through the array passed for newTabMenu.

    The following example shows the general syntax to add a button for new record creation in any table.

    ```
    {
    "label":{
    "translatable":INSERT_true_OR_false_BOOLEAN_VALUE_WITHOUT_QUOTES, "message":"INSERT_LABEL_NAME_TO_BE_DISPLAYED_ON_PLUS_BUTTON"
    },
    "routeInfo":{
    "route":"record",
    "fields":{
    "table":"INSERT_TARGET_TABLE_NAME",
    "sysId":"-1"
    },
    "multiInstField":"sysId"
    }
    }
    ```

    **Note:**

    -   Make sure that you add the comma either before or after the array to follow valid JSON format practices.
    -   sysId = -1 points to the new record being created on the table as Target\_Table\_Name.
    The following example shows how to add one more button to create a record in the Case table \(sn\_customerservice\_case\).

    ```
    {
    "label":{
    "translatable":true,
    "message":"New Case"
    },
    "routeInfo":{
    "route":"record",
    "fields":{
    "table":"sn_customerservice_case",
    "sysId":"-1"
    },
    "multiInstField":"sysId"
    }
    }
    ```

6.  Save the changes to the UX Application \(CSM Landing Page\) record.



---
title: Migrate the New Record menu
description: The New Record menu approach used in CSM Agent Workspace doesn't exist in CSM Configurable Workspace. Rebuild the menu using the chrome\_tab UX page property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/migration-new-record-menu.html
release: zurich
topic_type: task
last_updated: "2026-10-25"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Migrate the New Record menu

The New Record menu approach used in CSM Agent Workspace doesn't exist in CSM Configurable Workspace. Rebuild the menu using the chrome\_tab UX page property.

## Before you begin

Role required: admin

-   Review your existing New Record menu. Navigate to **All**, enter `sys_aw_new_menu_item.LIST`, and press **Enter** to see which buttons exist and which tables they point to.
-   Decide which buttons your agents need.

## About this task

The New Record menu is the **+** button that agents use to create cases, interactions, or other records without leaving the workspace. In the base system, the menu includes a button that creates an interaction record. Rebuilding the menu is also an opportunity to simplify it. Consider the following when you decide what to include:

-   Use Interaction as the entry point for case creation. This captures initial triage information separately and allows first-time resolutions that don't need a follow-up record such as a case, incident, or request.
-   Include only the tables that agents use most frequently, typically Case and Interaction.
-   Create accounts and contacts in a single source of truth, typically your CRM system, rather than from the New Record menu.
-   Users must have create access to a table for its button to appear in their New Record menu.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences**.

2.  Select **CSM/FSM Configurable Workspace**.

3.  In the **UX Page Properties** related list, open **chrome\_tab**.

4.  In the **Value** field, locate the `newTabMenu` array.

    You can add, change, or delete buttons in this array.

5.  Add a JSON object to the array for each button that you want to create.

    ```
    {
      "label": {
        "translatable": true,
        "message": "Label shown on the button"
      },
      "routeInfo": {
        "route": "record",
        "fields": {
          "table": "target_table_name",
          "sysId": "-1"
        },
        "multiInstField": "sysId"
      }
    }
    ```

    Set **translatable** to a Boolean value, `true` or `false`, without quotation marks. A **sysId** value of `-1` creates a new record on the target table.

    Separate each object from the next with a comma so that the array stays valid.

6.  Select **Save**.


## Example

The following JSON object adds a **New Case** button.

```
{
  "label": { "translatable": true, "message": "New Case" },
  "routeInfo": {
    "route": "record",
    "fields": {
      "table": "sn_customerservice_case",
      "sysId": "-1"
    },
    "multiInstField": "sysId"
  }
}
```


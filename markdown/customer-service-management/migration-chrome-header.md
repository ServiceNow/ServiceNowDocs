---
title: Migrate chrome header settings
description: In CSM Agent Workspace, header preferences are check boxes on the workspace record. In CSM Configurable Workspace, you configure the same settings in JSON using the chrome\_header UX page property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/migration-chrome-header.html
release: australia
topic_type: task
last_updated: "2026-11-12"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Migrate chrome header settings

In CSM Agent Workspace, header preferences are check boxes on the workspace record. In CSM Configurable Workspace, you configure the same settings in JSON using the chrome\_header UX page property.

## Before you begin

Role required: admin

Navigate to **All** &gt; **Workspace Experience** &gt; **Administration** &gt; **All Workspaces**, open the **Agent Workspace** record, and note which of the following check boxes are selected: **Search enabled**, **Notifications enabled**, and **User Preference Controls enabled**.

## Procedure

1.  Navigate to **All**, enter `sys_ux_page_property.LIST`, and press **Enter**.

2.  Group the records by **Page**.

3.  Under the CSM/FSM Configurable Workspace group, open the **chrome\_header** page property record.

4.  In the **Value** field, edit the JSON to match the header preferences that you noted in CSM Agent Workspace.

    The header preferences are in the `privatePage` object. Set each key to `true` or `false`, without quotation marks.

    |CSM Agent Workspace check box|JSON key|
    |-----------------------------|--------|
    |Search enabled|`searchEnabled`|
    |Notifications enabled|`notificationsEnabled`|
    |User Preference Controls enabled|`userPrefsEnabled`|

    Change only these keys and leave the rest of the JSON as it is. For example:

    ```
    {
      "privatePage": {
        "notificationsEnabled": true,
        "searchEnabled": true,
        "userPrefsEnabled": false,
        ...
      }
    }
    ```

5.  Select **Save**.



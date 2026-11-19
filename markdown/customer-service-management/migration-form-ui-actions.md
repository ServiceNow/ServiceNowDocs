---
title: UI Action Bar
description: Learn how the CSM Agent Workspace UI Actions component functions with CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/migration-form-ui-actions.html
release: zurich
topic_type: concept
last_updated: "2026-10-25"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# UI Action Bar

Learn how the CSM Agent Workspace UI Actions component functions with CSM Configurable Workspace.

UI actions include custom buttons, menu items, and limiting access to forms based on user role. The UI Action Bar component replaces the UI Actions component in CSM Agent Workspace.

UI actions are the buttons that agents use to act on a record, such as **Assign to me**, **Propose solution**, **Close case**, and any custom buttons that your organization built. UI actions don't appear in CSM Configurable Workspace automatically. If you skip this migration step, those buttons don't appear for agents.

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_ui\_action|sys\_ux\_form\_action|

To migrate UI actions, each UI action must have a corresponding form action to use UI actions in CSM Configurable Workspace.

To create a form action, navigate to **All** &gt; **Now Experience Framework** &gt; **Declarative Actions** &gt; **Form Actions** and select **New**.

For more information, see [Set up a form action in CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/config-csm-config-ws-form-action.md).

## Before you migrate UI actions

-   Focus on the UI actions that agents use, not system administrator actions.
-   Use the base system UI actions before you create custom ones, and question the value of each custom UI action.
-   For custom UI actions, check that scripts use workspace-compatible code. Scripts written for the Core UI may not work in CSM Configurable Workspace.

## Make UI actions available in CSM Configurable Workspace

Role required: admin

1.  Navigate to **All** &gt; **System UI** &gt; **UI Actions**.
2.  Filter by the table that you want to review, such as sn\_customerservice\_case.
3.  Open the UI action record.
4.  Select the **Format for Configurable Workspace** check box.
5.  Select **Save**.
6.  Repeat these steps for each UI action and each table that your agents use.


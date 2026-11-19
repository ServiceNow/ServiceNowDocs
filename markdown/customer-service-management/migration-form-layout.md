---
title: Migrate the form layout
description: CSM Configurable Workspace uses a workspace-specific form layout. Review your existing form layout and configure it for the workspace view before agents go live.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/migration-form-layout.html
release: australia
topic_type: task
last_updated: "2026-11-12"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Migrate the form layout

CSM Configurable Workspace uses a workspace-specific form layout. Review your existing form layout and configure it for the workspace view before agents go live.

## Before you begin

Role required: admin

Review the current form layout in CSM Agent Workspace and note which fields, sections, and related lists agents use most often.

## About this task

The form layout controls which fields, sections, and related lists agents see when they open a record. A layout that hasn't been reviewed for the workspace can show too many fields, the wrong fields, or fields in an order that doesn't match the agent workflow.

-   Keep important fields near the top of the form, and group related fields together.
-   Use the Workspace view for the form layout, or create a view specifically for the workspace. If you edit the default view instead, your changes also affect the Core UI.
-   Reuse layouts where possible to keep forms consistent. Fewer customizations also mean fewer items to maintain during upgrades.

## Procedure

1.  Open a record page in CSM Configurable Workspace, such as a case record.

2.  Select your profile name or picture at the top right of the record page, and then select **Configure page** &gt; **Form Layout**.

    The **Configure page** option appears after the record page finishes loading.

3.  Choose whether to configure the layout in Form Builder or in the Core UI.

    The form layout opens in the Core UI. If a dialog suggests Form Builder, select **Try Form Builder** to use Form Builder, or select **Not Now** to continue in the Core UI.

4.  Verify that the view name is set to Workspace.

    If it isn't, set the view name to Workspace or create a view specifically for the workspace before you make changes. This keeps workspace layout changes separate from the Core UI.

5.  Add the tabs and sections that the form needs, add or remove fields, and adjust the layout to match your agents' needs.

    Decide whether each section should be collapsible or mandatory. Collapsible sections reduce visual clutter on long forms.

6.  Save your changes.


## Result

Verify the layout in CSM Configurable Workspace before agents go live.


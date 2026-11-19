---
title: Form headers
description: Learn how CSM Agent Workspace form headers function with CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/migration-form-headers.html
release: australia
topic_type: concept
last_updated: "2026-10-25"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Form headers

Learn how CSM Agent Workspace form headers function with CSM Configurable Workspace.

Form headers provide an overview of the record.

Form headers give agents a quick summary at the top of every case or interaction record, such as the account name, contact, priority, and SLA status. Because CSM Agent Workspace and CSM Configurable Workspace share the same form header tables, you don't need to recreate your existing records. Link them to the CSM Configurable Workspace configuration instead.

**Note:** Any change to a form header record affects both CSM Agent Workspace and CSM Configurable Workspace. Test changes in both workspaces until your migration is complete.

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_aw\_form\_header|sys\_aw\_form\_header sys\_ux\_header\_config sys\_ux\_m2m\_workspace\_header\_ux\_header\_config|

To migrate your CSM Agent Workspace form header to CSM Configurable Workspace, add an additional step in custom form headers to the CSM Configurable Workspace form header setup.

-   An additional form header configuration is provided out of box, CSM/FSM Configurable Workspace Header Config.
-   Legacy form headers function without modification, but may affect the functionality of CSM Configurable Workspace.
-   Add the Form header component to your CSM Configurable Workspace for additional functionality.

For additional information, see [Set up a form header in CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/config-csm-config-ws-form-header.md).

## Before you migrate form headers

To see all existing form headers, navigate to **All** &gt; **Workspace Experience** &gt; **Forms** &gt; **Workspace Form Headers**. Use this list as your migration checklist.

-   Review the existing headers in the base system first to understand whether they need updating before you migrate them.
-   Don't leave header fields empty. Choose fields that agents can access and that contain critical information to highlight at a glance.
-   Headers and subheaders are optional. Add a subheader only when the extra context helps agents.
-   If an existing header needs updates, configure that header instead of creating a new one.

## Link form headers to CSM Configurable Workspace

Role required: admin

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Header Configurations**.
2.  Open the **CSM/FSM Configurable Workspace Header Config** record.
3.  In the **Workspace Form Headers** related list, select **Edit**.

    If the related list doesn't appear, configure the form to display it.

4.  Move the form headers that you want to add from the left column to the right column.
5.  Select **Save**.


---
title: Ribbons
description: Learn how CSM Agent Workspace ribbons function with CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/migration-form-ribbons.html
release: australia
topic_type: concept
last_updated: "2026-10-25"
reading_time_minutes: 2
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Ribbons

Learn how CSM Agent Workspace ribbons function with CSM Configurable Workspace.

Ribbons help agents quickly scan relevant information about a record, such as a timeline, a user, or a customer summary.

The ribbon displays the Customer 360, SLA, and timeline widgets. Because both workspaces share the same ribbon setting tables, migrating ribbons is a quick win: the records already exist, and you link them to the CSM Configurable Workspace configuration.

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_aw\_ribbon\_setting|sys\_aw\_ribbon\_setting sys\_ux\_ribbon\_config sys\_ux\_ribbon\_config\_setting|

Legacy ribbon widgets work in CSM Configurable Workspace, but not the legacy ribbon configurations. Add ribbon settings to a ribbon configuration to appear in CSM Configurable Workspace.

For more information, see [Set up a ribbon configuration in CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/config-csm-config-ws-ribbon.md).

**Note:**

-   When you migrate, verify that the widgets, width values, and order in each ribbon setting are correct for CSM Configurable Workspace. The total combined width of all ribbon components must be 12 or less.
-   Any change to a ribbon setting record affects both CSM Agent Workspace and CSM Configurable Workspace. Test changes in both workspaces until your migration is complete.

## Verify ribbon settings

Role required: admin

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Ribbon Setting**.
2.  Open the ribbon setting record and verify that the widgets, width values, and order are correct for CSM Configurable Workspace.
3.  If changes are needed, modify the ribbon setting and select **Save**.

## Add ribbon settings to a ribbon configuration

CSM Configurable Workspace includes one ribbon configuration, CSM/FSM Configurable Workspace Ribbon Config, which contains the Customer 360, Timeline, and Active SLA ribbon components. A ribbon setting appears in the workspace only after you add it to a ribbon configuration.

Role required: admin

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **Ribbon Configuration Settings**.
2.  Select **New**.
3.  Add the ribbon setting to the ribbon configuration, such as CSM/FSM Configurable Workspace Ribbon Config, and save the record.

## Tips for ribbon widgets

-   Choose widgets that show the data agents need most often. Divide the 12 width units between widgets based on the volume of information that each one contains.
-   For the Customer 360 widget, specify the primary user tables, such as contact and consumer, the primary user fields, such as name and phone, and the secondary fields. Fill in the secondary fields so that the widget isn't blank when primary user details are missing.
-   For the Timeline widget, specify which task states indicate that the task is awaiting a customer response.
-   Train agents on the ribbon so that they use it. Show agents how to interpret the SLA colors that indicate an SLA is approaching its breach limit, and explain that the Timeline calculations are affected if they don't update the task state correctly.


---
title: Lists
description: Learn about how CSM Agent Workspace lists function with CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/migration-lists.html
release: zurich
topic_type: concept
last_updated: "2026-10-25"
reading_time_minutes: 3
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Lists

Learn about how CSM Agent Workspace lists function with CSM Configurable Workspace.

The list view displays filtered lists of records, such as All tasks, Open tasks, and My tasks. By setting up list categories and filtered lists, you help your agents quickly find the records they need to work on. Configure your CSM Agent Workspace lists setups in CSM Configurable Workspace.

Agents use lists such as My Cases, My Open Cases, and Unassigned for my groups to find and manage their work, and they create personal lists for quick access to the records most relevant to their role. Verifying list access after migration means that agents see the right lists from their first day in CSM Configurable Workspace.

## Before you migrate lists

-   Note which lists and list categories exist in CSM Agent Workspace and which agent groups have access to each one. You need this information to set up audiences in CSM Configurable Workspace.
-   A list category doesn't appear in the workspace unless it has at least one list associated with it.
-   The **Order** field on a list category or list controls the display order in the workspace.
-   Remove list categories and lists that aren't relevant to your agents to reduce information overload in the workspace.
-   Decide whether lists need access controls for specific roles or groups.
-   Decide whether to disable the **New** button on list views.
-   Decide whether agents need UI notifications when a record is updated. If they do, define the recipients and the trigger conditions.

## List Menu Configuration

The Menu Configuration is a container that houses the default configurations of the list menu which consists of categories and filters.

|Legacy table name|UIB table name|
|-----------------|--------------|
|No corresponding table|sys\_ux\_list\_menu\_config|

The List Menu setup is added by default to CSM Configurable Workspace. Associate your list and list categories with this configuration.

## List categories

List categories enable you to group records so that agents can find the records they need to work on.

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_aw\_list\_category|sys\_ux\_list\_category|

## Filtered lists

Filtered lists enable you to group records that help agents do their work more efficiently.

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_aw\_list|sys\_ux\_list|

**Note:** Roles and groups are defined in the UIB table and are not applicable.

## Role and Access

Roles and access enable you to define the audience of each of the lists defined in the list filters.

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_aw\_list|sys\_ux\_applicability\_m2m\_list|

To migrate roles and access, select a filtered list and choose the audience.

In CSM Agent Workspace, list access is controlled by roles on the workspace record. In CSM Configurable Workspace, access is controlled by audiences.

**Note:** Changes to list categories and lists in CSM Configurable Workspace don't affect CSM Agent Workspace. The two workspaces use separate list configurations.

## Verify and update your list configuration

Role required: admin

1.  Open the UX List Menu Configuration page in one of the following ways:
    -   In UI Builder, go to the List page and select the **Configuration** link in the Config panel.
    -   Navigate to **All**, enter `sys_ux_list_menu_config.LIST`, press **Enter**, and open **CSM/FSM Configurable Workspace List Menu Config**.
2.  Review the existing list categories and lists, and remove any that aren't relevant to your agents.
3.  To add a list category, select **New** in the **UX List Categories** section, enter a name, and set the **Order** field.
4.  To add a list under a list category, select **New** in the **UX Lists** section under that category and fill in the required fields.

## Set audience access for lists

If your CSM Agent Workspace had different lists for different agent groups, set up equivalent audiences in CSM Configurable Workspace.

Role required: admin

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Audiences**, or use the **Applicability** link in UI Builder.
2.  Create an audience for each agent group that needs access to a specific set of lists, such as frontline agents and agent managers.
3.  In UI Builder, open the M2M Applicability List \[sys\_ux\_applicability\_m2m\_list\] and create a list applicability record for each audience and list combination.


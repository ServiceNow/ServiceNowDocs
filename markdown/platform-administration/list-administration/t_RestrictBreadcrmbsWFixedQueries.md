---
title: Restrict filters and breadcrumbs with fixed queries
description: The record list view allows users to navigate to different subsets of a table using breadcrumbs and filters. You can limit access to parts of the table by restricting active links in breadcrumbs or by suppressing breadcrumbs and filters for specific roles.
locale: en-US
release: xanadu
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Restrict filters and breadcrumbs with fixed queries

The record list view allows users to navigate to different subsets of a table using breadcrumbs and filters. You can limit access to parts of the table by restricting active links in breadcrumbs or by suppressing breadcrumbs and filters for specific roles.

## Before you begin

Role required: admin

## About this task

A breadcrumb option enables an administrator to control the base view of a record list presented to users. By adding a fixed query to the argument for a module, an administrator can prevent users from expanding their view past a specified starting point. The argument for this fixed query is written as **&amp;sysparm\_fixed\_query=active=true**. A use case for this query is to prevent users from using the breadcrumbs to switch a list of open incidents to a list of all incidents. When users select **Incident** &gt; **Open**, they are limited to viewing and filtering a list of open \(active=true\) incidents.

**Note:** A new Create ACL allows all users to save filters by default. This overrides any custom ACLs in place if administrators are restricting filter access. The new ACL gives all users access to the User field by default, and access to the Group field only if users have the filter\_group role and are in the currently selected group.

## Procedure

1.  Point to the application menu that contains the module to edit and click the edit application \(pencil\) icon.

    To open the module directly, point to the module and click the edit module \(pencil\) icon.

2.  Select the module to edit.

    For example, select **Open**.

3.  In the **Link Type** section of the Module form, select **List of Records** for the **Link type**.

4.  Delete the **Active is true** filter, if present.

5.  Add **&amp;sysparm\_fixed\_query=active=true** to the **Arguments** field and update the record.

    ![Add fixed query argument](../image/FixedQuery1.png)

6.  Navigate to **Incidents** &gt; **Open** and examine the breadcrumbs.

    The **Active=true** link is the widest view permitted in the list of Open incidents shown. The breadcrumb for **All** is not a link because of the fixed query.

    ![Breadcrumb for All is not linked](../image/FixedQuery2.png)


-   **[Suppress filters and breadcrumbs with list controls](t_SuppressFiltersAndBreadcrumbs.md)**  
Use list controls to suppress filters and breadcrumbs on defined tables for users with specific roles.
-   **[Use script includes to suppress filters and breadcrumbs](t_SuppressFiltersScriptInclude.md)**  
You can use a script to restrict filters and breadcrumbs to specific roles, either on a per-table or global basis. Using a script is an advanced option that offers additional flexibility compared to using list control.
-   **[Increase the allowed number of breadcrumb entries](increase-breadcrumb-entries.md)**  
You can add a property to allow for a larger number of breadcrumb entries in the filter.

**Parent Topic:**[List administration](../../core-configuration/concept/p_ListAdministration.md)


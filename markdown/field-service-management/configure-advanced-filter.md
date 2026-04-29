---
title: Configuring advanced resource filters for Dispatcher Workspace
description: Advanced resource filtering allows administrators and dispatchers to create and save their own filters for Dispatcher Workspace. This lets dispatchers personalize their view in Dispatcher Workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configuring advanced resource filters for Dispatcher Workspace

Advanced resource filtering allows administrators and dispatchers to create and save their own filters for Dispatcher Workspace. This lets dispatchers personalize their view in Dispatcher Workspace.

## Default resource filtering

By default, Dispatcher Workspace allows dispatchers to filter what they see with the contextual side panel. Dispatchers can filter by agent, contractor, or skill. For more information, see [Filter Dispatcher Workspace views](../task/filter-workspace-views.md).

## Advanced resource filtering

Advanced resource filtering allows dispatchers to create their own filtered view in Dispatcher Workspace. They can save the filtered view to personalize what they see every time they open Dispatcher Workspace. Dispatchers can also create and save any number of filters so they can quickly re-apply any view they might need to see.

Advanced resource filtering also allows administrators to create their own advanced filter and apply it to Dispatcher Workspace for all dispatchers to use.

## The advanced resource filter system property

When you enable the advanced resource filter system property you turn on four data base views. Database views are collections of tables. These four database views contain tables with values that dispatchers can use to create their advanced resource filters. The four database views are the:

-   agent filter configuration database view
-   crew filter configuration database view
-   equipment filter configuration view
-   contractor filter configuration view

The advanced resource filter system property also turns on a control which allows administrators to create any custom filter and add it to Dispatcher Workspace for all dispatchers to use. This control is called the Resource Filter configuration.

You must have the calendar collapsed system property \(`sn_fsm_disp_wrkspc.calendarCollapsedBehavior`\) enabled to use advanced resource filters.

## Database views

The four database views contain a list of tables. By default, dispatchers can create advanced filters based off of:

-   Username or user skill in the **Agents** tab.
-   Crew name or crew skill in the **Crews** tab.
-   Equipment category or resource type in the **Equipment** tab.
-   Contractor name in the **Contractor** tab.

    **Note:** In the **Contractor** tab the field that you select to filter a contractor is labeled Assignment Group, even though you are filtering on contractors.


If you want dispatchers to be able to use more values to create advanced filters with, then you must indicate what values in the tables are available.

The tables are different if you have assignment groups or territories configured. For a list of the tables that contain the values administrators must enable for dispatchers to use to create resource filters, see [Advanced resource filter tables](../reference/advanced-filter-tables.md)

## Extending tables

The values in any tables related to users or crews that are part of your deployment can be extended into Dispatcher Workspace and used to create an advanced resource filter. The process is called Creating database views for reporting.

**Warning:** You must be a professional developer and a service now administrator to set this up.

For more information, see [Working with database views for reporting](https://www.servicenow.com/docs/access?context=c_DatabaseViews&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Resource filter configuration

Administrators can create advanced resource filters for dispatchers using the values available in the [Advanced resource filter tables](../reference/advanced-filter-tables.md). When an administrator creates an advanced resource filter, the resource filter is available for all dispatchers to use in Dispatcher Workspace.

## Configuration overview

The steps for setting up advanced resource filters are:

1.  [Properties installed with Field Service Management](../../planning-and-policy/reference/r_PropInstallWFieldServMgmnt.md)

    Enable the advanced resource filters system property \(sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.show\_advanced\_resource\_filter\).

2.  \(Optional\) [Configure resource filter options](../task/configure-filter-options.md)

    Select the values that are available for dispatchers to create advanced resource filters with.

3.  \(Optional\) [Create an advanced resource filter for dispatchers](../task/create-resource-filter.md)

    Create an advanced resource filter for all dispatchers to use in Dispatcher Workspace.

4.  [Advanced Filtering in Dispatcher Workspace](advance-filter-dispatch.md)

    Dispatchers can create and apply their own advanced filters.



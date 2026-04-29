---
title: Add Workbench widgets to an in-line dashboard
description: You can place Core UI workbench widgets on an inline dashboard. They are added in compatibility mode.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Add elements, Edit a dashboard, Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Add Workbench widgets to an in-line dashboard

You can place Core UI workbench widgets on an inline dashboard. They are added in compatibility mode.

## Before you begin

Role required: Any user can add workbench widgets from the library to a dashboard they have edit rights on. Users with admin or pa\_admin roles can create new workbench widgets in Core UI.

The system property com.snc.pae.workbench\_enabled must be set to true.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Either [create a dashboard](create-db-in-ac.md) or open the dashboard you want to edit.

3.  If the dashboard has an **Edit** button, select it.

    A new dashboard is automatically in editing mode. A technical dashboard has an **Open in UI Builder** button instead of an **Edit** button. For more information about technical dashboards, see [Technical dashboards](../../performance-analytics/concept/technical-dashboards.md).

4.  Expand **Add New Element**.

5.  Select the **Workbench** element.

6.  Choose one or more workbenches from the library and select **Add to Dashboard**.![Select a workbench from the library modal showing four elements with name, description, creator, and last updated timestamp](../../par-for-workspace/image/inline-db-select-wb.png)

    Users with the admin or pa\_admin roles see the option to create new workbench widgets in Core UI. For more information, see [Monitor a workflow with a workbench process widget](../../performance-analytics/concept/c_MonitorWorkflowWorkbenchWidget.md#).


## Result

The Core UI workbench widgets are added to the inline dashboard in compatibility mode.

**Parent Topic:**[Add visual elements to an in-line dashboard](add-elements-to-a-dashboard.md)


---
title: Add Guided Decisions to Service Portal
description: Create or edit a page to add decision trees to Service Portal so internal users can troubleshoot their issues.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Add Guided Decisions to Service Portal

Create or edit a page to add decision trees to Service Portal so internal users can troubleshoot their issues.

## Before you begin

The decision tree that you want to add to the Service Portal page must exist. For more information, see [Configuring decision trees in Decision Tree Builder](../concept/decision-trees-in-gdb.md).

Role required: sp\_admin or admin

## About this task

These steps are intended for users with little to no coding experience.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  From the Service Portal Designer, either select an existing page or add a new page.

<table id="choicetable_bmv_x5r_c1c"><thead><tr><th align="left" id="d181503e111">

Option

</th><th align="left" id="d181503e114">

Action

</th></tr></thead><tbody><tr><td id="d181503e120">

**Use an existing page**

</td><td>

Select the page.

</td></tr><tr><td id="d181503e129">

**Add a page**

</td><td>

1.  Select **Add a new Page**.
2.  Provide the page title and ID.
3.  Select **Submit**


</td></tr></tbody>
</table>4.  Under Layouts, create the area to add widgets by selecting **Container** and dragging it onto the page.

5.  In the **Widgets** tab, in the **Filter Widget** field, search for the Decision tree - Visualiser widget, then drag the widget to the layout.

6.  Select the Edit icon \(![Edit icon](../image/icon-pencil-ac.png)\).

7.  Provide the decision tree ID.

    1.  On the decision tree record, select the Additional actions icon \(![Additional actions icon](../../../use/collaboration/image/IconMenu.png)\).

    2.  Select **Copy sys\_id** from the menu.

8.  Select **Save**.


## What to do next

If you want the decision tree theme to match the Service Portal, you can apply a UX theme to change your existing theme. For more information, see [Match the theme of the decision tree component with the Service Portal page](apply-new-theme-to-service-portal.md).

**Related topics**  


[Configuring Guided Decisions](../concept/setting-up-guided-decisions.md)

[Configuring guidances and decision trees](../concept/configuring-guided-decisions.md)


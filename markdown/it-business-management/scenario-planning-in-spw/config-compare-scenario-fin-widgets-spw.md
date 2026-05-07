---
title: Configure financial widgets in compare scenario
description: Add or manage existing widgets to view financial insights while comparing scenarios. Define your own attribute from the cost types to view it's details in the Compare scenario page.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring scenario planning in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Configure financial widgets in compare scenario

Add or manage existing widgets to view financial insights while comparing scenarios. Define your own attribute from the cost types to view it's details in the Compare scenario page.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Widgets**.

2.  In the Widgets list, filter the Short description with **Compare scenario** to view the existing list.

    By default, there are five financial widgets enabled to compare the financial performance of scenarios.

    ![List of default financial widgets shipped for scenario planning.](../image/financial-widgets-compare-scenario-ootb.png)

3.  Edit an existing widget or create a widget to use it in scenario planning.

<table id="choicetable_rl1_scr_dfc"><thead><tr><th align="left" id="d242884e96">

Choice

</th><th align="left" id="d242884e99">

Description

</th></tr></thead><tbody><tr><td id="d242884e105">

**Edit an existing widget**

</td><td>

1.  Select a record from the list.
2.  Edit the **Script** field to customize and fetch required financial information into the widget.


</td></tr><tr><td id="d242884e126">

**Create a widget**

</td><td>

1.  Select **New**.
2.  In the **Name** field, enter a unique name for the widget.
3.  In the **Script**, write the script to fetch the required financial data.

For example, if you want to view the Software Capex budget widget, update the target and cost type sys\_id in the widget.

4.  Right-click on the header and select **Save**.
5.  Select **Widget associations** related list and select **New**.
6.  From the Association ID lookup option, select **Scenario item financial \[sn\_align\_ws\_scenario\_item\_financial\]**.
7.  Select **Submit**.


</td></tr></tbody>
</table>4.  Select **Submit**.



---
title: Personalize the Prioritization view
description: All references to "Backlog" are changed to "Prioritization" following the change of the feature name in the app.Personalize the List view in the Prioritization page by grouping, sorting, and hiding columns so that you can view the information that is most relevant for planning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/scenario-planning-in-spw/personalize-backlog-in-alignment-planner-workspace.html
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace]
breadcrumb: [Personalizing views for prioritization, Prioritize portfolio plan work, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Personalize the Prioritization view

Personalize the List view in the Prioritization page by grouping, sorting, and hiding columns so that you can view the information that is most relevant for planning.

## Before you begin

[Create a portfolio plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/create-portfolio-plans-in-alignment-planner-workspace.md).

Role required: sn\_align\_core.apw\_user

## About this task

This task provides guidance on different options to personalize the view of Prioritization tab in the Planning page.

Personalization preferences are saved as the portfolio plan's settings in Strategic Planning. So, these settings are applied to all the users or user groups that the portfolio plan is shared with.

## Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.

2.  From the list of portfolio plans, select one and then select **Planning**.

3.  Use the Personalize side panel to update the display of rows and columns on the page.

    1.  Select the Personalize icon \(\[Omitted image "icon-settings.png"\] Alt text: Personalize icon.\).

    2.  From the Columns section, select the columns that you want to see or hide the data of.

        You can reorder the columns here to change their display order on the backlog.

        If you want additional columns to be available in this page, your admin can configure them. See [Configuring additional columns for Prioritization in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/customizing-the-default-backlog-view-in-alignment-planner-workspace.md).

    3.  From the Rows section, choose how the rows are displayed, using the **Shade alternate rows** toggle.

4.  Group your items by one or multiple columns that are on display in the Prioritization tab.

    You can group the planning items by an attribute of the type choice or reference. Some examples to group by are Planning state, Planning item type, Owner, and Primary goal.

    Use one of the following ways to group the planning items. Repeat the action to group the list by multiple attributes.

<table id="choicetable_mwf_cgk_htb"><thead><tr><th align="left" id="d140623e201">

Choice

</th><th align="left" id="d140623e204">

Action

</th></tr></thead><tbody><tr><td id="d140623e210">

**Drag and drop**

</td><td>

Drag and drop a column name to the **Grouped by** bar above the list.

 In the sample list here, the Planning item type column is dropped into the **Grouped by** bar.

 \[Omitted image "backlog-grouping-animation.gif"\] Alt text: Animation showing grouping the backlog list by planning item type.

</td></tr><tr><td id="d140623e238">

**Use Column actions**

</td><td>

Select the Column actions icon \(\[Omitted image "icon-column-actions.png"\] Alt text: Column actions.\) and select **Group by &lt;attribute&gt;**.\[Omitted image "backlog-grouping-option.png"\] Alt text: Prioritization page grouping option from column actions.

</td></tr></tbody>
</table>    Grouping remains unaffected even when you switch to Kanban or Hierarchy tabs. The same setting is retained when you come back to the Prioritization tab. This preference is saved per session for a portfolio plan.

5.  Sort the planning items by any column, by clicking the column name.

    For example, you can sort the items by **Approved start date**.

6.  Pin columns to the left or right of the list.

    1.  For the column that you want to pin, select the Column actions icon \(\[Omitted image "icon-column-actions.png"\] Alt text: Column actions.\).

    2.  From the Pin column section, select **Pin to left** or **Pin to right**.

        The default selection is **Unpin**.

7.  Adjust the width of the columns as per choice or set the width to autofit.

    Hold and drag the column border to adjust its width. You can set the column width to autofit using the **Autofit this column** or **Autofit all columns** options from the Column actions \(\[Omitted image "icon-column-actions.png"\] Alt text: Column actions.\).

8.  Reset columns to default settings by selecting **Reset columns** from the Personalize menu \(\[Omitted image "icon-settings.png"\] Alt text: Personalize icon.\).

    Selecting this option reverts the column personalization, grouping, and sorting to default settings.

    Personalization settings that you've made so far on the Prioritization tab would be cleared. Any personalization that you make after this point is set as the new preference for the portfolio.

9.  Apply filters to the data shown in Prioritization.


**Parent Topic:**[Personalizing views for prioritization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/personalize-prioritization-page-in-strategic-planinng-workspace.md)


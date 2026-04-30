---
title: Set objectives for Process Mining projects
description: Define the kind of data or process that you want to view and analyze in your graph. You must select a specific table \(parent table\) that has the data that you want to analyze.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a project or template using Project Builder, Using Process Mining, Process Mining, Platform Analytics]
---

# Set objectives for Process Mining projects

Define the kind of data or process that you want to view and analyze in your graph. You must select a specific table \(parent table\) that has the data that you want to analyze.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

## Procedure

1.  When you select **Create New Project**, you’re taken to the **Set objectives** tab.

2.  Provide the following details.

<table id="choicetable_j24_f5k_nzb"><thead><tr><th align="left" id="d89337e65">

Field

</th><th align="left" id="d89337e68">

Description

</th></tr></thead><tbody><tr><td id="d89337e74">

**Select type**

</td><td>

Choose whether you want to create a project or a template.

</td></tr><tr><td id="d89337e83">

**Template type**

</td><td>

This field is available only if you choose the type as **Template**.Four values are available:

-   Default
-   WFO
-   Vendor Management
-   Digital Portfolio Management
For a template that is not part of WFO, Vendor Management, or Digital Portfolio Management, choose **Default**. For example, to create a Performance Analytics template, select **Default**.

</td></tr><tr><td id="d89337e122">

**Name**

</td><td>

An intuitive name for the project or template you’re creating.

</td></tr><tr><td id="d89337e131">

**Short description**

</td><td>

A short description for the project or template you’re creating.

</td></tr><tr><td id="d89337e141">

**Source Type**

</td><td>

The source for the project or template you’re creating.-   Table: Any database table
-   Report source: Select a table that has reports
-   External data: Select a table that has the imported dataset.
-   Archived data: Select an archived table.


</td></tr><tr><td id="d89337e164">

**Table**

</td><td>

Select a table that you want to base your project on. This list varies depending on the type of source that you’ve selected.

</td></tr><tr><td id="d89337e176">

**Mark as restricted**

</td><td>

Select the check box if you want to limit project access to the owner and the users they explicitly share it with. Administrators and power users don't have access to the mined data unless the project is shared with them. Once a project is marked as restricted, only the owner can clear this field.

When you’re dealing with sensitive data and must restrict access, you can use this option.

</td></tr><tr><td id="d89337e189">

**Auto retire**

</td><td>

This field is available only if you choose the type as **Project**.

 Select the **Auto Retire** check box if you want to retire the project automatically based on inactivity for a specified number of days \(Default: 90 days\).

 You can extend the retirement by moving it back to published or draft state before the versions get cleaned in another 90 Days \(default\).

 If you don’t change the retired status within the specified days, the mined versions are permanently deleted. However, the project definition isn’t deleted. You can opt out of auto retirement by clearing this check box.

 The default value of 90 days can be changed by the administrator in the System Properties. For more information see, [Data cleanup properties](../concept/data-cleanup.md#).

</td></tr><tr><td id="d89337e229">

**Add a KPI dashboard**

</td><td>

Select the check box if you want to add a KPI dashboard. You must then select a dashboard. If you want to create a dashboard, select the **New Dashboard** button. It automatically takes you to the Performance Analytics workspace.

</td></tr></tbody>
</table>3.  Select **Create project**.

    You’re taken to the **Scope your analysis** tab.

4.  You can also select a template to create your project.

    You can filter, sort, or group the templates according to your need.

    If you select an existing template, then after you select the template, you’re taken to the **Review and Mine** page.


**Parent Topic:**[Create a project or template using Project Builder](define-workflow-model.md)


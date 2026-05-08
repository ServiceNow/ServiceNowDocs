---
title: Set objectives for Process Mining projects
description: Define the kind of data or process that you want to view and analyze in your graph. You must select a specific table \(parent table\) that has the data that you want to analyze.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a project or template using Project Builder, Use, Process Mining, Platform Analytics]
---

# Set objectives for Process Mining projects

Define the kind of data or process that you want to view and analyze in your graph. You must select a specific table \(parent table\) that has the data that you want to analyze.

## Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

## Procedure

1.  When you select **Create New Project** on the Projects page, you’re taken to the **Set objectives** tab.

2.  Provide the following details.

    **Note:** If you want to create a project using Agentic AI data, see [Create a project using Agentic AI](project-agentic-ai.md). If you want to create a project using Playbook data, see [Create a project using Playbook data](playbook-project.md).

<table id="choicetable_j24_f5k_nzb"><thead><tr><th align="left" id="d94273e104">

Field

</th><th align="left" id="d94273e107">

Description

</th></tr></thead><tbody><tr><td id="d94273e113">

**Select type**

</td><td>

Choose whether you want to create a project or a template.

</td></tr><tr><td id="d94273e122">

**Template type**

</td><td>

This field is available only if you choose the type as **Template**.Four values are available:

-   Default
-   WFO
-   Vendor Management
-   Digital Portfolio Management
For a template that is not part of WFO, Vendor Management, or Digital Portfolio Management, choose **Default**. For example, to create a Performance Analytics template, select **Default**.

</td></tr><tr><td id="d94273e161">

**Name**

</td><td>

An intuitive name for the project or template you’re creating.

</td></tr><tr><td id="d94273e170">

**Short description**

</td><td>

A short description for the project or template you’re creating.

</td></tr><tr><td id="d94273e180">

**Source Type**

</td><td>

The source for the project or template you’re creating.-   Table: Any database table
-   Report source: Select a table that has reports
-   External data: Select a table that has the imported dataset.
-   Archived data: Select an archived table.
-   Agentic AI data: Select a table with agentic AI data.
-   Playbook: Select a table with playbook data.


</td></tr><tr><td id="d94273e210">

**Table__Note:__ This name changes based on the choice of source you want to analyze.

**

</td><td>

Select a source that you want to base your project on. This list varies depending on the type of source that you’ve selected.

 This field is auto-selected for Agentic AI.

</td></tr><tr><td id="d94273e227">

**Mark as restricted**

</td><td>

Select the check box if you want to limit project access to the owner and the users they explicitly share it with. Administrators and power users don't have access to the mined data unless the project is shared with them. Once a project is marked as restricted, only the owner can clear this field.

When you’re dealing with sensitive data and must restrict access, you can use this option.

</td></tr><tr><td id="d94273e240">

**Auto retire**

</td><td>

This field is available only if you choose the type as **Project**.

 Select the **Auto Retire** check box if you want to retire the project automatically based on inactivity for a specified number of days \(Default: 90 days\).

 You can extend the retirement by moving it back to published or draft state before the versions get cleaned in another 90 Days \(default\).

 If you don’t change the retired status within the specified days, the mined versions are permanently deleted. However, the project definition isn’t deleted. You can opt out of auto retirement by clearing this check box.

 The default value of 90 days can be changed by the administrator in the System Properties. For more information see, [Data cleanup properties](../concept/data-cleanup.md#).

</td></tr><tr><td id="d94273e280">

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


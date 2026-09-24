---
title: Set objectives for Process Mining projects
description: Define the kind of data or process that you want to view and analyze in your graph. You must select a specific table \(parent table\) that has the data that you want to analyze.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/set-objectives.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Create a project or template using Project Builder, Use, Process Mining, Platform Analytics]
---

# Set objectives for Process Mining projects

Define the kind of data or process that you want to view and analyze in your graph. You must select a specific table \(parent table\) that has the data that you want to analyze.

## Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

## Procedure

1.  When you select **Create New Project** on the Projects page, you’re taken to the **Set objectives** tab.

2.  Provide the following details.

    **Note:** If you want to create a project using Agentic AI data, see [Create a project using agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/project-agentic-ai.md). If you want to create a project using Playbook data, see [Create a project using Playbook data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/playbook-project.md).

<table id="choicetable_j24_f5k_nzb"><thead><tr><th align="left" id="d98857e107">

Field

</th><th align="left" id="d98857e110">

Description

</th></tr></thead><tbody><tr><td id="d98857e116">

**Select type**

</td><td>

Choose whether you want to create a project or a template.

</td></tr><tr><td id="d98857e125">

**Template type**

</td><td>

This field is available only if you choose the type as **Template**.

 Select the type of template you want to create.

 -   **Standard**: Shared with everyone in the instance. Standard templates are read-only. Sharing settings can't be changed and the template can't be edited once created. Standard templates can't have filter conditions on their entities.
-   **Custom**: Visible only to the users or groups it's shared with, though anyone with the power user role or higher can see all custom templates. Custom templates can have filter conditions on their entities, which is what makes them suitable for the region-specific or team-specific use case.
 Only power users or higher can create or delete Standard templates. Analysts can view them.

 Analysts and above can create Custom templates. An analyst never sees the **Template type** filed when creating a template. The type is always set to Custom.

</td></tr><tr><td id="d98857e165">

**Name**

</td><td>

An intuitive name for the project or template you’re creating.

</td></tr><tr><td id="d98857e174">

**Short description**

</td><td>

A short description for the project or template you’re creating.

</td></tr><tr><td id="d98857e184">

**Source Type**

</td><td>

The source for the project or template you’re creating.-   Table: Any database table
-   Report source: Select a table that has reports
-   External data: Select a table that has the imported dataset.
-   Archived data: Select an archived table.
-   Agentic AI data: Select a table with agentic AI data.
-   Playbook: Select a table with playbook data.


</td></tr><tr><td id="d98857e214">

**Table__Note:__ This name changes based on the choice of source you want to analyze.

**

</td><td>

Select a source that you want to base your project on. This list varies depending on the type of source that you’ve selected.

 This field is auto-selected for Agentic AI.

</td></tr><tr><td id="d98857e231">

**Mark as restricted**

</td><td>

Select the check box if you want to limit project access to the owner and the users they explicitly share it with. Administrators and power users don't have access to the mined data unless the project is shared with them. Once a project is marked as restricted, only the owner can clear this field.

When you’re dealing with sensitive data and must restrict access, you can use this option.

</td></tr><tr><td id="d98857e244">

**Auto retire**

</td><td>

This field is available only if you choose the type as **Project**.

 Select the **Auto Retire** check box if you want to retire the project automatically based on inactivity for a specified number of days \(Default: 90 days\).

 If you don’t change the retired status within the specified days, the mined versions are permanently deleted. However, the project definition isn’t deleted. You can opt out of auto retirement by clearing this check box.

 The default value of 90 days can be changed by the administrator in the System Properties. For more information see, [Data cleanup properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/data-cleanup.md).

**Note:** If a project has been automatically retired, you can remine it directly. Remining a retired project automatically sets its state to Draft if the project wasn't shared earlier, or to Published if it was shared. Previously, you had to open the project and manually change its state to Draft or Published before you could remine it.

</td></tr><tr><td id="d98857e283">

**Add a KPI dashboard**

</td><td>

Select the check box if you want to add a KPI dashboard. You must then select a dashboard. If you want to create a dashboard, select the **New Dashboard** button. It automatically takes you to the Performance Analytics workspace.

</td></tr></tbody>
</table>3.  Select **Create project**.

    You’re taken to the **Scope your analysis** tab.

4.  You can also select a template to create your project.

    You can filter, sort, or group the templates according to your need.

    If you select an existing template, then after you select the template, you’re taken to the **Review and Mine** page.


**Parent Topic:**[Create a project or template using Project Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/define-workflow-model.md)


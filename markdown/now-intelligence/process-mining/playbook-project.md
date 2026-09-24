---
title: Create a project using Playbook data
description: Use Process Mining to analyze Playbook executions and identify bottlenecks in your workflows. Process Mining works alongside Playbooks configured in Workflow Studio. By analyzing execution logs generated during playbook runs, Process Mining enables post-execution visibility into how human agents are handling playbooks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/playbook-project.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Use, Process Mining, Platform Analytics]
---

# Create a project using Playbook data

Use Process Mining to analyze Playbook executions and identify bottlenecks in your workflows. Process Mining works alongside Playbooks configured in Workflow Studio. By analyzing execution logs generated during playbook runs, Process Mining enables post-execution visibility into how human agents are handling playbooks.

## Before you begin

Role required: pd\_author, pd\_operator, sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin. You must have the playbook.write role.

## About this task

Playbooks are built and configured in Workflow Studio, where you define activities for human agents and set up decision logic based on customer scenarios. When agents execute these playbooks, the system generates execution logs that Process Mining can analyze.

\[Omitted image "workflow-studio.png"\] Alt text: Workflow studio

**Note:** Note the following:

-   Only one playbook can be analyzed at a time.
-   The Analyst workbench provides basic analysis and bottleneck identification only.
-   Summary insights, improvement opportunities, and detailed phase information aren’t yet available.

The key benefits of the feature are as follows:

-   See the full distribution of completion times for an activity or phase, not just the average. You can then tell whether a slow average is caused by consistent slowness or by outliers.
-   Correlate Playbook performance with the attributes of the record that triggered it, such as priority or category.
-   Compare how different Playbook variants perform against the base Playbook, to make informed decisions about variant design.

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  Select **Create New Project** from the projects page.

    The Set objectives tab is displayed.

3.  Provide details on the **Set objectives** tab.

<table id="choicetable_akh_rrs_33c"><thead><tr><th align="left" id="d61009e154">

Field

</th><th align="left" id="d61009e157">

Description

</th></tr></thead><tbody><tr><td id="d61009e163">

**Select type**

</td><td>

Select `Project`.

</td></tr><tr><td id="d61009e175">

**Name**

</td><td>

Provide an intuitive name for the project that you’re creating.

</td></tr><tr><td id="d61009e184">

**Short description**

</td><td>

Provide a short description for the project you’re creating.

</td></tr><tr><td id="d61009e193">

**Source Type**

</td><td>

Select `Playbook` from the list.

</td></tr><tr><td id="d61009e206">

**Playbook**

</td><td>

Select a table with playbook data from the list.

</td></tr><tr><td id="d61009e215">

**Mark as restricted**

</td><td>

Select the check box if you want to limit project access to the owner and the users they explicitly share it with. Administrators and power users don't have access to the mined data unless the project is shared with them. Once a project is marked as restricted, only the owner can clear this field.

When you’re dealing with sensitive data and must restrict access, you can use this option.

</td></tr><tr><td id="d61009e228">

**Auto retire**

</td><td>

This field is available only if you choose the type as **Project**.

 Select the **Auto Retire** check box if you want to retire the project automatically based on inactivity for a specified number of days \(Default: 90 days\).

 If you don’t change the retired status within the specified days, the mined versions are permanently deleted. However, the project definition isn’t deleted. You can opt out of auto retirement by clearing this check box.

 The default value of 90 days can be changed by the administrator in the System Properties. For more information see, [Data cleanup properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/data-cleanup.md).

 **Note:** If a project has been automatically retired, you can remine it directly. Remining a retired project automatically sets its state to Draft if the project wasn't shared earlier, or to Published if it was shared. Previously, you had to open the project and manually change its state to Draft or Published before you could remine it.

</td></tr></tbody>
</table>4.  Select **Create project**.

    The Scope your analysis page is displayed.

    The tab has two tabs:

    -   Filter conditions: Filter conditions are preconfigured. You can add new filters, but can't delete the preconfigured filters.
    -   Breakdowns: Add one or more breakdowns based on attributes of the trigger table.
    **Note:** There are no improvement opportunities for playbook projects.

5.  Select **Review and Mine**, and mine the project.

    \[Omitted image "playbook-new.png"\] Alt text: Playbook project in Analyst workbench

    **Viewing playbook project in Analyst workbench**

    -   The Analyst workbench provides execution metrics for completed playbook runs, including duration, average time per execution, and activity occurrence counts. The Analyst workbench visualizes parallel activities and decision points within the workflow to help you understand how playbooks are being executed.
    -   Select an activity node or a phase, to view the histogram, median, and standard deviation.
    -   Select a breakdown to view its statistics.
    -   In the Playbook Variants panel on the right side of the screen, select the variant you want to analyze.
    -   The data on the workbench updates to reflect the selected variant.
    -   You can see how frequently the selected variant runs, and its average duration, median, and standard deviation. This helps you to assess whether the variant's added activities or routes improve on the base playbook.
    \[Omitted image "playbook-aw.png"\] Alt text: Analyst workbench for playbooks

    **Viewing variants in playbook projects**

    \[Omitted image "playbook-variant.gif"\] Alt text: Playbook variant


**Parent Topic:**[Using Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/use-process-mining.md)


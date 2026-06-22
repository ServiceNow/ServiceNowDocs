---
title: Create a project using Playbook data
description: Use Process Mining to analyze Playbook executions and identify bottlenecks in your workflows. Process Mining works alongside Playbooks configured in Workflow Studio. By analyzing execution logs generated during playbook runs, Process Mining enables post-execution visibility into how human agents are handling playbooks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/playbook-project.html
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Process Mining, Platform Analytics]
---

# Create a project using Playbook data

Use Process Mining to analyze Playbook executions and identify bottlenecks in your workflows. Process Mining works alongside Playbooks configured in Workflow Studio. By analyzing execution logs generated during playbook runs, Process Mining enables post-execution visibility into how human agents are handling playbooks.

## Before you begin

Role required: pd\_author, pd\_operator, sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin. You must have the playbook.write roles.

## About this task

Playbooks are built and configured in Workflow Studio, where you define activities for human agents and set up decision logic based on customer scenarios. When agents execute these playbooks, the system generates execution logs that Process Mining can analyze.

\[Omitted image "workflow-studio.png"\] Alt text: Workflow studio

**Note:** Note the following:

-   Only one playbook can be analyzed at a time.
-   The Analyst workbench provides basic analysis and bottleneck identification only.
-   Summary insights, improvement opportunities, and detailed phase information aren’t yet available.

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  Select **Create New Project** from the projects page.

    The Set objectives tab is displayed.

3.  Provide details on the **Set objectives** tab.

<table id="choicetable_akh_rrs_33c"><thead><tr><th align="left" id="d56788e136">

Field

</th><th align="left" id="d56788e139">

Description

</th></tr></thead><tbody><tr><td id="d56788e145">

**Select type**

</td><td>

Select `Project`.

</td></tr><tr><td id="d56788e157">

**Name**

</td><td>

Provide an intuitive name for the project that you’re creating.

</td></tr><tr><td id="d56788e166">

**Short description**

</td><td>

Provide a short description for the project you’re creating.

</td></tr><tr><td id="d56788e175">

**Source Type**

</td><td>

Select `Playbook` from the list.

</td></tr><tr><td id="d56788e188">

**Playbook**

</td><td>

Select a table with playbook data from the list.

</td></tr><tr><td id="d56788e197">

**Mark as restricted**

</td><td>

Select the check box if you want to limit project access to the owner and the users they explicitly share it with. Administrators and power users don't have access to the mined data unless the project is shared with them. Once a project is marked as restricted, only the owner can clear this field.

When you’re dealing with sensitive data and must restrict access, you can use this option.

</td></tr><tr><td id="d56788e210">

**Auto retire**

</td><td>

This field is available only if you choose the type as **Project**.

 Select the **Auto Retire** check box if you want to retire the project automatically based on inactivity for a specified number of days \(Default: 90 days\).

 You can extend the retirement by moving it back to published or draft state before the versions get cleaned in another 90 Days \(default\).

 If you don’t change the retired status within the specified days, the mined versions are permanently deleted. However, the project definition isn’t deleted. You can opt out of auto retirement by clearing this check box.

 The default value of 90 days can be changed by the administrator in the System Properties. For more information see, [Data cleanup properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/data-cleanup.md).

</td></tr></tbody>
</table>4.  Select **Create project**.

    The Scope your analysis tab is displayed. The filter conditions are preconfigured.

    **Note:** There are no improvement opportunities for playbook projects. All conditions are preconfigured. You can’t edit any condition.

5.  Select **Review and Mine**.

    \[Omitted image "playbook.png"\] Alt text: Playbook project in Analyst workbench

    The Analyst workbench provides execution metrics for completed playbook runs, including duration, average time per execution, and activity occurrence counts. The Analyst workbench visualizes parallel activities and decision points within the workflow to help you understand how playbooks are being executed.


**Parent Topic:**[Using Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/use-process-mining.md)


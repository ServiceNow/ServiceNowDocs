---
title: Create a project using Agentic AI
description: Create a project using Agentic AI data to understand any bottlenecks and inefficiencies caused when using agentic AI in your processes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/project-agentic-ai.html
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Process Mining, Platform Analytics]
---

# Create a project using Agentic AI

Create a project using Agentic AI data to understand any bottlenecks and inefficiencies caused when using agentic AI in your processes.

## Before you begin

Role required: sn.aia.viewer, sn.aia.admin

You must have the Agentic AI plugin installed.

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  Select **Create new project** from the projects page.

    The Set objectives tab is displayed.

    \[Omitted image "agentic-proj-obj.png"\] Alt text: Agentic AI project set up

3.  Provide details on the Set objectives tab.

<table id="choicetable_j24_f5k_nzb"><thead><tr><th align="left" id="d62656e100">

Field

</th><th align="left" id="d62656e103">

Description

</th></tr></thead><tbody><tr><td id="d62656e109">

**Select type**

</td><td>

Select `Project`.

</td></tr><tr><td id="d62656e121">

**Name**

</td><td>

Provide an intuitive name for the project that you’re creating.

</td></tr><tr><td id="d62656e130">

**Short description**

</td><td>

Provide a short description for the project you’re creating.

</td></tr><tr><td id="d62656e139">

**Source Type**

</td><td>

Select `Agentic AI data` from the list.

</td></tr><tr><td id="d62656e152">

**Table**

</td><td>

This is auto-populated \(Execution Plan\).

</td></tr><tr><td id="d62656e161">

**Mark as restricted**

</td><td>

Select the check box if you want to limit project access to the owner and the users they explicitly share it with. Administrators and power users don't have access to the mined data unless the project is shared with them. Once a project is marked as restricted, only the owner can clear this field.

When you’re dealing with sensitive data and must restrict access, you can use this option.

</td></tr><tr><td id="d62656e174">

**Auto retire**

</td><td>

This field is available only if you choose the type as **Project**.

 Select the **Auto Retire** check box if you want to retire the project automatically based on inactivity for a specified number of days \(Default: 90 days\).

 You can extend the retirement by moving it back to published or draft state before the versions get cleaned in another 90 Days \(default\).

 If you don’t change the retired status within the specified days, the mined versions are permanently deleted. However, the project definition isn’t deleted. You can opt out of auto retirement by clearing this check box.

 The default value of 90 days can be changed by the administrator in the System Properties. For more information see, [Data cleanup properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/data-cleanup.md).

</td></tr><tr><td id="d62656e214">

**Add a KPI dashboard**

</td><td>

Select the check box if you want to add a KPI dashboard. You must then select a dashboard. If you want to create a dashboard, select the **New Dashboard** button. It automatically takes you to the Performance Analytics workspace.

</td></tr><tr><td id="d62656e229">

**Quick start**

</td><td>

The template for Agentic AI project is auto-selected.

</td></tr></tbody>
</table>4.  Select **Create project**.

    A dialog box is displayed asking your confirmation to proceed with the template. Select **Yes**.

    You will be taken to the **Review and mine** tab.

    **Note:** You can go to any of the tabs and edit any information you want. No improvement opportunities are added by default. You can add if required. The touchpoint and idle-time metrics are grayed out for Agentic AI projects.

    After you mine your project, you cannot use the some analysis such as root cause analysis, work notes analysis, and clustering. Task mining is also not available for Agentic AI projects.

    \[Omitted image "agentic-ai-project.png"\] Alt text: Agentic AI project


**Parent Topic:**[Using Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/use-process-mining.md)


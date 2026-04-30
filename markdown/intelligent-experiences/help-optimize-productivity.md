---
title: Platform Help optimize team productivity agentic workflow
description: Use the Platform Help optimize team productivity AI agents agentic workflow to gather relevant information about tasks automatically and make decisions about priorities and assignments.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 7
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# Platform Help optimize team productivity agentic workflow

Use the Platform Help optimize team productivity AI agents agentic workflow to gather relevant information about tasks automatically and make decisions about priorities and assignments.

## Help optimize team productivity overview

The Help optimize team productivity agentic workflow offers multiple capabilities that can enhance your team's performance. Improving assignments based on previous work and balancing workloads, the agentic workflow can address problems that traditional work assignment rules may have.

The agentic workflow performs the following tasks:

-   Analyzes historical performance of team members
-   Calculates workloads relative to each team member's typical capacity
-   Enables proactive team management with data-driven insights

The agents, tools, and triggers that are associated with the Help optimize team productivity agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](../task/activate-aia-use-case.md) by making triggers active and setting the display settings to include the Now Assist panel. If you want to change this agentic workflow's instructions, you must [duplicate it](../task/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

## Prerequisites and setup

To access this workflow, you must have Now Assist for Platform installed on your instance, which you can get if you install any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

## Role masking

Required role: sn\_uxc\_gen\_ai.platform\_ai\_help\_allocate\_work.

[Role masking](aia-role-masking.md) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](../task/define-sec-controls-aw.md).

In the data access settings, you must also add the necessary roles to enable reading of the tables for records assigned to team members. For example, you can add the itil role to the agentic workflow's list of approved roles so that it can access Incident records.

## Additional configuration

You can change different settings related to the agentic workflow by changing values for the Now Assist Skill Config Var Set. To access the variable set and make changes, do the following while in the Platform AI Agents and Skills scope:

-   Go to the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table.
-   Open the record named **Optimal Ticket Assignment**.
-   In the Now Assist Skill Config Var Set related list, select **Work Allocator**.
-   Edit the variable values.
-   Save or update the record.

The Help optimize team productivity configuration variable sets include the following variables.

<table><thead><tr><th>

Config field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tickets per batch

</td><td>

The number of tickets processed by the agentic workflow for evaluation.

 Default: 25

</td></tr><tr><td>

Metrics Calculation Window

</td><td>

How many days back to include in metric calculations.

 Default: 600

</td></tr><tr><td>

Assignment Group

</td><td>

The assignment group whose tickets are used for evaluation, analysis, and recommendations.

</td></tr><tr><td>

Table for Query

</td><td>

The table used to gather information about the work assigned to team members.

</td></tr><tr><td>

Backlog Ticket Query

</td><td>

Filter conditions for determining what counts as "backlog" work for team members to complete.

</td></tr><tr><td>

Similarity Score Table

</td><td>

The table used for gathering information about other work that has been previously assigned to team members.

</td></tr><tr><td>

Similarity Score Fields

</td><td>

Fields to consider for calculating which tasks are similar to the one that needs assigning. For example, selecting category and subcategory as similarity score fields includes those fields in calculating whether a team member has worked on similar assignments within the metric calculation window.

</td></tr></tbody>
</table><table><thead><tr><th>

Config field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable scheduled job

</td><td>

Enable the agentic workflow to run on its own using a scheduled job.

</td></tr><tr><td>

Assignment Group

</td><td>

The assignment group whose tickets are used for evaluation, analysis, and recommendations.

</td></tr><tr><td>

Scheduled job

</td><td>

The name of the scheduled job that runs to trigger the agentic workflow.

</td></tr><tr><td>

Scheduler frequency

</td><td>

How often the scheduled job runs and triggers the agentic workflow.

</td></tr></tbody>
</table>## Accessing the Help optimize team productivity agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Help optimize team productivity**.

The first step of the guided setup includes a complete list of included AI agents. Selecting the name of an AI agent opens it in a new browser tab, where you can see the full description, role, list of steps, and tools. Tools are displayed in the second step of the AI agent guided setup, Add tools and information.

## In-product agentic AI and UI actions

Agentic workflows can be accessed in the Core UI and in workspaces in the AI Activity panel. From there, you can track their progress, provide or review input, and see the results of the work performed. For more information, see [In-product agentic AI](in-product-agentic-ai.md) for more details about the AI Activity panel.

To enable users to access agentic workflows with UI actions, you can open the agentic workflow in AI Agent Studio and navigate to the **Select channels and access** step. You can select a UI action as a possible way to access the workflow

If you don't see your UI actions after configuring it in AI Agent Studio, ensure that the property **com.glide.agentic\_processes\_view.enabled** is set to `true`. See [Enable the in-product experience for agentic workflows](../task/enable-inproduct-aia.md).

## Testing the Help optimize team productivity agentic workflow

You can manually test an agentic workflow execution or access on the Testing page of AI Agent Studio if you have the sn.aia\_admin role and all other roles configured [in the security controls](../task/define-sec-controls-aw.md). Start a manual test, select a test type and the name of the workflow, and use utterances in the Task field like the following samples. See [Test an agentic workflow execution](../task/test-aia-use-case.md).

If you want to evaluate the agentic workflow over many different execution logs, run an [automated evaluation](../task/execute-aia-eval.md).

## Sample utterance

After the workflow has been activated in AI Agent Studio, enter "Give me optimized assignment evaluations for the Software assignment group" or similar phrases in the Now Assist panel to trigger the workflow. You must name the specific assignment group you're allocating work for.

You must have the sn.now\_assist\_panel\_user role to run the workflow. You can also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin role.

## AI agents used in the Help optimize team productivity agentic workflow

The following table lists the agents that are used in the Help optimize team productivity agentic workflow.

**Important:** In the Define availability step of each AI agent's guided setup, make sure that the Status toggle is enabled to activate the AI agent.

|AI agent name|AI agent description|Role required|
|-------------|--------------------|-------------|
|Work Allocator AI Agent|Streamlines ticket management by automatically fetching backlog tickets, evaluating agent workloads and performance metrics, and assigning tickets to agents in a way that optimizes distribution and operational efficiency.|sn\_uxc\_gen\_ai.platform\_ai\_help\_allocate\_work|

## Other Platform agentic workflows

For more information on other agentic workflows that are associated with the Platform workflow, see [Platform agentic workflows](platform-use-cases.md).


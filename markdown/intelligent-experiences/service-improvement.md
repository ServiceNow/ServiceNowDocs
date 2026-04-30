---
title: Platform Identify ways to improve service agentic workflow
description: Use the Platform Identify ways to improve service agentic workflow to analyze feedback, performance metrics, and historical trends that identify areas for service improvement.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 6
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# Platform Identify ways to improve service agentic workflow

Use the Platform Identify ways to improve service agentic workflow to analyze feedback, performance metrics, and historical trends that identify areas for service improvement.

## Identify ways to improve service overview

The Identify ways to improve service agentic workflow optimizes service delivery and customer satisfaction by analyzing feedback, metrics, and trends to provide actionable process improvement recommendations. After the analysis is generated, you can continue the conversation to ask follow-up questions or download the analysis as a PDF or Word document.

The Now Assist applications provide the agents, tools, and triggers for the Identify ways to improve service agentic workflow. You can [activate the agentic workflow template](../task/activate-aia-use-case.md) by making triggers active and setting the display settings to include the Now Assist panel. To change this agentic workflow's instructions, [duplicate it](../task/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version instead.

## Prerequisites and setup

To access this workflow, you must have Now Assist for Platform installed on your instance. You can get this by installing any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

Because this agentic workflow relies on survey data, you must have Assessment records associated with task tables to analyze.

## Role masking

Required role: sn\_uxc\_gen\_ai.platform\_ai\_improve\_services.

[Role masking](aia-role-masking.md) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](../task/define-sec-controls-aw.md).

In the data access settings, add the necessary roles to enable reading of the Assessment table and other required tables. For example, add the itil role to the agentic workflow's list of approved roles so it can access Incident records.

## Additional configuration

You can change agentic workflow settings by changing values for the Now Assist Skill Config Var Set. To access the variable set and make changes, do the following while in the Platform AI Agents and Skills scope:

-   Go to the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table.
-   Open the record named **Identify ways to improve service**.
-   In the Now Assist Skill Config Var Set related list, select **Survey analysis input config**.
-   Edit the variable values.
-   Save or update the record.

<table><thead><tr><th>

Config field

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

Maximum number of records

</td><td>

Maximum number of records included in analysis

</td><td>

500

</td></tr><tr><td>

Analysis Time Frame

</td><td>

Time range, in months, for the survey analyzer to examine records to identify trends. Users can specify smaller ranges when running the agentic workflow, but this value defines the maximum limit.

</td><td>

3

</td></tr></tbody>
</table>## Accessing the Identify ways to improve service agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Identify ways to improve service**.

The first step of the guided setup includes a complete list of included AI agents. Selecting an AI agent name opens it in a new browser tab, where you can see the full description, role, list of steps, and tools. Tools are displayed in the second step of the AI agent guided setup, Add tools and information.

## In-product agentic AI and UI actions

You can access agentic workflows in the Core UI and in workspaces in the AI Activity panel. From there, you can track their progress, provide or review input, and see the results of the work performed. For more information, see [In-product agentic AI](in-product-agentic-ai.md) for more details about the AI Activity panel.

To enable users to access agentic workflows with UI actions, open the agentic workflow in AI Agent Studio and navigate to the **Select channels and access** step. You can select a UI action as a possible way to access the workflow

If you don't see your UI actions after configuring it in AI Agent Studio, verify that the property **com.glide.agentic\_processes\_view.enabled** is set to `true`. See [Enable the in-product experience for agentic workflows](../task/enable-inproduct-aia.md).

## Testing the Identify ways to improve service agentic workflow

You can manually test an agentic workflow execution or access on the Testing page of AI Agent Studio if you have the sn.aia\_admin role and all other roles configured [in the security controls](../task/define-sec-controls-aw.md). Start a manual test, select a test type and the workflow name, and use utterances in the Task field like the following samples. See [Test an agentic workflow execution](../task/test-aia-use-case.md).

To evaluate the agentic workflow over many different execution logs, run an [automated evaluation](../task/execute-aia-eval.md).

## Sample utterance

After the workflow is activated in AI Agent Studio, enter similar phrases to the following in the Now Assist panel to trigger the workflow. You can also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin role.

-   Make suggestions for continuous service improvement based on surveys within the last 3 months
-   Summarize surveys to improve services within the last 2 years
-   Give ideas for improving case resolution based on Post-Case survey results over the last month

## AI agents used in the Identify ways to improve service agentic workflow

The following table lists the agents used in the Identify ways to improve service agentic workflow.

**Important:** In the Select channels and access of each AI agent's guided setup, verify that the Status toggle is enabled to activate the AI agent.

|AI agent name|AI agent description|Role required|
|-------------|--------------------|-------------|
|Survey Analysis AI agent|Acquires survey data within the specified time range and analyzes it for ways to improve services|sn\_uxc\_gen\_ai.platform\_ai\_improve\_services|

## Other Platform agentic workflows

For more information on other agentic workflows associated with the Platform workflow, see [Platform agentic workflows](platform-use-cases.md).


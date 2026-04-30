---
title: Platform Analyze task trends agentic workflow
description: Use the Platform Analyze task trends AI agents agentic workflow to detect recurring task patterns so that you can flag and resolve them before they escalate.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-11-18"
reading_time_minutes: 7
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# Platform Analyze task trends agentic workflow

Use the Platform Analyze task trends AI agents agentic workflow to detect recurring task patterns so that you can flag and resolve them before they escalate.

## Analyze task trends overview

The Analyze task trends agentic workflow can help enhance task management by detecting recurring patterns, predicting disruptions, and enabling a proactive resolution to reduce downtime and improve reliability. Tasks are grouped and indexed by the Large Language Model \(LLM\) so that the LLM can analyze common recurring issues and root patterns. The LLM then generates resolution recommendations based on the analysis and displays it to you. You can provide feedback for the LLM to guide additional analysis, and the conversation ends after you confirm satisfaction with the results.

The agents, tools, and triggers that are associated with the Analyze task trends agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](../task/activate-aia-use-case.md) by making triggers active and setting the display settings to include the Now Assist panel. If you want to change this agentic workflow's instructions, you must [duplicate it](../task/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

## Prerequisites and setup

To access this workflow, you must have Now Assist for Platform installed on your instance, which you can get if you install any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

For this agentic workflow to behave as expected, you should have at least 500 records on your task table.

You must also configure Group Action Framework \(GAF\). See [Group Action Framework](group-action-framework.md) for more information on what GAF is and how to set it up. The Incident table is the default table for this workflow, but you can configure GAF for other task tables such as Case or HR Case.

## Role masking

Required role: sn\_uxc\_gen\_ai.platform\_ai\_analyze\_trnds.

[Role masking](aia-role-masking.md) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](../task/define-sec-controls-aw.md).

In the data access settings, you must also add the necessary roles to enable reading of the tables for the records you want to access for trend analysis. For example, you can add the itil role to the agentic workflow's list of approved roles so that it can access Incident records.

## Additional configuration

You can change different settings related to the agentic workflow by changing values for the Now Assist Skill Config Var Set. To access the variable set and make changes, do the following while in the Platform AI Agents and Skills scope:

-   Go to the Now Assist Skill Config \[sn\_nowassist\_skill\_config\] table.
-   Open the record named **Analyze Task Trends**.
-   In the Now Assist Skill Config Var Set related list, select **Task Trends Input Config**.
-   Edit the variable values.
-   Save or update the record.

<table><thead><tr><th>

Config field

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

Analysis Time Frame

</td><td>

Range of time, in months, for the trends analyzer to look at records to identify trends. You can specify smaller ranges when running the agentic workflow, but this value defines the maximum limit.

</td><td>

3

</td></tr><tr><td>

GAF Record Limit

</td><td>

Number of records analyzed per GAF record grouping. See the preceding **Prerequisites and setup** section.

</td><td>

8

</td></tr></tbody>
</table>## Accessing the Analyze task trends agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Analyze task trends**.

The first step of the guided setup includes a complete list of included AI agents. Selecting the name of an AI agent opens it in a new browser tab, where you can see the full description, role, list of steps, and tools. Tools are displayed in the second step of the AI agent guided setup, Add tools and information.

## In-product agentic AI and UI actions

Agentic workflows can be accessed in the Core UI and in workspaces in the AI Workflows panel. From there, you can track their progress, provide or review input, and see the results of the work performed. For more information, see [In-product agentic AI](in-product-agentic-ai.md) for more details about the AI Workflows panel.

To enable users to access agentic workflows with UI actions, you can open the agentic workflow in AI Agent Studio and navigate to the **Select channels and access** step. You can select a UI action as a possible way to access the workflow

If you don't see your UI actions after configuring it in AI Agent Studio, ensure that the property **com.glide.agentic\_processes\_view.enabled** is set to `true`.

## Testing the Analyze task trends agentic workflow

You can manually test an agentic workflow execution or access on the Testing page of AI Agent Studio if you have the sn.aia\_admin role and all other roles configured [in the security controls](../task/define-sec-controls-aw.md). Start a manual test, select a test type and the name of the workflow, and use utterances in the Task field like the following samples. See [Test an agentic workflow execution](../task/test-aia-use-case.md).

If you want to evaluate the agentic workflow over many different execution logs, run an [automated evaluation](../task/execute-aia-eval.md).

## Sample utterance

After the workflow has been activated in AI Agent Studio, similar queries to the following to run the agentic workflow in the Now Assist panel. You can also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin role.

Each utterance must include the name of the table and the time frame to analyze. If the utterance doesn’t include these things, the agentic workflow prompts you for more information.

The time frame specified by the user can’t exceed the maximum value set by the Analysis time frame configuration.

-   Analyze incident trends related to payment issues within the last two months
-   Analyze case trends within the last month
-   Analyze HR case trends with High Priority within the last two years
-   Analyze incident and problem trends within the last two weeks

## Troubleshooting

When running this agentic workflow, it’s possible to see an error that states "I couldn't analyze as I didn't have the required resources." This error occurs when GAF isn’t configured for the table you want to analyze. See [Configure Group Action Framework](../task/configure-gaf.md) for steps to configure GAF for the table. If you’re still having issues after GAF is configured, reach out to Now Support.

## AI agents used in the Analyze task trends agentic workflow

The following table lists the agents that are used in the Analyze task trends agentic workflow.

**Important:** In the Select channels and status step of each AI agent's guided setup, make sure that the Status toggle is enabled to activate the AI agent.

|AI agent name|AI agent description|Role required|
|-------------|--------------------|-------------|
|Issue trend analysis AI agent|Analyzes grouped task data to identify recurring issues and root causes. Provides detailed, actionable recommendations using structured analysis.|sn\_uxc\_gen\_ai.platform\_ai\_analyze\_trnds|

## Other Platform agentic workflows

For more information on other agentic workflows that are associated with the Platform workflow, see [Platform agentic workflows](platform-use-cases.md).


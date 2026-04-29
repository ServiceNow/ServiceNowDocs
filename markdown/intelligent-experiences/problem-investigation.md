---
title: Platform Investigate problems agentic workflow
description: Use the Platform Investigate problems AI agents agentic workflow to perform root cause and risk assessments so that you can create an actionable resolution plan for a problem.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 6
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# Platform Investigate problems agentic workflow

Use the Platform Investigate problems AI agents agentic workflow to perform root cause and risk assessments so that you can create an actionable resolution plan for a problem.

## Investigate problems overview

The Investigate problems agentic workflow can help to assist agents and subject matter experts \(SMEs\) in investigating problems in their IT landscape. A problem can be associated with many incidents, and any investigator must be aware of a large number of details when looking at a problem. The agentic workflow can help provide insights from the incident and problem details and suggest plans or possible solutions.

The agents, tools, and triggers that are associated with the investigate problems agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](../task/activate-aia-use-case.md) by making triggers active and setting the display settings to include the Now Assist panel. If you want to change this agentic workflow's instructions, you must [duplicate it](../task/clone-aia-usecase.md), adjust the settings to suit your specific needs, and activate the duplicated version of the agentic workflow instead.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](../../ai-implementation/concept/ai-native-sku-overview.md).

## Prerequisites and setup

To access this workflow, you must have Now Assist for Platform installed on your instance, which you can get if you install any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

Because this agentic workflow analyzes problems and incidents related to those problems, you must have records on the Problem and Incident table.

## Role masking

Required role: sn\_uxc\_gen\_ai.platform\_ai\_problem\_investigator.

Agentic workflows and their AI agents use [role masking](aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](../task/define-sec-controls-aw.md).

In the data access settings, you must also add the necessary roles to enable reading of the tables for Problems and related records. For example, you can add the itil role to the agentic workflow's list of approved roles so that it can access Incident records.

## Accessing the Investigate problems agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Investigate problems**.

The first step of the guided setup includes a complete list of included AI agents. Selecting the name of an AI agent opens it in a new browser tab, where you can see the full description, role, list of steps, and tools. Tools are displayed in the second step of the AI agent guided setup, Add tools and information.

## In-product agentic AI and UI actions

Agentic workflows can be accessed in the Core UI and in workspaces in the AI Activity panel. From there, you can track their progress, provide or review input, and see the results of the work performed. For more information, see [In-product agentic AI](in-product-agentic-ai.md) for more details about the AI Activity panel.

To enable users to access agentic workflows with UI actions, you can open the agentic workflow in AI Agent Studio and navigate to the **Select channels and access** step. You can select a UI action as a possible way to access the workflow

If you don't see your UI actions after configuring it in AI Agent Studio, ensure that the property **com.glide.agentic\_processes\_view.enabled** is set to `true`. See [Enable the in-product experience for agentic workflows](../task/enable-inproduct-aia.md).

## Testing the Investigate problems agentic workflow

You can manually test an agentic workflow execution or access on the Testing page of AI Agent Studio if you have the sn.aia\_admin role and all other roles configured [in the security controls](../task/define-sec-controls-aw.md). Start a manual test, select a test type and the name of the workflow, and use utterances in the Task field like the following samples. See [Test an agentic workflow execution](../task/test-aia-use-case.md).

If you want to evaluate the agentic workflow over many different execution logs, run an [automated evaluation](../task/execute-aia-eval.md).

## Sample utterance

After the workflow has been activated in AI Agent Studio, enter `investigate the problem PRB001` or similar phrases in the Now Assist panel to trigger the workflow. You can also run this workflow on the Testing page of AI Agent Studio with the same utterance in the Task field if you have the sn.aia\_admin role.

## Troubleshooting

If a Problem has a large number of related incidents, you may run into an error that states "This model's maximum context length is 128000 tokens. However, your messages resulted in \[X\] tokens. Please reduce the length of the messages." This maximum token count is in place for all Now Assist skills, so there is currently no way to work around this error. You can try the agentic workflow again using a different Problem.

## AI agents used in the Investigate problems agentic workflow

The following table lists the agents that are used in the Investigate problems agentic workflow.

**Important:** In the Define availability step of each AI agent's guided setup, make sure that the Status toggle is enabled to activate the AI agent.

|AI agent name|AI agent description|
|-------------|--------------------|
|Problem investigation AI agent|Identifies the root causes, performs an impact assessment, and plans resolutions.|

## Other Platform agentic workflows

For more information on other agentic workflows associated with the Platform workflow, see [Platform agentic workflows](platform-use-cases.md).


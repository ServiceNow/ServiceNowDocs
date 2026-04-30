---
title: Platform Propose survey responses agentic workflow
description: Use the Platform Propose survey responses AI agents agentic workflow to assist requesters in completing surveys.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-11-18"
reading_time_minutes: 5
breadcrumb: [Platform agentic workflows, Now Assist agentic workflows, Now Assist AI assets, Enable AI experiences]
---

# Platform Propose survey responses agentic workflow

Use the Platform Propose survey responses AI agents agentic workflow to assist requesters in completing surveys.

## Propose survey responses overview

The Propose survey responses agentic workflow can help simplify and increase survey responses. Many callers end up not filling out surveys after requests have been fulfilled, and this agentic workflow helps them to make informed decisions to answer survey questions quickly.

When this agentic workflow and trigger are activated, the assignee receives an email with AI-suggested answers to their survey based on the associated Incident or Request. They then have the option to accept the AI-generated answers with a link at the bottom of the email. They can also choose to fill out the survey manually.

The agents, tools, and triggers that are associated with the Propose survey responses agentic workflow are provided by Now Assist applications. You can [activate the agentic workflow template](../task/activate-aia-use-case.md) by making the trigger active. If you want to change this agentic workflow's instructions, you must [duplicate it](../task/clone-aia-usecase.md), adjust the settings to suit your needs, and activate the duplicated version of the agentic workflow instead.

## Prerequisites and setup

To access this workflow, you must have Now Assist for Platform installed on your instance, which you can get if you install any other Now Assist application, such as Now Assist for IT Service Management \(ITSM\).

You can use this workflow for any survey triggered on the Incident or Request table. For example, this agentic workflow can be used by the Short Customer Satisfaction Survey with Smiley Face when an Incident is closed. You can change existing surveys, and the agentic workflow can still propose answers. The agentic workflow can also be used for custom surveys triggered by the Incident or Request table as long as there’s a trigger associated with the survey. See [Configure a trigger condition for a survey](https://www.servicenow.com/docs/access?context=t_CreateATriggerCondition&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for instructions on adding a trigger to a survey.

Propose survey responses isn’t available for Now Assist panel.

## Role masking

Required role: sn\_uxc\_gen\_ai.platform\_ai\_survey\_response.

[Role masking](aia-role-masking.md) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](../task/define-sec-controls-aw.md).

In the data access settings, you must also add the necessary roles to enable reading of survey tables and other related tables.

## Accessing the Propose survey responses agentic workflow

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Propose survey responses**.

The first step of the guided setup includes a complete list of included AI agents. Selecting the name of an AI agent opens it in a new browser tab, where you can see the full description, role, list of steps, and tools. Tools are displayed in the second step of the AI agent guided setup, Add tools and information.

## In-product agentic AI and UI actions

Agentic workflows can be accessed in the Core UI and in workspaces in the AI Activity panel. From there, you can track their progress, provide or review input, and see the results of the work performed. For more information, see [In-product agentic AI](in-product-agentic-ai.md) for more details about the AI Activity panel.

To enable users to access agentic workflows with UI actions, you can open the agentic workflow in AI Agent Studio and navigate to the **Select channels and access** step. You can select a UI action as a possible way to access the workflow

If you don't see your UI actions after configuring it in AI Agent Studio, ensure that the property **com.glide.agentic\_processes\_view.enabled** is set to `true`. See [Enable the in-product experience for agentic workflows](../task/enable-inproduct-aia.md).

## Sample utterance

After the workflow has been activated in AI Agent Studio, you need to set a trigger for the workflow to run. This workflow cannot be triggered from the Now Assist panel.

If you want to test the agentic workflow in AI Agent Studio and you have the sn.aia\_admin role, enter the following phrase in the Testing page in the Task field: `Help me with survey AINST00XXXX. List of fields to extract inc/case/req details: number, short_description, description, calendar_stc, escalation, reopen_count, close_code, close_notes, state, priority, caller_id`. You must include the list of fields to extract.

## AI agents used in the Propose survey responses agentic workflow

The following table lists the agents that are used in the Propose survey responses agentic workflow.

**Important:** In the Define availability step of each AI agent's guided setup, make sure that the Status toggle is enabled to activate the AI agent.

|AI agent name|AI agent description|Role required|
|-------------|--------------------|-------------|
|Survey response suggestion AI agent|Suggests answers to questions based on record details.|sn\_uxc\_gen\_ai.platform\_ai\_survey\_response|
|Survey filling data collection AI agent|Collects the data related to the record and the survey questions to gather feedback.|sn\_uxc\_gen\_ai.platform\_ai\_survey\_response|

## Other Platform agentic workflows

For more information on other agentic workflows that are associated with the Platform workflow, see [Platform agentic workflows](platform-use-cases.md).


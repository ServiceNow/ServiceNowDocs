---
title: IT Service Management AI agent collection Generate change request plans agentic workflow
description: Use the Change request planning AI agent team to monitor similar change requests autonomously and generate the necessary plans. This approach may help reduce the time required for scheduling changes and managing change-related risks.
locale: en-US
release: xanadu
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2025-03-26"
reading_time_minutes: 2
keywords: [Now Assist, Agentic AI]
breadcrumb: [Use agentic workflows in ITSM, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection Generate change request plans agentic workflow

Use the Change request planning AI agent team to monitor similar change requests autonomously and generate the necessary plans. This approach may help reduce the time required for scheduling changes and managing change-related risks.

## Generate change request plans agentic workflow overview

Generate the desired change plans using a team of AI agents in the Generate change request plans agentic workflow.

To modify the Generate change request plans agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## Generate change request plans agentic workflow

Autonomously generate the implementation, backout, or test change plans for a given change request number using similar change requests. After generating the plans, complete the plan execution by flushing the cache.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Change request planning**.

## Change request planning AI agents

In the Generate change request plans agentic workflow, use specific AI agents for each type of planner to generate the desired plans.

**Important:** In the Define availability screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

|AI agent|AI agent role|
|--------|-------------|
|Change implementation plan AI agent|Collaborates with the user to create a step-by-step implementation plan and revises it based on the feedback.|
|Change backout plan AI agent|Collaborates with the user to create a step-by-step backout plan and revises it based on the feedback.|
|Change test plan AI agent|Collaborates with the user to create a step-by-step test plan and revises it based on the feedback.|
|Change risk and impact analysis AI agent|Analyzes the potential risk and impact of a change request.|
|Change justification proposal AI agent|Proposes justification for a change request.|
|Finish change plan AI agent|Flushes the cache and informs the user that the execution completed successfully.|

## Generating a change plan

In the use agentic workflow:

1.  Review the information in the Describe and connect screen and in the Define trigger screen, make the necessary updates, and then select **Save and Continue**.
2.  In the Select display screen:

    1.  Choose where you want the use case output to be displayed.
    2.  Use the arrow next to it to add roles that can access the use case.

        **Note:** The itil role is added by default.

    3.  Select **Save and test**.

        The agent executes the request for the use case.

    **Example of a Generate change request plans agentic workflow output in the ServiceNow StudioAI Agent Studio**

    ![Generate change request plans agentic workflow output.](../image/now-assist-itsm-aiagents-change-imp-nap.png)


In the AI Agent Studio, the human agent gets notified as soon as the report gets generated so that they can follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).

**Parent Topic:**[Using agentic workflows in Now Assist for ITSM](now-assist-itsm-ai-agents-use-cases.md)


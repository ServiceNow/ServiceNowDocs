---
title: IT Service Management AI agent collection Generate change request plans agentic workflow
description: Use the Change request planning AI agent team to monitor similar change requests autonomously and generate the necessary plans. This approach may help reduce the time required for scheduling changes and managing change-related risks.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [ITSM, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection Generate change request plans agentic workflow

Use the Change request planning AI agent team to monitor similar change requests autonomously and generate the necessary plans. This approach may help reduce the time required for scheduling changes and managing change-related risks.

## Generate change request plans agentic workflow overview

Generate the desired change plans using a team of AI agents in the Generate change request plans agentic workflow.

To modify the Generate change request plans agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

**Important:** In the Edit trigger form, make sure that the **Active** button is turned on to enable the AI agent to trigger autonomously.

## Generate change request plans agentic workflow

Autonomously generate the implementation, backout, or test change plans for a given change request number using similar change requests. After generating the plans, complete the plan execution by flushing the cache.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Change request planning**.

## AI agent used in the Change request plans agentic workflow

Use the Change request plans AI agent to create implementation, backout, and test plans and revise them for feedback. You can also do the following with this agent:

-   Analyze the potential risk and impact of a change request.
-   Propose justification for a change request.

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

    ![Generate change request plans agentic workflow output.](../image/now-assist-itsm-aiagents-change-plan-nap.png)


In the AI Agent Studio, the human agent gets notified as soon as the report gets generated so that they can follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).


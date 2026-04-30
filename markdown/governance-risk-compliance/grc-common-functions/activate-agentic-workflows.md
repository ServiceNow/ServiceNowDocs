---
title: Activate agentic workflows in Now Assist for Integrated Risk Management \(IRM\)
description: You must activate agentic workflows that contain a set of LLM instructions with one or more AI agents to execute tasks.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Configure, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Activate agentic workflows in Now Assist for Integrated Risk Management \(IRM\)

You must activate agentic workflows that contain a set of LLM instructions with one or more AI agents to execute tasks.

## Before you begin

Install the Now Assist for IRM plugin \(sn\_irm\_gen\_ai\).

Role required: sn\_nowassist\_admin.nsa\_admin or sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.

2.  Select the agentic workflow that you want to activate.

3.  On the agentic workflow page, under the **Add AI agents that can perform these steps** section, select an AI agent.

    ![Select an AI agent.](../image/agentic-wf-connect-ai-agents.png)

4.  On the AI agent page, perform the following steps:

    1.  Under the **Define the specialty**, review the details and select **Continue** to proceed to the next section.

    2.  Under the **Add tools and information** section, review the details and select **Continue** to proceed to the next section.

    3.  Under the **Define security controls** section, review the details in **Define user access** and **Define data access** sub-sections, and select **Continue**.

    4.  Under the **Add triggers** section, review the details and select **Continue** to proceed to the next section.

    5.  Under the **Select channels and status** section, in the **Activation status** section, turn on the **This AI agent is active** toggle switch to make the AI agent available in related workflows.

        ![Status of the AI agent.](../image/ai-agent-status-active.png)

    6.  Select **Save and test**.

    7.  On the Test AI reasoning page, select the **Version** and then enter details for **Task**.

    8.  Select **Start test** to initiate the testing of the AI agent.

5.  Repeat steps 4 for all the AI agents \(if available\).

6.  On the agentic workflow page, perform the following steps:

    1.  Under the **Define key requirements**, review the details and select **Continue** to proceed to the next section.

    2.  Under the **Define security controls** section, review the details in **Define user access** and **Define data access** sub-sections, and select **Continue**.

    3.  Under the **Add triggers** section, review the details and select **Continue** to proceed to the next section.

    4.  Under the **Select channels and status** section, set the display as active.

    5.  Select **Save and test**.

    6.  On the Test AI reasoning page, select the **Version** and then enter details for **Task**.

    7.  Select **Start test** to initiate the testing of the agentic workflow.


## Result

The agentic workflow and all the AI agents within the workflow are activated.


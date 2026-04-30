---
title: Identify risks for an entity using Now Assist for IRM
description: Identify and consolidate risks using the Risk Suggestion AI agent through a conversational assistant. This feature helps streamline risk discovery, eliminate duplicates, and provide a comprehensive list of risks relevant to the entity.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-11-13"
reading_time_minutes: 1
breadcrumb: [Agentic workflows, Use agentic AI, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Identify risks for an entity using Now Assist for IRM

Identify and consolidate risks using the Risk Suggestion AI agent through a conversational assistant. This feature helps streamline risk discovery, eliminate duplicates, and provide a comprehensive list of risks relevant to the entity.

## Before you begin

**Important:** This agent is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Role required: sn\_grc\_sharegenai.risk\_suggestion\_aiagent\_user

Make sure that the following prerequisites are met to use this feature:

-   Now Assist for IRM and any Workspace must be installed.
-   Suggest potential risks workflow and Risk Suggestion AI agent must be activated. For more, refer to [Activate agentic workflows in Now Assist for Integrated Risk Management \(IRM\)](../../grc-common/task/activate-agentic-workflows.md).

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace**.

    You can also navigate to your required Workspace.

2.  Select the list ![](../../grc-compliance-case-mgmt/image/list-icon.png) icon.

3.  From the list, navigate to **Library** &gt; **Entities**.

4.  Select the entity to identify potential risks.

5.  Navigate to the **Risks** tab and select **Suggested risks**.

6.  Select the **Suggest risks** button.![Suggest risks button.](../image/suggest-risks.png)

    A conversational assistant opens within the Now Assist panel.

7.  Interact with the conversational AI agent by responding to its questions to identify potential risks.![Now Assist panel displaying the conversational chat.](../image/risk-suggestion-ai-agent.png)

    The agent automatically pulls the entity context, guides you through risk domain selection, and surfaces relevant risks from internal, industry, and external sources. During this process, it automatically removes any duplicate suggestions that exist.

8.  Review the consolidated list of suggested risks in the panel before proceeding.

9.  Choose whether to create the suggested risks as triage records when prompted.

    If you select **Yes**, the risks are added as triage records.

10. Review the listed risks for accuracy and make any necessary changes before creating them.![Suggested risk records](../image/traige-risk-records.png)

    Risks identified from existing risk statements are listed under Risks from risk statements. Any newly identified Risks are listed under the Ad-hoc risks type.

11. Choose the required risks and select **Create risk**.

    The selected risks are added and appear in the **Directly related risks** section.

12. Select **Suggest risk** button to reinitiate the same process.

13. To delete the suggested risks, choose the required risks, and select **Delete**.



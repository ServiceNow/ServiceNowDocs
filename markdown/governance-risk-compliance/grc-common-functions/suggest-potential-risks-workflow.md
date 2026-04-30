---
title: Suggest potential risks agentic workflow
description: The Suggest potential risks workflow uses AI to identify and consolidate risks from multiple sources. It replaces manual, workshop-based risk discovery with a faster, consistent, and data-driven process that stays current with new regulations and trends.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-11-13"
reading_time_minutes: 2
breadcrumb: [Explore, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Suggest potential risks agentic workflow

The Suggest potential risks workflow uses AI to identify and consolidate risks from multiple sources. It replaces manual, workshop-based risk discovery with a faster, consistent, and data-driven process that stays current with new regulations and trends.

## Suggest potential risks workflow overview

**Important:** This agentic workflow is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

The Suggest potential risks workflow uses AI to identify and consolidate risks from multiple sources, streamlining discovery and providing a comprehensive, ready-to-triage risk list. It automates manual risk discovery processes, staying up to date with new regulations and trends, and eliminating duplication and inconsistencies. The Risk Suggestion AI Agent analyzes the entity and suggests relevant risks from various sources, consolidating them into a reviewable list. Risk managers can review the suggested risks, confirm their validity, and promote them to the risk register for further assessment and prioritization.

To use this feature, Now Assist for IRM and any Workspace must be installed. Users with sn\_grc\_sharegenai.risk\_suggestion\_aiagent\_user role can use the conversational assistant embedded in Now Assist panel to discover risks.

The Suggest potential risks workflow supports the identification, evaluation, and prioritization of risks related to a specific entity. It combines information provided by the user, internal entity data, internal risk statement list, and relevant external sources to identify relevant risks for the entity.

The **Risks** tab on the entity record page displays the following options in a vertical layout:

-   **Directly related risks**: List all risks that are directly associated with the entity.
-   **Suggested risks**: List all risks suggested by the Risk Suggestion AI Agent.
-   **All risks**: List all directly related risks and downstream risks.

![Risk identification in Now Assist panel.](../image/risk-identification-agent.png)

## Suggest potential risks workflow benefits

The benefits are as follows:

-   Accelerates risk discovery by replacing manual, workshop-based identification with an AI-guided process.
-   Keeps pace with evolving regulations and industry trends through continuous updates from internal, industry, and external sources.
-   Improves efficiency by automatically pulling entity context and preparing a ready-to-triage risk list in one place.
-   Simplifies user experience through an intuitive conversational assistant embedded in the Now Assist Panel.

**Note:** This use case is optimized for large-scale model providers that support advanced multi-step reasoning, strong instruction adherence, and reliable structured data handling. For best results, use a supported model provider such as Azure OpenAI \(default\), Google Gemini, or Anthropic Claude on AWS. Now LLM is currently not recommended for this use case. For more information, see [KB2804715](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2804715)

**Related topics**  


[Activate agentic workflows in Now Assist for Integrated Risk Management \(IRM\)](../../grc-common/task/activate-agentic-workflows.md)

[Identify risks for an entity using Now Assist for IRM](../task/identify-risks-for-entity.md)


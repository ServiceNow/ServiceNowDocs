---
title: ServiceNow Otto for Integrated Risk Management \(IRM\)
description: The ServiceNow ServiceNow Otto for Integrated Risk Management \(IRM\) application brings generative AI to Governance, Risk, and Compliance. ServiceNow Otto for Integrated Risk Management \(IRM\) was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-05"
reading_time_minutes: 8
---

# ServiceNow Otto for Integrated Risk Management \(IRM\)

The ServiceNow® ServiceNow Otto for Integrated Risk Management \(IRM\) application brings generative AI to Governance, Risk, and Compliance. ServiceNow Otto for Integrated Risk Management \(IRM\) was enhanced and updated in the Zurich release.

## ServiceNow Otto for Integrated Risk Management \(IRM\) highlights for the Zurich release

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.
-   Use AI-generated recommendations to identify which policies are impacted by a regulatory alert.
-   Use the get regulatory analysis agentic workflow to enrich regulatory alerts with external context, classification, summarization, and recommended impacted items. Start by selecting Get analysis from the Ask Now Assist action menu on the regulatory alert page or Get Regulatory Analysis from the Now Assist panel.
-   Use the generate regulatory action plan agentic workflow to turn regulatory insights into actionable compliance strategies with structured tasks, clear ownership, and timelines. Start by selecting Generate action plan from the Ask Now Assist action menu on the regulatory alert page or Generate Regulatory Action Plan from the Now Assist panel.
-   Use the Risk Suggestion AI Agent to discover potential risks for an entity, giving risk managers better insights for informed decision-making.
-   Use the report a GRC issue AI agent in the Employee Center to report issues through a guided conversational experience.
-   Additional role configuration required for agentic workflows and AI agents included with your applications.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md):

-   Use AI-generated recommendations to identify which controls are impacted by a regulatory alert.

See [ServiceNow Otto for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/now-assist-for-irm.md) for more information.

**Important:** ServiceNow Otto for Integrated Risk Management \(IRM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Recommend policies for a regulatory alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/manage-recos-for-policies.md)**

    If you’re a RCM User \[sn\_grc\_reg\_change.user\] and have the Regulatory change AI user \[sn\_grc\_comp\_genai.reg\_change\_ai\_user\] role, you can generate AI-driven recommendations to help identify and mark relevant policies as impacted during regulatory alert reviews. These recommendations assist in associating policy impacts with alerts. You can accept suggested policy impacts to create action tasks immediately or dismiss recommendations to filter out irrelevant information.

-   **Citation impact analysis and updates with Now Assist for IRM**

    When a citation’s description or supplemental guidance is updated, Control Objective Impact Analyzer skill identifies related control objectives that might be affected. The AI agent, ControlObjective Change Agent, then reviews these control objectives to determine whether the descriptions or guidance need changes and provides suggested updates. Users can review, provide feedback, and approve these updates directly in the Now Assist panel, ensuring that citation changes are reflected in associated control objectives.

-   **Enhancements to control objectives rationalization process**

    The following enhancements have been introduced to the generative AI rationalization process of control objectives:

    -   Rationalization process is now automatically created when selecting the Rationalize button in the control objective page. 
    -   The recommendation workflow has been simplified into a two-step process: Step 1 identifies duplicates by accepting or dismissing recommendations; Step 2 finalizes by retaining one recommendation or creating a new common control objective.
    -   Approvals for the rationalization process are skipped for owners who are reviewers, and levels where all reviewers are owners are automatically approved. 
    -   Owners and approvers can add comments and justifications directly on recommendation cards and reply to existing comments. 
    -   The user interface has been updated with better navigation, quick summaries, visual improvements, and clear error messages.
-   **[Get regulatory analysis agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/get-rcm-reg-insight.md)**

    If you’re a RCM User \[sn\_grc\_reg\_change.user\] and have the \[sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user\] role, you can analyze and enrich regulatory alerts by using the get regulatory analysis agentic workflow in the Now Assist panel. This agentic workflow uses web search to enhance alert context, summarizes the alert, and recommends potential impacts on citations, policies, and control objectives to support fast and accurate compliance decisions. You can get started by selecting Get analysis from the Ask Now Assist action menu on the regulatory alert page or by selecting Get Regulatory Analysis from the Now Assist panel.

-   **[Generate regulatory action plans agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/generate_regulatory_action_plans.md)**

    If you’re a RCM User \[sn\_grc\_reg\_change.user\] and have the sn\_grc\_comp\_genai.reg\_change\_ai\_agent\_user role, you can generate a regulatory action plans by using the generate regulatory action plans agentic workflow in the Now Assist panel. This agentic workflow analyzes impacted areas and similar historical alerts to create change tasks and action tasks that help implement regulatory change. You can get started by selecting Generate action plan from the Ask Now Assist action menu on the regulatory alert page or by selecting Generate Regulatory Action Plan from the Now Assist panel.

-   **[Identify risks for an entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/suggest-potential-risks-workflow.md)**

    If you’re a Workspace user with the sn\_grc\_sharegenai.risk\_suggestion\_aiagent\_user role, you can use the Risk Suggestion AI Agent to identify risks related to an entity. The AI agent analyzes the entity and suggests relevant risks from various sources, consolidating them into a reviewable list to verify for accuracy. Risk managers can then confirm and promote these risks to the risk register for further assessment. This feature automates risk discovery, helping identify potential risks and prepare for compliance requirements.

-   **[Report a GRC issue AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/issue-submission-ai-agent.md)**

    The report a GRC issue AI agent is now available in Employee Center, enabling employee users to report issues through a guided conversational experience. As users respond to prompts, the agent structures the issue and recommends relevant controls, entities, and policies based on the input provided. The AI agent helps ensure that the issue is well-defined and enriched with contextual information before it's submitted.


-   **[Recommend controls for a regulatory alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/manage-recos-for-controls.md)**

    If you’re a RCM User \[sn\_grc\_reg\_change.user\] and have the Regulatory change AI user \[sn\_grc\_comp\_genai.reg\_change\_ai\_user\] role, you can generate AI-driven recommendations to help identify and mark relevant controls as impacted during regulatory alert reviews. These recommendations assist in associating control impacts with alerts, reducing manual effort and improving consistency. You can accept suggested control impacts to create action tasks immediately or dismiss recommendations to filter out irrelevant information.


## UI changes

-   **Now Assist skills for Risk &amp; Sustainability**

    The skill family name **Regulatory change management** has been updated to **Regulatory change** to improve naming clarity and consistency within Now Assist skills for Risk &amp; Sustainability under the Technology workflow module in the AI Admin Hub Center.


-   **Now assist skills group renamed**

    The skill group previously named IRM is now renamed Risk &amp; Sustainability under the Technology workflow module in the AI Admin Hub Center.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with your applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


## Activation information

Install ServiceNow Otto for Integrated Risk Management \(IRM\) by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

All ServiceNow Otto for IRM skills and agentic workflows are activated by default after installing ServiceNow Otto for Integrated Risk Management \(IRM\).

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    Use the AI Admin Hub console for quick and effortless access to the important information that you must set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use this conversational interface in ServiceNow® Service Operations Workspace to summarize a chat, an incident, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the ServiceNow® Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/grc-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)


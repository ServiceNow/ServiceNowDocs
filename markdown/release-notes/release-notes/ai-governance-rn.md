---
title: AI Control Tower release notes
description: The ServiceNowAI Control Tower application provides a centralized workspace for AI stewards to manage and monitor AI within the enterprise. The AI Inventory, based on a unified AI asset data model on the ServiceNow AI Platform along with associated governance business processes are available in this workspace.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
---

# AI Control Tower release notes

The ServiceNow®AI Control Tower application provides a centralized workspace for AI stewards to manage and monitor AI within the enterprise. The AI Inventory, based on a unified AI asset data model on the ServiceNow AI Platform® along with associated governance business processes are available in this workspace.

## Plugin information

The AI Control Tower application is available as a Store app. For plugin details, see the Activation information section.

**Important:** AI Control Tower is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## AI Control Tower highlights for the Yokohama release

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   AI connections are introduced in AI Control Tower using Service Graph Connectors. AI connections are combination of hyperscalars, AI apps, and agentic AI frameworks. The AI Service Graph Connectors available from March 2026:
    -   [AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aws_0.md)
    -   [Microsoft](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/microsoft.md)- Azure Foundry and Copilot
    -   [n8n](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/n8n.md)
    -   [GCP Vertex AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/gcp-vertex-ai.md)
    -   [LangGraph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/langgraph.md)
    -   [Salesforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/salesforce.md)

[Yokohama Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-6.md)

-   Monitor the performance of guardrails enabled through Now Assist Guardian using the Health tab.
-   Measure and improve the quality of interactions with virtual agents using the Evaluation tab.

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   AI Control Tower helps customers manage and oversee performance, risk profile &amp; workforce transformation while also helping to seamlessly embed AI into enterprise strategy.

-   -   Create an AI steward role.
-   Use the AI Asset inventory to catalog AI-related artifacts.
-   Use the AI skills Approvals to review and approval flows.
-   Create a AI Control Tower Workspace.

## Important information for Upgrading AI Control Tower to Yokohama

General availability release, no upgrade.

## AI Control Tower Features

[Yokohama Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-6.md)

-   **[Health tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aict-health-tab.md)**

    Monitor and evaluate the effectiveness of offensive content and prompt injection guardrails active on your AI assets.

-   **[Evaluation tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/ai-evaluation.md)**

    Measure and improve the quality of interactions with virtual agents using the Evaluation tab.


-   **[Explore AI model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/ai-model-providers.md)**

    Enable choice for third party model providers powering ServiceNow® skills and agents.


-   **[AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/ai-control-tower-landing.md)**
    -   A single pane view of the AI inventory, its state, and its risk and compliance posture.
    -   Lifecycle to manage AI asset onboarding and deployment.
    -   Helps user oversee and manage AI Asset inventory's risk profile with regard to enterprise policies and global regulations, as defined by the user, with a focus on privacy, data governance, and ethical AI.
    -   AI Case management to oversee AI asset-related inquiries and cases, enabling faster response and improved tracking.
    -   Multi-instance management to synchronize AI asset inventory from sub-prod to prod instances to initiate governance early in the build process.
    -   Control settings to block only ''other'' skills in Now Assist AI deployment pending approvals.

-   **[AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/ai-control-tower-landing.md)**
    -   AI Steward role- Facilitate and coordinate governance activities between innovation, legal, security, risk and compliance teams.
    -   AI Asset inventory- Unified data model on the ServiceNow AI Platform to catalog AI Model, datasets, prompts, and other related artifacts including Now Assist and AI leveraging Generative AI Controller.
    -   AI skills Approvals- Review and approval flows for Now Assist skills and other related assets like AI Models and AI datasets deployed through Now Assist or generative AI Controller.
    -   AI Control Tower Workspace- Intuitive workspace to surface governance tasks, reports, inventory, and insights.

## UI changes

-   **[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)**

    Enhancements to landing page dashboards for AI steward.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aia-security-implementation.md)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## Activation information

The AI Control Tower application is installed as part of the generative AI Controller.

## Browser requirements

The AI Control Tower application supports all the browsers.

## Accessibility information

The AI Control Tower application supports all the platform accessibility features.

## Localization information

-   **[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)**

    The AI Control Tower application isn’t localized


## Related ServiceNow applications and features

-   **[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)**

    [AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/ai-risk-and-compliance.md)


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)


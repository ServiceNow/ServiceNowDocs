---
title: ServiceNow Otto for Hardware Asset Management \(HAM\) release notes
description: The ServiceNow Otto for Hardware Asset Management \(HAM\) application brings agentic AI to Hardware Asset Management. ServiceNow Otto for HAM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-08-14"
reading_time_minutes: 5
---

# ServiceNow Otto for Hardware Asset Management \(HAM\) release notes

The ServiceNow Otto for Hardware Asset Management \(HAM\) application brings agentic AI to Hardware Asset Management. ServiceNow Otto for HAM was enhanced and updated in the Zurich release.

## ServiceNow Otto for HAM highlights for the Zurich release

[Zurich Patch 12](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-12.md)- ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Hardware Asset Management \(HAM\). Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

[Zurich Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-11.md)- Prepare for Now LLM Service to be deprecated in a future release.

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)- Gain real-time visibility into critical asset data through generative AI-driven asset analysis summaries.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)- Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)- Some Now Assist skills, agents, and agentic workflows are now turned on by default.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)- Automate the hardware asset repair process by using an agentic workflow.

See [ServiceNow Otto for Hardware Asset Management \(HAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/now-assist-ham.md) for more information.

**Important:** ServiceNow Otto for HAM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading ServiceNow Otto for HAM to Zurich

If you have the procurement\_user user role, you can access the help manage hardware asset requests agentic workflow, which includes the following AI agents:

-   Hardware asset management sourcing AI agent
-   Transfer order creation AI agent
-   Purchase order creation AI agent

## New in the Zurich release

-   **[Manage your assets with comprehensive and real-time data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/generate-asset-analysis-now-assist-ham.md)**

    View consolidated asset information through AI-generated analysis summary on the asset record. The AI-generated summary dynamically updates based on the asset state and includes context from any active incidents or tasks. The summary displays the asset life cycle, current assignment and location, audit status, financial metrics, and identifies missing data to support asset management activities.


-   **[Optimize hardware asset repair process with the suite of AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/now-assist-ham-repair-agent-workflow.md)**

    Automate the repair of defective and out-of-warranty hardware assets by using AI agents in the help repair hardware assets agentic workflow. These AI agents validate the repair tasks, provide detailed troubleshooting and repair instructions, and complete the tasks on receiving user confirmation.


-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-security-implementation.md)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## Changed in this release

-   **[Now Assist &gt; ServiceNow Otto announcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


-   **[Now LLM Service deprecation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


-   **[Changes to AI usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with your applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


## Activation information

Install ServiceNow Otto for HAM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Additional requirements

The ServiceNow Otto for HAM application requires the Hardware Asset Management Pro plus license.

## Related ServiceNow applications and features

-   **[AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    Use the AI Admin Hub console for quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use this conversational interface in ServiceNow® Service Operations Workspace to summarize a chat, an incident, or resolution notes so that you can get the context of this information more quickly.

-   **[Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the ServiceNow® Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[IT Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/it-asset-management-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)


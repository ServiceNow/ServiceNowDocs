---
title: Now Assist for Operational Sustainability Management Management release notes
description: The ServiceNow Now Assist for Operational Sustainability Management application brings generative AI to Operational Sustainability Management. Now Assist for Operational Sustainability was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-05"
reading_time_minutes: 5
keywords: [AI agents, agentic AI]
---

# Now Assist for Operational Sustainability Management Management release notes

The ServiceNow® Now Assist for Operational Sustainability Management application brings generative AI to Operational Sustainability Management. Now Assist for Operational Sustainability was enhanced and updated in the Zurich release.

## Now Assist for Operational Sustainability highlights for the Zurich release

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.

Accelerate carbon reporting with AI-powered calculations, validation, and insights for Scope 3 emissions.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

Automate metric data collection from utility invoices by extracting key information using the AI-driven document intelligence for utility invoices.

See [Now Assist for Operational Sustainability Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/environmental-social-governance/now-assist-for-esg.md) for more information.

**Important:** Now Assist for Operational Sustainability is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Use agentic AI in Now Assist for Operational Sustainability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/environmental-social-governance/use-agentic-ai-in-now-assist-for-esg-management.md)**

    The carbon calculations agentic workflow acts as a copilot for sustainability teams, streamlining carbon accounting workflows. It intelligently selects metric definitions and emission factors from the library, generates calculated metric definitions, and enables user review and adjustments before final use.


-   **[Extract data from utility invoices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/environmental-social-governance/extract-data-from-utility-invoices.md)**

    Now Assist for Operational Sustainability with document intelligence for utility bills, designed to streamline your ESG metric data collection and reporting. Here are the key highlights:

    -   Extract ESG metric data with Gen AI-Powered Document Intelligence from utility bills, like electricity, gas, and water, with accuracy and efficiency.
    -   Automate data collection by eliminating manual data entry and reducing errors.
    -   Integrate extracted data with ESG metric workflows for a seamless experience.
    -   Scale your operations with an enterprise-scale solution that handles large volumes of data.
    -   Confirm compliance and transparency with built-in audit features that support reporting requirements.

## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


## Activation information

Install Now Assist for Operational Sustainability by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and Features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    Use the Now Assist Admin console for quick and effortless access to the important information that you must set up, configure, and monitor Now Assist applications and features.

-   **[AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-agent-studio.md)**

    Use AI Agent Studio to create, manage, or test AI agents and agentic workflows so that you can create self-executing workflows to help you achieve your business goals.

-   **[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use the Now Assist panel conversational interface in ServiceNow® Software Asset Workspace to interact with and get assistance from generative AI.

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the ServiceNow® Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Operational Sustainability Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/esg-management-rn.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)


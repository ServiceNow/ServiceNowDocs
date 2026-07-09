---
title: Now Assist for Enterprise Architecture \(EA\) release notes
description: The ServiceNow Now Assist for Enterprise Architecture \(EA\) application introduces generative AI skills into the Enterprise Architecture Workspace. You can summarize Architectural Decision Records \(ADR\) in the Enterprise Architecture Workspace. Now Assist for Enterprise Architecture \(EA\) is a new application in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-03-07"
reading_time_minutes: 3
---

# Now Assist for Enterprise Architecture \(EA\) release notes

The ServiceNow® Now Assist for Enterprise Architecture \(EA\) application introduces generative AI skills into the Enterprise Architecture Workspace. You can summarize Architectural Decision Records \(ADR\) in the Enterprise Architecture Workspace. Now Assist for Enterprise Architecture \(EA\) is a new application in the Yokohama release.

## Now Assist for Enterprise Architecture \(EA\) highlights for the Yokohama release

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 1: Generate and summarize Enterprise Modeling and Visualization diagrams for business applications hierarchy, using the Enterprise architecture diagrams AI agent.

Yokohama Early Availability

-   Generate a summary of Architectural Decision Records \(ADR\) in the Enterprise Architecture Workspace.
-   Request a business application or a digital integration using Now Assist in ServiceNow® Virtual Agent.

See [Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/now-assist-ea.md) for more information.

**Important:** Now Assist for Enterprise Architecture \(EA\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Now Assist for Enterprise Architecture \(EA\) features

-   **Yokohama Patch 1 [Using Enterprise Architecture Diagramming AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/using-na-ea-ai-agents.md)**

    Use the Enterprise architecture diagrams AI agent to create Enterprise Modeling and Visualization diagrams for business applications hierarchy and summarize them.

-   **Yokohama Early Availability [Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/now-assist-ea.md)**
    -   Use the ServiceNow® Now Assist for Enterprise Architecture \(EA\) application to summarize Architectural Decision Records \(ADR\) in the Enterprise Architecture Workspace. Use the Architectural Decision Records \(ADR\) to explain your infrastructure. ADR is a type of artifact that helps you to understand the background of a specific architectural decision.
    -   Register a business application and a digital integration with an interactive generative AI experience using Now Assist in Virtual Agent. For more information, see [Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/now-assist-ea.md).

## UI changes

-   **Yokohama Patch 3 [Agentic workflow name update](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/using-na-ea-ai-agents.md)**

    Renamed the Enterprise Architecture Diagrammer AI agent to Enterprise architecture diagrams AI agent.

-   **[UI name updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/configure-now-assist-ea.md)**
    -   In the All menu, renamed the **Features** option under **Now Assist Admin** to **Skills**.
    -   On the Now Assist Admin page, renamed the **Now Assist Features** tab to **Now Assist Skills**.

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

Now Assist features are available with activation of the Now Assist for Enterprise Architecture \(EA\) plugin. The [Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/now-assist-ea.md) application requires an Enterprise Architecture Pro plus license. For more information, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configuring-now-assist.md)**

    The Now Assist Admin console provides you with quick and effortless access to the important information that you must set up, configure, and monitor in Now Assist applications and features.

-   **[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use the Now Assist panel to interact with and get assistance from generative AI.

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills.md)**

    Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows, including content summarization in docs.


**Parent Topic:**[Enterprise Architecture release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/enterprise-architecture-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)


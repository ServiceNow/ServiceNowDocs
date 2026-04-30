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

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 1: Generate and summarize Enterprise Modeling and Visualization diagrams for business applications hierarchy, using the Enterprise architecture diagrams AI agent.

Yokohama Early Availability

-   Generate a summary of Architectural Decision Records \(ADR\) in the Enterprise Architecture Workspace.
-   Request a business application or a digital integration using Now Assist in ServiceNow® Virtual Agent.

See [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US) for more information.

**Important:** Now Assist for Enterprise Architecture \(EA\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Now Assist for Enterprise Architecture \(EA\) features

-   **Yokohama Patch 1 [Using Enterprise Architecture Diagramming AI agent](https://www.servicenow.com/docs/access?context=using-na-ea-ai-agents&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    Use the Enterprise architecture diagrams AI agent to create Enterprise Modeling and Visualization diagrams for business applications hierarchy and summarize them.

-   **Yokohama Early Availability [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
    -   Use the ServiceNow® Now Assist for Enterprise Architecture \(EA\) application to summarize Architectural Decision Records \(ADR\) in the Enterprise Architecture Workspace. Use the Architectural Decision Records \(ADR\) to explain your infrastructure. ADR is a type of artifact that helps you to understand the background of a specific architectural decision.
    -   Register a business application and a digital integration with an interactive generative AI experience using Now Assist in Virtual Agent. For more information, see [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US).

## UI changes

-   **Yokohama Patch 3 [Agentic workflow name update](https://www.servicenow.com/docs/access?context=using-na-ea-ai-agents&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    Renamed the Enterprise Architecture Diagrammer AI agent to Enterprise architecture diagrams AI agent.

-   **[UI name updates](https://www.servicenow.com/docs/access?context=configure-now-assist-ea&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**
    -   In the All menu, renamed the **Features** option under **Now Assist Admin** to **Skills**.
    -   On the Now Assist Admin page, renamed the **Now Assist Features** tab to **Now Assist Skills**.

## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## Activation information

Now Assist features are available with activation of the Now Assist for Enterprise Architecture \(EA\) plugin. The [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US) application requires an Enterprise Architecture Pro plus license. For more information, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Help improve productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The Now Assist Admin console provides you with quick and effortless access to the important information that you must set up, configure, and monitor in Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist panel to interact with and get assistance from generative AI.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Now Assist products provide generative AI skills that are tailored to meet the needs of users in different workflows, including content summarization in docs.


**Parent Topic:**[Enterprise Architecture release notes](enterprise-architecture-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)


---
title: Now Assist for IT Operations Management \(ITOM\) release notes
description: The ServiceNow ServiceNow Otto for ITOM application brings generative AI to ITOM. ServiceNow Otto for ITOM was enhanced and updated in the Yokohama release.The ServiceNow ServiceNow Otto for ITOM application brings generative AI to ITOM. ServiceNow Otto for ITOM was enhanced and updated in the Yokohama release.The ServiceNow ServiceNow Otto for ITOM application brings generative AI to ITOM. ServiceNow Otto for ITOM was enhanced and updated in the Yokohama release.The ServiceNow ServiceNow Otto for ITOM application brings generative AI to ITOM. ServiceNow Otto for ITOM was enhanced and updated in the Yokohama release.The ServiceNow ServiceNow Otto for ITOM application brings generative AI to ITOM. ServiceNow Otto for ITOM was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-04-02"
reading_time_minutes: 7
---

# Now Assist for IT Operations Management \(ITOM\) release notes

The ServiceNow® ServiceNow Otto for ITOM application brings generative AI to ITOM. ServiceNow Otto for ITOM was enhanced and updated in the Yokohama release.

## About Now Assist for IT Operations Management \(ITOM\)

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Now Assist skills used in the analyze potential impact agentic workflow are turned on by default.
-   Use the new manage alerts autonomously workflow to efficiently manage alerts and minimize resolution times, including an AI agent for triage, impact analysis, and root cause investigation.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Get deeper impact analysis in the Analyze alert impact agentic workflow with five new AI agents.
-   Review Alert analysis, and relevant information for new mixed alert groups in the Now Assist panel to help investigate alerts more effectively.
-   Use the Triage and analyze alert agentic workflow to perform initial triage and analysis in the context of an incident.
-   Enhance security for Now Assist AI agents with Access Control Lists \(ACLs\).
-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

Yokohama Patch 3

-   Investigate alerts and get the context that you need to respond efficiently using the Analyze alert impact agentic workflow.
-   Automatically perform initial alert triage and analysis tasks such as assigning alerts, analyzing alert history, and summarizing past incidents, with the Triage and analyze alert agentic workflow.


See [ServiceNow Otto for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-itom.md) for more information.

## Activation and other requirements

**Important:** ServiceNow Otto for ITOM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**
    -   Install the AIOps Experience \[sn\_sow\_aiops\] application from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).
    -   Install ServiceNow Otto for ITOM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).
-   **Additional requirements**

    The ServiceNow Otto for ITOM application requires an ITOM Pro Plus or Enterprise Plus license.


**Parent Topic:**[IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/it-operations-management-rn-landing.md)

## January 2026

The ServiceNow® ServiceNow Otto for ITOM application brings generative AI to ITOM. ServiceNow Otto for ITOM was enhanced and updated in the Yokohama release.

### What's new

-   **[Enhance IT operations with AI-driven, autonomous alert management using the manage alerts autonomously workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-autonomous-operator-workflow.md)**

    Automate alert triage, impact analysis, and root cause investigation with an AI-driven workflow that replaces manual operator steps with autonomous decision-making. The workflow processes incoming alerts end-to-end and surfaces consolidated insights through Express List, giving operators immediate visibility into what happened, what's affected, and why.

-   **[Configure the Datadog and Gemini Cloud Assistant observability skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-ai-agent-configuration.md)**

    Set up the new Datadog and Gemini Cloud Assistant observability skills to get insights from those tools in the manage alerts autonomously agentic workflow. With Datadog and Google Gemini, the workflow now supports five observability tools, including Dynatrace, Kentik, and New Relic, helping you investigate and respond to a wider range of alerts.


### What's changed

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aia-security-implementation.md)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.

-   **[AIOps AI agents removed from the analyze alert impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-itom-agentic-aia.md)**

    Four AIOps AI agents have been removed from the analyze alert impact agentic workflow as they're now available in the manage alerts autonomously agentic workflow. AI agents for Dynatrace, Kentik, and New Relic remain in the analyze alert impact agentic workflow to help you learn about and respond to alerts.


## September 2025

The ServiceNow® ServiceNow Otto for ITOM application brings generative AI to ITOM. ServiceNow Otto for ITOM was enhanced and updated in the Yokohama release.

### What's new

-   **[Configure the Dynatrace analysis AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-itom-config-dynatrace.md)**

    Set up the Dynatrace analysis AI agent in the Analyze alert impact agentic workflow to investigate Dynatrace alerts. With Dynatrace, the agentic workflow now supports three observability tools, including Kentik and New Relic, helping you investigate and respond to a wider range of alerts.

-   **[Expand the Analyze alert impact agentic workflow with four new AIOps agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-itom-use-aia.md)**

    Get a fuller view of alert impact with four new AIOps agents in the Analyze alert impact agentic workflow. Along with observability data, the agentic workflow now includes information from within ServiceNow to help surface business impact and related issues. Activate the AIOps agents to include them in the agentic workflow.

-   **[Enhance your decision-making process with the Analyze Potential Impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-itom-analyze-potential-impact-workflow.md)**

    Assess the potential impact of a change using the Analyze Potential Impact agentic workflow. This workflow provides an analysis of the relevant servers and suggested services that might be impacted by your change request, ensuring you have all the insights needed to make informed decision before a change.

-   **[Add access control lists for security in AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aia-security-implementation.md)**

    Enable security settings to run AI agents and agentic workflows using ACLs and user identities. You can configure and manage the ACLs in AI Agent Studio.

-   **[Utilize the Triage and analyze alerts agentic workflow in the context of an incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-alert-triage-agentic-workflow.md)**

    Initiate the Triage and analyze alerts agentic workflow from the Now Assist panel in the context of the incident form to perform all the functions of the workflow. This workflow automatically assigns, acknowledges, and summarizes origin alerts, determines their significance through historical analysis, and analyzes related incidents.


## August 2025

The ServiceNow® ServiceNow Otto for ITOM application brings generative AI to ITOM. ServiceNow Otto for ITOM was enhanced and updated in the Yokohama release.

### What's new

-   **[New third-party AI model provider options available for all Now Assist applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


### What's deprecated or removed

-   Starting with version 2.0.1 of AI Agents for Observability, the sn\_obs\_aia.admin role, previously required to configure AI agents in the Analyze alert impact agentic workflow, has been removed. Users must now have the credential\_admin and connection\_admin roles instead.
-   Starting with version 2.0.1 of AI Agents for Observability, the prompt `How severe is this alert?` no longer appears in the Analyze alert impact agentic workflow.

## May 2025

The ServiceNow® ServiceNow Otto for ITOM application brings generative AI to ITOM. ServiceNow Otto for ITOM was enhanced and updated in the Yokohama release.

### What's new

-   **[Analyze alert impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-itom-agentic-aia.md)**

    Analyze the impact of alerts and identify the possible causes with the Analyze alert impact agentic workflow. The workflow interacts with observability tools, such as Kentik and New Relic, to surface alert details and provide insights.

-   **[Now Assist for IT Operations Management \(ITOM\) Triage and analyze alert agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/itom-alert-triage-agentic-workflow.md)**

    Automatically assign, acknowledge, and summarize the alerts, determine their significance through history analysis, and analyze the related incidents. Initiate multiple parallel processes to triage and analyze the different alerts.



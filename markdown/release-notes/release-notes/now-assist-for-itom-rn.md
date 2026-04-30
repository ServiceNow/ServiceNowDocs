---
title: Now Assist for IT Operations Management \(ITOM\) release notes
description: The ServiceNow Now Assist for ITOM application brings generative AI to ITOM. Now Assist for ITOM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-08-21"
reading_time_minutes: 10
---

# Now Assist for IT Operations Management \(ITOM\) release notes

The ServiceNow® Now Assist for ITOM application brings generative AI to ITOM. Now Assist for ITOM was enhanced and updated in the Zurich release.

## Now Assist for ITOM highlights for the Zurich release

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   AIOps LEAP added support for new third-party model Claude Sonnet 4.6.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Use the Dynatrace Model Context Protocol \(MCP\) server agent for deeper analysis in the analyze alert impact and manage alerts autonomously agentic workflows.
-   Analyze a Service Observability dashboard to find performance insights.
-   Understand service health by analyzing all available Service Observability dashboards for a service.
-   Expand support for 3P AI Model in AIOps LEAP to include additional model options across Small \(OpenAI GPT-4o mini, Claude Haiku 4.5, Gemini 2.0 Flash\) and Large \(OpenAI GPT-4o, Claude Sonnet 4.5, Gemini 2.0 Pro\) tracks.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.
-   Now Assist skills used in the analyze potential impact agentic workflow are turned on by default.
-   Use the new manage alerts autonomously workflow to efficiently manage alerts and minimize resolution times, including an AI agent for triage, impact analysis, and root cause investigation.
-   -   ****

    Create Knowledge Base articles with embedded command snippets

    Guided chat workflow to create and manage Playbook and KBs

    Break large groups into targeted sub-groups using generative AI

    Generate comprehensive resolution steps from multiple web sources

    Regenerate resolutions when new data sources are enabled


[Zurich Patch 4](../quality/zurich-patch-4.md)

-   View an error analysis by Now Assist in Agent Client Collector.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Get deeper impact analysis in the analyze alert impact agentic workflow with five new AI agents.
-   Enhance security for Now Assist AI agents with access control lists \(ACLs\).
-   Find all TLS certificates expiring within a determined time and renew them in a single prompt.
-   Use the triage and analyze alert agentic workflow to perform initial triage and analysis in the context of an incident.
-   Review Alert analysis, and relevant information for new mixed alert groups in the Now Assist panel to help investigate alerts more effectively.

See [Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information.

**Important:** Now Assist for ITOM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Configure the Dynatrace MCP server agent](https://www.servicenow.com/docs/access?context=now-assist-itom-config-dynatrace-mcp&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Set up the new Dynatrace MCP server agent, which replaces the Dynatrace analysis AI agent, for deeper alert analysis. In the analyze alert impact agentic workflow, you can ask more detailed questions about Dynatrace alerts, such as questions about logs, topology, or recent changes. In the manage alerts autonomously agentic workflow, investigations now pull more comprehensive Dynatrace context based on alert type.

-   **[Updates to the manage alerts autonomously agentic workflow](https://www.servicenow.com/docs/access?context=itom-autonomous-operator-workflow&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    The manage alerts autonomously agentic workflow has been updated to provide additional AI insights in the preview panel and alert record. These updates include:

    -   Summaries of the logic behind automated decisions, such as auto closures of insignificant alerts
    -   A written summary of the Service Observability dashboard
    Additionally, automated alert groups are now supported across Now Assist features such as alert assist and AI insights.

-   **[Analyze log analytics alerts to assess impact and triage urgency](https://www.servicenow.com/docs/access?context=itom-autonomous-operator-workflow&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    The manage alert autonomously agentic workflow now includes AI-driven analysis for log analytics alerts. The alert hypothesizer skill evaluates historical patterns to assess if triage is required. It also classifies alerts as proactive or reactive, where proactive indicates emerging risk and reactive indicates an active issue. The analysis can include contextual insights such as potential failure scenarios to support an alert investigation.

-   **[Analyze Service Observability dashboard skill](https://www.servicenow.com/docs/access?context=analyze-a-dashboard-in-service-observability&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    The analyze Service Observability dashboard skill uses generative AI to summarize a single Service Observability dashboard and calls out insights found in charts. This summary helps operators quickly orient to and understand a particular dashboard. Once activated, this skill is available on all Service Observability dashboards and runs automatically from Incident Investigation when Service Observability is installed.

-   **[Analyze service health](https://www.servicenow.com/docs/access?context=analyze-service-health-in-service-observability&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    The analyze service health skill uses generative AI to analyze all available Service Observability dashboards for the selected service in the Service Operations Workspace \(SOW\). It generates a summary of a service’s health and calls out any found insights. Once activated, this skill is available from the header of a service record in the SOW.


-   **[Enhance IT operations with AI-driven, autonomous alert management using the manage alerts autonomously workflow](https://www.servicenow.com/docs/access?context=itom-autonomous-operator-workflow&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Automate alert triage, impact analysis, and root cause investigation with an AI-driven workflow that replaces manual operator steps with autonomous decision-making. The workflow processes incoming alerts end-to-end and surfaces consolidated insights through Express List, giving operators immediate visibility into what happened, what's affected, and why.

-   **[Configure the Datadog and Gemini Cloud Assistant observability skills](https://www.servicenow.com/docs/access?context=itom-ai-agent-configuration&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Set up the new Datadog and Gemini Cloud Assistant observability skills to get insights from those tools in the manage alerts autonomously agentic workflow. With Datadog and Google Gemini, the workflow now supports five observability tools, including Dynatrace, Kentik, and New Relic, helping you investigate and respond to a wider range of alerts.

-   **[AIOps LEAP skill setup](https://www.servicenow.com/docs/access?context=change-leap-large-languauge-model-llm&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Status information for records grouping job run is available when skills are modified with support KB content.

-   **[AIOps LEAP settings page](https://www.servicenow.com/docs/access?context=setup-aiops-leap-properties&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    The new interface for the AIOps LEAP properties includes default configuration to achieve opportunity savings and reporting.

-   **[Action Insights panel](https://www.servicenow.com/docs/access?context=automation-opportunity-sub-groups&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    The Action Insights panel on the automation opportunity details page provides suggestion to create sub-groups when there are large volumes of records. This helps optimize opportunities and knowledge gaps for architects.


-   **[View an error analysis by Now Assist in Agent Client Collector](https://www.servicenow.com/docs/access?context=agent-errors-now-assist&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Starting in version 6.0.0, use Now Assist AI agents to gather information about errors occurring on Agent Client Collector agents. For example, you can verify the underlying cause behind a specific error or error code.


-   **[Configure the Dynatrace analysis AI agent](https://www.servicenow.com/docs/access?context=now-assist-itom-config-dynatrace&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Set up the Dynatrace analysis AI agent in the analyze alert impact agentic workflow to investigate Dynatrace alerts. With Dynatrace, the agentic workflow now supports three observability tools, including Kentik and New Relic, helping you investigate and respond to a wider range of alerts.

-   **[Expand the analyze alert impact agentic workflow with four new AIOps agents](https://www.servicenow.com/docs/access?context=now-assist-itom-use-aia&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Get a fuller view of alert impact with four new AIOps agents in the analyze alert impact agentic workflow. Along with observability data, the agentic workflow now includes information from within ServiceNow to help surface business impact and related issues. Activate the AIOps agents to include them in the agentic workflow.

-   **[Enhance your decision-making process with the analyze potential impact agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itom-analyze-potential-impact-workflow&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Assess the potential impact of a change using the analyze potential impact agentic workflow. This workflow provides an analysis of the relevant servers and suggested services that might be impacted by your change request, ensuring that you have all the insights needed to make informed decisions before making a change.

-   **[Add access control lists for security in AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Enable security settings to run AI agents and agentic workflows using ACLs and user identities. You can configure and manage the ACLs in AI Agent Studio.

-   **[Now Assist certificate renewal AI agent](https://www.servicenow.com/docs/access?context=now-assist-cert-renewal-ai-agent&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Use the Now Assist certificate renewal AI agentic workflow to automatically renew certificates before they expire. You can perform the following with the Now Assist certificate renewal AI agent:

    -   Renew individual certificates
    -   Find all certificates about to expire
    -   Renew all certificates about to expire in a single prompt
-   **[Utilize the triage and analyze alerts agentic workflow in the context of an incident](https://www.servicenow.com/docs/access?context=itom-alert-triage-agentic-workflow&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Initiate the triage and analyze alerts agentic workflow from the Now Assist panel in the context of the incident form to perform all the functions of the workflow. This workflow automatically assigns, acknowledges, and summarizes origin alerts, determines their significance through historical analysis, and analyzes related incidents.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[AIOps AI agents removed from the analyze alert impact agentic workflow](https://www.servicenow.com/docs/access?context=now-assist-itom-agentic-aia&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Four AIOps AI agents have been removed from the analyze alert impact agentic workflow because they're now available in the manage alerts autonomously agentic workflow. AI agents for Dynatrace, Kentik, and New Relic remain in the analyze alert impact agentic workflow to help you learn about and respond to alerts.

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[AIOps LEAP rebranding](https://www.servicenow.com/docs/access?context=exploring-aiops-leap&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    AIOps LEAP is renamed as Learning-Enhanced Automation Platform reflecting expanded scope beyond just Playbook creation.

-   **[Service Operations Workspace \(SOW\) Integration](https://www.servicenow.com/docs/access?context=view-and-use-aiops-leap-playbooks-in-sow&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    Playbooks appear in SOW module.

-   **[Data Range Display](https://www.servicenow.com/docs/access?context=exploring-aiops-leap&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    The AIOps LEAP landing page shows analyzed data date range for automation teams to be aware of time-ranges of analysis.


-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


## Deprecations

In [Zurich Patch 7](../quality/zurich-patch-7.md), the Dynatrace analysis AI agent is being prepared for future deprecation. To continue getting Dynatrace insights in agentic workflows, deactivate the Dynatrace analysis AI agent and set up the Dynatrace MCP server agent. For configuration details, see [Configure the Dynatrace MCP server agent](https://www.servicenow.com/docs/access?context=now-assist-itom-config-dynatrace-mcp&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).

## Activation information

Install AIOps Experience \[sn\_sow\_aiops\] and Now Assist for ITOM from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

The Now Assist for ITOM application requires an ITOM Pro Plus or Enterprise Plus license.

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Help improve organizational efficiency, deliver better self-service, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console to learn how to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in the ServiceNow® Service Operations Workspace to summarize a chat, incident, or resolution notes, and get the context that you need.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Work with ServiceNow® Now Assist products to use generative AI skills in different workflows. Workflows include summarizing cases or incidents, summarizing chats, generating resolution notes, and generating code.


**Parent Topic:**[IT Operations Management release notes](it-operations-management-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)


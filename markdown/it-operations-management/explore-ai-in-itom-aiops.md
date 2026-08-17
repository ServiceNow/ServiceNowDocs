---
title: AI in ITOM AIOps
description: AI features in ITOM AIOps help operators triage alerts, investigate incidents, analyze service health, and improve service reliability using generative AI and agentic workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/explore-ai-in-itom-aiops.html
release: australia
topic_type: concept
last_updated: "2026-07-02"
reading_time_minutes: 8
keywords: [AI, ITOM AIOps, generative AI, agentic AI]
breadcrumb: [ITOM AIOps, IT Operations Management]
---

# AI in ITOM AIOps

AI features in ITOM AIOps help operators triage alerts, investigate incidents, analyze service health, and improve service reliability using generative AI and agentic workflows.

AI features in ITOM AIOps span several products. The following tables summarize all available AI features by type and product.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

## Agentic workflows

ServiceNow Otto for ITOM includes agentic workflows that use AI agents to complete alert management and investigation tasks autonomously or with minimal operator input.

<table id="table_explore-agentic-workflows"><thead><tr><th>

Product

</th><th>

AI feature

</th><th>

Description

</th><th>

Use case

</th><th>

Resources

</th></tr></thead><tbody><tr><td>

Event Management, Express List

</td><td>

Analyze alert impact agentic workflow

</td><td>

Uses observability AI agents to investigate an alert and surface information about its severity, impact, ownership, and potential root causes. Integrates with observability tools such as Dynatrace, Kentik, and New Relic.

</td><td>

An operator selects an alert from an observability-connected source and wants to understand its blast radius, identify responsible teams, and find potential root causes before escalating.

</td><td>

-   [Analyze alert impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/now-assist-itom-agentic-aia.md)
-   [Analyze alert impact in the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/now-assist-itom-use-aia.md)

</td></tr><tr><td>

Event Management, Express List

</td><td>

Manage alerts autonomously agentic workflow

</td><td>

Provides a unified AI-driven process that automates alert triage, impact analysis, and root cause investigation. Generates reports, summarizes key insights and possible next steps, and stores structured findings in the alert record. Also analyzes Health Log Analytics alerts in an alert group and can classify alerts as proactive or reactive.

</td><td>

An operations team wants alerts to be triaged, analyzed, and summarized automatically as they arrive, with AI insights available in Express List without manual intervention.

</td><td>

-   [Manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/itom-autonomous-operator-workflow.md)
-   [Configure the manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/configure-manage-alerts-autonomously-workflow.md)
-   [Review AI-generated alert insights in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/use-ai-insights-express-list.md)

</td></tr><tr><td>

Event Management, Express List

</td><td>

Analyze potential impact agentic workflow

</td><td>

Analyzes how a change request might affect relevant servers and services. The agent verifies prerequisites, retrieves the change request, selects up to 10 affected servers, identifies matches with suggested services, and displays an impact analysis in the ServiceNow Otto panel. The analysis is also saved to the change request work notes. Includes Service Mapping Candidate and Service Mapping Candidates Impact skills.

</td><td>

An operator or change manager wants to assess the risk of a change request before approving it, without manually reviewing all affected CIs.

</td><td>

-   [Analyze potential impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/now-assist-itom-analyze-potential-impact-workflow.md)
-   [Assess a change request with the Analyze potential impact workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/use-now-assist-analyze-impact-agentic-workflow.md)

</td></tr></tbody>
</table>## AI agents

Standalone AI agents in ITOM AIOps run autonomously on a schedule or in response to a trigger, without requiring user input.

|Product|AI feature|Description|Use case|Resources|
|-------|----------|-----------|--------|---------|
|Service Reliability Management|SLO creator agent|Runs every 14 days and processes up to 25 services or CIs that do not already have auto-generated SLOs. Analyzes historical alerts, incidents, and outages to generate one SLO per service or CI with up to 10 service level indicators \(SLIs\). Generated SLOs are active by default. Email notifications are sent to team managers when SLOs are generated and when the error budget falls to 25% or lower. Requires ServiceNow Otto for ITOM and Service Reliability Management.|A team wants to adopt SLOs without manually defining them, using historical incident and alert data to generate a starting point for each service.|[SLO creator agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-level-objective-management/now-assist-itom-slo-generation.md)|

## Generative AI skills

Generative AI skills in ITOM AIOps are discrete, on-demand capabilities that operators invoke to generate analyses, summaries, or descriptions for a specific alert, group, or service.

<table id="table_explore-generative-ai-skills"><thead><tr><th>

Product

</th><th>

AI feature

</th><th>

Description

</th><th>

Use case

</th><th>

Resources

</th></tr></thead><tbody><tr><td>

Event Management, Express List

</td><td>

Alert analysis skill

</td><td>

Generates a human-readable brief of an alert and additional technical information to support investigation. Available in the ServiceNow Otto panel, on the alert Overview tab in Service Operations Workspace, and in the Express List preview panel. Analyses are provided in English regardless of the language used in the alert description.

</td><td>

An operator opens an alert and wants a quick summary of what it means and what to investigate next.

</td><td>

-   [View an alert analysis by ServiceNow Otto in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/alert-summarization-now-assist.md)
-   [View an alert analysis by ServiceNow Otto in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/alert-summary-now-assist-express-list.md)

</td></tr><tr><td>

Express List

</td><td>

Alert group analysis skill

</td><td>

Generates a simplified, human-readable description of an alert group and technical information to support investigation. Available in the Express List preview panel.

</td><td>

An operator selects an alert group and wants to understand its overall significance before deciding how to respond.

</td><td>

[View an alert group analysis by ServiceNow Otto in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/alert-group-analysis-el.md)

</td></tr><tr><td>

Express List

</td><td>

Alert group description generation skill

</td><td>

Generates a comprehensive description of an alert group that encompasses all alerts within the group. The generated description replaces the original alert group description.

</td><td>

An operator wants to replace a system-generated alert group description with a meaningful, AI-generated summary that reflects the full scope of the group.

</td><td>

[Generate an alert group description in Express List using ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/alert-group-descr-generate-el.md)

</td></tr><tr><td>

Event Management, Express List

</td><td>

Past incident analysis skill

</td><td>

Queries historical records to find related past incidents and analyzes their frequency, criticality, work notes, and resolution. Presents a summary of the most relevant incidents in the ServiceNow Otto panel, including resolution strategies and contact details for teams who resolved similar incidents.

</td><td>

An operator is investigating an alert and wants to know whether similar issues have occurred before and how they were resolved.

</td><td>

-   [Accelerate alert resolution with past incident analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/nai-past-incidents.md)
-   [Generate a ServiceNow Otto summary of past related incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/nai-analyze-past-incidents.md)

</td></tr><tr><td>

Express List

</td><td>

AI-generated incident creation skill

</td><td>

Creates an incident with a human-readable, AI-generated description directly from an alert in Express List.

</td><td>

An operator determines that an alert requires an incident and wants the incident description generated automatically rather than written manually.

</td><td>

[Create an incident from an alert with ServiceNow Otto in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/create-incident-now-assist-el.md)

</td></tr><tr><td>

Service Observability

</td><td>

Analyze dashboard skill

</td><td>

Summarizes a single Service Observability dashboard using generative AI, including calling out insights found in the charts. The skill analyzes data within the selected time period and reports any insights it finds. Results remain available for one hour. Requires manual activation.

</td><td>

An operator wants a quick orientation to an unfamiliar dashboard or needs to identify anomalies in chart data without manually reviewing each chart.

</td><td>

-   [Activate the analyze Service Observability dashboard skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/activate-the-analyze-service-observability-dashboard-skill.md)
-   [Analyze a dashboard in Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/analyze-a-dashboard-in-service-observability.md)

</td></tr><tr><td>

Service Observability

</td><td>

Analyze service health skill

</td><td>

Analyzes all available Service Observability dashboards for a selected service. Detects insights, reports on general service health, and helps operators assess service impact, identify root causes, and streamline incident response. When activated, the skill also runs automatically during incident investigation from the **Investigate** tab. Requires manual activation.

</td><td>

An operator is triaging an incident and needs to quickly assess service impact, identify root causes, and determine next steps across all dashboards for the affected service.

</td><td>

-   [Activate the analyze service health skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/activate-the-analyze-service-health-skill.md)
-   [Analyze service health in Service Observability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-observability/analyze-service-health-in-service-observability.md)

</td></tr></tbody>
</table>
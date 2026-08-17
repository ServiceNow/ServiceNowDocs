---
title: AI in Express List
description: ServiceNow Otto for ITOM provides generative AI skills and agentic workflows in Express List that help operators triage alerts, investigate incidents, and respond faster.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/exploring-ai-in-express-list.html
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-07-02"
reading_time_minutes: 5
keywords: [ServiceNow Otto, generative ai, Express List, agentic workflow, alert analysis, alert triage]
breadcrumb: [Express List in SOW for ITOM, Event Management, ITOM AIOps, IT Operations Management]
---

# AI in Express List

ServiceNow Otto for ITOM provides generative AI skills and agentic workflows in Express List that help operators triage alerts, investigate incidents, and respond faster.

Express List includes several generative AI skills and agentic workflows. All features require ServiceNow Otto for IT Operations Management \(ITOM\) to be installed. For a summary of all AI features across ITOM AIOps, see [AI in ITOM AIOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/explore-ai-in-itom-aiops.md).

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

<table id="table_exploring-ai-in-express-list"><thead><tr><th>

AI feature

</th><th>

Description

</th><th>

Use case

</th><th>

Resources

</th></tr></thead><tbody><tr><td>

Alert analysis skill

</td><td>

Uses generative AI to generate a human-readable brief of an alert and additional technical information to support investigation. Analyses are provided in English regardless of the language used in the alert description.

</td><td>

An operator opens an alert in Express List and wants a quick summary of what the alert means and what to investigate next.

</td><td>

[View an alert analysis by ServiceNow Otto in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/alert-summary-now-assist-express-list.md)

</td></tr><tr><td>

Alert group analysis skill

</td><td>

Uses generative AI to generate a simplified, human-readable description of an alert group and technical information to support investigation.

</td><td>

An operator selects an alert group in Express List and wants to understand the group's overall significance before deciding how to respond.

</td><td>

[View an alert group analysis by ServiceNow Otto in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/alert-group-analysis-el.md)

</td></tr><tr><td>

Alert group description generation skill

</td><td>

Uses generative AI to generate a comprehensive description of an alert group that encompasses all alerts within the group. The generated description replaces the original alert group description.

</td><td>

An operator wants to replace a system-generated alert group description with a meaningful, AI-generated summary that reflects the full scope of the group.

</td><td>

[Generate an alert group description in Express List using ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/alert-group-descr-generate-el.md)

</td></tr><tr><td>

Past incident analysis skill

</td><td>

Queries historical records to find related past incidents and analyzes their frequency, criticality, work notes, and resolution. Presents a summary of the most relevant incidents in the ServiceNow Otto panel, including resolution strategies and contact details for teams who resolved similar incidents.

</td><td>

An operator is investigating an alert and wants to know whether similar issues have occurred before and how they were resolved.

</td><td>

-   [Accelerate alert resolution with past incident analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/nai-past-incidents.md)
-   [Generate a ServiceNow Otto summary of past related incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/nai-analyze-past-incidents.md)

</td></tr><tr><td>

AI-generated incident creation skill

</td><td>

Creates an incident with a human-readable, AI-generated description directly from an alert in Express List.

</td><td>

An operator determines that an alert requires an incident and wants the incident description to be generated automatically rather than written manually.

</td><td>

[Create an incident from an alert with ServiceNow Otto in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/create-incident-now-assist-el.md)

</td></tr><tr><td>

Analyze alert impact agentic workflow

</td><td>

Uses observability AI agents to investigate an alert and surface information about its severity, impact, ownership, and potential root causes. Integrates with observability tools such as Dynatrace, Kentik, and New Relic.

</td><td>

An operator selects an alert from an observability-connected source and wants to understand its blast radius, identify responsible teams, and find potential root causes before escalating.

</td><td>

-   [Analyze alert impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/now-assist-itom-agentic-aia.md)
-   [Analyze alert impact in the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/now-assist-itom-use-aia.md)

</td></tr><tr><td>

Analyze potential impact agentic workflow

</td><td>

Analyzes how a change request might affect relevant servers and services. The agent verifies prerequisites, retrieves the change request, selects up to 10 affected servers, identifies matches with suggested services, and displays an impact analysis in the ServiceNow Otto panel. The analysis is also saved to the change request work notes.

</td><td>

An operator or change manager wants to assess the risk of a change request before approving it, without manually reviewing all affected CIs.

</td><td>

-   [Analyze potential impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/now-assist-itom-analyze-potential-impact-workflow.md)
-   [Assess a change request with the Analyze potential impact workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/use-now-assist-analyze-impact-agentic-workflow.md)

</td></tr><tr><td>

Manage alerts autonomously agentic workflow

</td><td>

Provides a unified AI-driven process that automates alert triage, impact analysis, and root cause investigation. Generates reports, summarizes key insights and possible next steps, and stores structured findings in the alert record. Also analyzes Health Log Analytics alerts in an alert group and can classify alerts as proactive or reactive.

</td><td>

An operations team wants alerts to be triaged, analyzed, and summarized automatically as they arrive, with AI insights available in Express List without manual intervention.

</td><td>

-   [Manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/itom-autonomous-operator-workflow.md)
-   [Configure the manage alerts autonomously agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/configure-manage-alerts-autonomously-workflow.md)
-   [Review AI-generated alert insights in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/use-ai-insights-express-list.md)

</td></tr></tbody>
</table>
---
title: IT Operations Management AI agents
description: The following AI agents are available for IT Operations Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/itom-ai-agents-overview.html
release: australia
topic_type: concept
last_updated: "2026-08-04"
reading_time_minutes: 8
breadcrumb: [IT Operations Management, AI agents library, AI assets, Enable AI experiences]
---

# IT Operations Management AI agents

The following AI agents are available for IT Operations Management.

-   **[Alert impact summary AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-alert-impact-summary-ai-agent.md)**  
This AI agent responds to alerts with an impact summary.
-   **[Alert information retrieval AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-alert-information-retrieval-ai-agent.md)**  
This AI agent looks up and returns information on an em\_alert record.
-   **[Analyze potential impact AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-analyze-potential-impact-ai-agent.md)**  
This agent analyzes the potential business and operational impact of a proposed change by identifying affected servers and services. The agent reviews the change request, performs impact analysis, and documents findings in work notes to support informed decision-making and effective mitigation strategies.
-   **[AWS CloudWatch API AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-aws-cloudwatch-api-agent-ai-agent.md)**  
This AI agent investigates AWS CloudWatch alarm firings end to end by querying alarm configuration, metric time series, log groups, ML anomaly detectors, and Logs Insights. It then synthesizes findings into a structured root cause analysis report with metric analysis, log evidence, and correlated service impact.
-   **[AWS CloudWatch MCP server AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-aws-cloudwatch-mcp-server-agent-ai-agent.md)**  
This AI agent automates AWS CloudWatch alert investigations by analyzing alarm details, querying affected resources, and retrieving CloudWatch metrics and logs across multiple strategies. It provides clear summaries with root cause analysis and actionable recommendations for resolution.
-   **[Azure Monitor MCP AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-azure-monitor-mcp-agent-ai-agent.md)**  
This AI agent investigates Azure Monitor alerts by querying Log Analytics workspaces with KQL, retrieving platform metrics, and checking activity logs and resource health through Azure MCP tools. It returns structured findings to the parent agent.
-   **[CSDM business application to infrastructure AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-csdm-business-application-to-infrastructure-ai-specialist-ai-agent.md)**  
This AI specialist finds the best matching discovered service for each business application and creates the standard CSDM "Uses::Used by" relationship in the CI relationships table \[cmdb\_rel\_ci\].
-   **[Datadog APM MCP server AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-datadog-apm-mcp-server-agent-ai-agent.md)**  
This AI agent queries Datadog APM observability data using the full suite of Datadog MCP server tools. It can answer questions about service health, distributed traces, triggered monitors, log analysis, incidents, SLO compliance, deployment events, and service dependencies.
-   **[Dynatrace analysis AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-dynatrace-analysis-ai-agent.md)**  
This AI agent provides the details for a given alert by querying the Dynatrace API.
-   **[Dynatrace MCP server AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-dynatrace-mcp-server-agent-ai-agent.md)**  
This AI agent provides the details for a given alert by querying the Dynatrace API.
-   **[Gemini Cloud Assist A2A investigation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-gemini-cloud-assist-a2a-investigation-agent-ai-agent.md)**  
This AI agent investigates Google Cloud \(googlemonitor\) alerts by driving a Gemini Cloud Assist investigation through Google's A2A investigation endpoint. It starts an investigation, polls task status, and retrieves the structured investigation result with root-cause hypotheses and next steps.
-   **[Kentik analysis AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-kentik-analysis-ai-agent.md)**  
This AI agent fetches the incident insights report for a Kentik alert.
-   **[LogicMonitor API AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-logicmonitor-api-agent-ai-agent.md)**  
This AI agent investigates alerts that originate with LogicMonitor, as well as operator-initiated entity checks. The agent parses the alert context, resolves the entity, samples the alerting datapoint, checks collector health, and synthesizes a plain-language assessment with a resource-category-aware handoff recommendation.
-   **[Network SME AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-network-sme-agent-ai-agent.md)**  
This AI agent investigates network issues using either alert-driven context or direct network identifiers. It identifies the exact bottleneck location and root cause and recommends remediation by delegating data retrieval to the appropriate vendor subject matter expert agents.
-   **[New Relic analysis AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-new-relic-analysis-ai-agent.md)**  
This AI agent fetches the incident insights report for a New Relic incident.
-   **[New Relic MCP server AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-new-relic-mcp-server-agent-ai-agent.md)**  
This AI agent queries and interprets observability data from New Relic using the full suite of New Relic MCP server tools. It answers questions about entity health, service dependencies, log analysis, alert details and history, performance metrics, and change events.
-   **[Prometheus API AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-prometheus-api-agent-ai-agent.md)**  
This AI agent analyzes and investigates alerts sourced from Prometheus and answers general Prometheus observability questions. It queries Prometheus for current and historical metric values, available metrics, and PromQL expressions for common infrastructure metrics.
-   **[Service map creation AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-service-map-creation-ai-specialist-ai-agent.md)**  
This AI specialist discovers service infrastructure from application service candidates using ML analysis, and then it maps and persists the full service topology in CMDB.
-   **[SolarWinds analysis AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-solarwinds-analysis-ai-agent.md)**  
This AI agent fetches the details related to a SolarWinds alert by executing SWQL queries against SolarWinds to resolve the affected entity and retrieve supporting diagnostic information.
-   **[Splunk MCP server AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-splunk-mcp-server-agent-ai-agent.md)**  
This AI agent investigates Splunk Cloud and compatible Splunk Enterprise alerts by querying SPL-based Splunk platform data using SPL queries, saved searches, index exploration, and ownership metadata retrieval. It translates alert questions into structured findings. This agent does not cover Splunk Observability Cloud or SignalFx.
-   **[SRE investigate AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-sre-investigate-ai-agent.md)**  
This AI agent coordinates investigation activities across multiple observability platforms by orchestrating tool-specific agents, such as Dynatrace, New Relic, Kentik, SolarWinds, Splunk, AWS, ThousandEyes, and LogicMonitor. It correlates findings, identifies root causes, and synthesizes comprehensive investigation reports.
-   **[ThousandEyes MCP server AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/itom-obs-thousandeyes-mcp-server-agent-ai-agent.md)**  
This AI agent investigates ThousandEyes tests. It retrieves test configuration, analyzes metrics and anomalies, correlates network events and outages, and performs path visualization to provide actionable root cause analysis. It receives a test ID and optional alert context from the orchestrator.

**Parent Topic:**[ServiceNow AI agents library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-agent-landing-page.md)


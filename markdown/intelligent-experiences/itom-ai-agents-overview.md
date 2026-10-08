---
title: IT Operations Management AI agents
description: The following AI agents are available for IT Operations Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/itom-ai-agents-overview.html
release: australia
topic_type: concept
last_updated: "2026-08-04"
reading_time_minutes: 6
breadcrumb: [IT Operations Management, AI agents library, AI assets, Enable AI experiences]
---

# IT Operations Management AI agents

The following AI agents are available for IT Operations Management.

-   **[Analyze potential impact AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-analyze-potential-impact-ai-agent.md)**  
This agent analyzes the potential business and operational impact of a proposed change by identifying affected servers and services. The agent reviews the change request, performs impact analysis, and documents findings in work notes to support informed decision-making and effective mitigation strategies.
-   **[AWS CloudWatch API AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-aws-cloudwatch-api-agent-ai-agent.md)**  
This AI agent investigates AWS CloudWatch alarm firings end to end by querying alarm configuration, metric time series, log groups, ML anomaly detectors, and Logs Insights. It then synthesizes findings into a structured root cause analysis report with metric analysis, log evidence, and correlated service impact.
-   **[AWS CloudWatch MCP server AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-aws-cloudwatch-mcp-server-agent-ai-agent.md)**  
This AI agent automates AWS CloudWatch alert investigations by analyzing alarm details, querying affected resources, and retrieving CloudWatch metrics and logs across multiple strategies. It provides clear summaries with root cause analysis and actionable recommendations for resolution.
-   **[Azure Monitor MCP AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-azure-monitor-mcp-agent-ai-agent.md)**  
This AI agent investigates Azure Monitor alerts by querying Log Analytics workspaces with KQL, retrieving platform metrics, and checking activity logs and resource health through Azure MCP tools. It returns structured findings to the parent agent.
-   **[CSDM business application to infrastructure AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-csdm-business-application-to-infrastructure-ai-specialist-ai-agent.md)**  
This AI specialist finds the best matching discovered service for each business application and creates the standard CSDM "Uses::Used by" relationship in the CI relationships table \[cmdb\_rel\_ci\].
-   **[Datadog APM MCP server AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-datadog-apm-mcp-server-agent-ai-agent.md)**  
This AI agent queries Datadog APM observability data using the full suite of Datadog MCP server tools. It can answer questions about service health, distributed traces, triggered monitors, log analysis, incidents, SLO compliance, deployment events, and service dependencies.
-   **[Dynatrace MCP server AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-dynatrace-mcp-server-agent-ai-agent.md)**  
This agent investigates Dynatrace alerts by retrieving alert impact summaries and querying the Dynatrace API for problem details, entity enrichment, log analysis, and root cause theories.
-   **[Gemini Cloud Assist A2A investigation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-gemini-cloud-assist-a2a-investigation-agent-ai-agent.md)**  
This AI agent investigates Google Cloud alerts by driving a Gemini Cloud Assist investigation through Google's A2A investigation endpoint. It starts an investigation, polls task status, and retrieves the structured investigation result with root-cause hypotheses and next steps.
-   **[Kentik analysis AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-kentik-analysis-ai-agent.md)**  
This AI agent fetches the incident insights report for a Kentik alert.
-   **[LogicMonitor API AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-logicmonitor-api-agent-ai-agent.md)**  
This AI agent investigates LogicMonitor alerts and monitored entities, assesses entity health, and recommends next steps.
-   **[Network SME AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-network-sme-agent-ai-agent.md)**  
This AI agent investigates network issues and recommends next steps.
-   **[New Relic MCP server AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-new-relic-mcp-server-agent-ai-agent.md)**  
This AI agent queries and interprets observability data from New Relic using the full suite of New Relic MCP server tools.
-   **[Prometheus API AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-prometheus-api-agent-ai-agent.md)**  
This AI agent analyzes and investigates Prometheus alerts and answers general Prometheus questions, surfacing infrastructure metrics through instant and range queries.
-   **[Service map creation AI specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-service-map-creation-ai-specialist-ai-agent.md)**  
This AI specialist discovers service infrastructure from application service candidates using ML analysis, and then it maps and persists the full service topology in CMDB.
-   **[SolarWinds analysis AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-solarwinds-analysis-ai-agent.md)**  
This AI agent fetches the details related to a SolarWinds alert by executing SWQL queries against SolarWinds.
-   **[Splunk MCP server AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-splunk-mcp-server-agent-ai-agent.md)**  
This AI agent investigates Splunk Cloud and compatible Splunk Enterprise alerts by querying Splunk platform data. It doesn't cover Splunk Observability Cloud.
-   **[SRE investigate AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-sre-investigate-ai-agent.md)**  
This AI agent coordinates investigation activities across multiple observability platforms by orchestrating tool-specific agents. It correlates findings, identifies probable root causes, and synthesizes comprehensive investigation reports.
-   **[ThousandEyes MCP server AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-obs-thousandeyes-mcp-server-agent-ai-agent.md)**  
This AI agent investigates ThousandEyes tests by analyzing metrics, anomalies, network events, and outages. It returns probable causes and recommended next steps.

**Parent Topic:**[ServiceNow AI agents library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-agent-landing-page.md)


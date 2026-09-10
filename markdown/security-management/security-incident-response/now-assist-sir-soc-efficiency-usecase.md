---
title: Analyze security operations
description: The Analyze security operations metrics agentic workflow helps security operations center managers analyze the performance of their security teams.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/now-assist-sir-soc-efficiency-usecase.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use agentic workflows, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Analyze security operations

The Analyze security operations metrics agentic workflow helps security operations center managers analyze the performance of their security teams.

## The Analyze security operations metrics agentic workflow overview

Security operations center \(SOC\) managers can analyze metrics for overall case volume, mean time to assign \(MTTA\), and mean time to resolve \(MTTR\) on security incident response \(SIR\) records to give them insight into their security analysts' performance. They can also ask for recommendations for how to improve the metrics.

## Agents used in the Analyze security operations metrics agentic workflow

-   Security incident retrieval AI agent
-   Security metrics analysis AI agent

## Tools mapped to the Analyze security operations metrics agentic workflow

The following tools are mapped to the AI agents that are used in the Analyze security operations metrics agentic workflow.

|Tool type|Execution mode|Name|Description|
|---------|--------------|----|-----------|
|Script|Autonomous|Lookup security incidents|This tool invokes the script with the correct input from the user's query to retrieve the security incidents from the database.|
|Script|Autonomous|Analysis|Provides further analysis for a specified metric type,`analyst`, `group`, `startDate`, `endDate`, to SOC performance.|
|Script|Autonomous|Calculation|Calculates performance metrics for SOC managers such as mean time to resolve \(MTTR\) and mean time to assign \(MTTA\).|
|Script|Autonomous|Recommend|Recommends managerial actions that could be taken based on an analysis of a metric.|

## Triggers for the Analyze security operations metrics agentic workflow

There are no triggers for this use case. If required, you can add a trigger to invoke the use case automatically.

-   **[Analyze security operations metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/assess-metrics-sir-aiagent.md)**  
Chat with an AI agent from the ServiceNow Otto panel to help you gain insight into how efficiently your security analysts are working with security incidents resolution.

**Parent Topic:**[Using agentic AI workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/using-now-assist-ai-agents-sir.md)


---
title: Security Incident Response AI agent collection for the Analyze security operations metrics agentic workflow
description: The Analyze security operations metrics agentic workflow helps security operations center managers analyze the performance of their security teams.
locale: en-US
release: zurich
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use agentic workflows, Now Assist for Security Incident Response, Security Operations]
---

# Security Incident Response AI agent collection for the Analyze security operations metrics agentic workflow

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


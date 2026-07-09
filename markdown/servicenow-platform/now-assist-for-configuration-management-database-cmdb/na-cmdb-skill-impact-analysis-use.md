---
title: Analyze change and incident impact
description: Use the impact analysis skill to identify upstream services and CIs likely to be affected by a proposed change. Invoke the skill from a change record or directly with a CI and description to receive a prioritized impact assessment with severity levels and reasoning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-impact-analysis-use.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-07-01"
reading_time_minutes: 4
keywords: [impact analysis, change impact, CMDB analysis, NowAssist, change management, Now Assist for CMDB]
breadcrumb: [Analyzing the impact of a change or incident, Use agentic workflows, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Analyze change and incident impact

Use the impact analysis skill to identify upstream services and CIs likely to be affected by a proposed change. Invoke the skill from a change record or directly with a CI and description to receive a prioritized impact assessment with severity levels and reasoning.

## Before you begin

-   Activate the analyze impact agentic workflow, as described in [AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-agent-studio.md).
-   You have the `itil` role to read CMDB, incident, and change records
-   A change record \(change\_request or incident\) exists and is active, or you have a CI sys\_id and a description of the proposed change
-   The affected CI has at least one upstream dependency in the CMDB \(topological relationships\)

Role required: `itil`

## About this task

The impact analysis skill helps change and incident managers make informed approval decisions by automatically identifying which upstream services and CIs are at risk from a proposed change. Rather than manually tracing CMDB relationships, the skill uses AI to reason about propagation likelihood based on the change description and dependency topology. This reasoning helps you make an informed approval decision, schedule appropriate maintenance windows, and notify relevant stakeholders before the change is implemented.

You can invoke the skill in any of the following ways:

-   From a change record \(change request or incident\) where the affected CI and change description are automatically extracted.
-   Directly with a CI sys\_id and description for analysis. The impact analysis skill is invoked through the Assess CMDB change impact agentic workflow."
-   Third way.

If the analysis reaches the LLM reasoning step, the invocation consumes one Now Assist credit. Calls that fail before reaching the LLM step \(for example, CI not found, no description available\) don't consume credits.

## Procedure

1.  In the Now Assist panel, provide one of the following items to ask the impact analysis skill about the change impact in natural language:by selecting the Now Assist icon in the workspace or application.

    -   Reference the change record number from a change record. For example, "What is the impact of CHG0001234?" or "Analyze the impact of CHG0001235". The skill reads the affected CI and change description from the record.
    -   Provide a CI sys\_id and a description of the proposed change. For example, "Analyze the impact of restarting server abc12345. We need to apply a kernel patch and restart." Use this option when invoking from a CI record or agentic workflow without a change record in context.
    The impact analysis skill processes your request by traversing the CMDB topology and querying the LLM for impact reasoning. The skill resolves the CI and description, performs a three-phase BFS traversal of CMDB relationships to build the upstream dependency topology, and uses an LLM to assess impact on each upstream service.

2.  Review the impact analysis result.

    The skill returns a list of affected upstream CIs and services with the following details for each:

    -   CI name and class: The affected service or configuration item \(for example, "payment-db-primary, cmdb\_ci\_db\_instance"\).
    -   Impact level: Severity of the impact \(High, Medium, Low, or None\).
    -   Impact type: Category of impact \(Availability, Performance, Data Integrity, Functional, Security, or Operational\).
    -   Confidence: Confidence level in the assessment \(high, medium, or low\).
    -   Reason: Plain-language explanation, including redundancy awareness and propagation logic.
3.  Use the impact analysis to inform your change approval or incident decision.

    Consider the following based on the results:

    -   Prioritize services with high impact and no redundancy—these are single points of failure.
    -   Medium-impact services that could need staging, rollback procedures, or additional testing.
    -   Identify which stakeholders own high- and medium-impact services, and notify them before approval.
    -   Decide whether to proceed as planned, reschedule during a maintenance window, or modify the change request to reduce impact.
4.  Select the relevant CIs in the result to open their detail pages, or continue with your change approval workflow.

    The agent renders the result with direct links to affected CI records in the CMDB.


**Parent Topic:**[Analyzing the impact of a change or incident overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-impact-analysis-using.md)

**Related topics**  


[Analyzing the impact of a change or incident overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-impact-analysis-using.md)

[Analyze impact agentic workflow reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-impact-analysis-ref.md)


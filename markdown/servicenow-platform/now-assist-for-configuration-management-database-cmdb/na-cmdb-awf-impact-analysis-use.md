---
title: Analyze change and incident impact
description: Use the Assess CMDB impact agentic workflow to identify upstream services and CIs likely to be affected by a proposed change. Invoke the workflow in the ServiceNow Otto panel with a change record or a CI and plain language description to receive a prioritized impact assessment with severity levels and reasoning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-use.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 4
keywords: [impact analysis, change impact, CMDB analysis, NowAssist, change management, ServiceNow Otto for CMDB]
breadcrumb: [Analyzing the impact of a change or incident, Using agentic workflows, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Analyze change and incident impact

Use the Assess CMDB impact agentic workflow to identify upstream services and CIs likely to be affected by a proposed change. Invoke the workflow in the ServiceNow Otto panel with a change record or a CI and plain language description to receive a prioritized impact assessment with severity levels and reasoning.

## Before you begin

-   Activate the Assess CMDB impact agentic workflow, as described in [AI Agent Studio overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-agent-studio.md).
-   You have the `itil` role to read CMDB, incident, and change records
-   A change record \(change\_request or incident\) exists and is active, or you have a CI sys\_id and a description of the proposed change
-   The affected CI has at least one upstream dependency in the CMDB \(topological relationships\)

Role required: `itil`

## About this task

The workflow helps change and incident managers make informed approval decisions by automatically identifying which upstream services and CIs are at risk from a proposed change. Rather than manually tracing CMDB relationships, the workflow uses AI to reason about propagation likelihood based on the change description and dependency topology. This reasoning helps you make an informed approval decision, schedule appropriate maintenance windows, and notify relevant stakeholders before the change is implemented.

You can invoke the workflow in one of the following ways:

-   From a change record \(change request or incident\) where the affected CI and change description are automatically extracted.
-   Directly with a CI sys\_id and description for analysis.

If the analysis reaches the LLM reasoning step, the invocation consumes one ServiceNow Otto credit. Calls that fail before reaching the LLM step \(for example, CI not found, no description available\) don't consume credits.

## Procedure

1.  Select the ServiceNow Otto icon and, in the ServiceNow Otto panel, ask the workflow about the impact of a change.

    -   Provide the change record number from a change record. The workflow reads the affected CI and change description from the record.
    -   Provide a CI sys\_id plus a text description of the proposed change. Use this option when there is no change record — the change has not yet been formally raised.
<table><thead><tr><th>

Mode

</th><th>

Inputs

</th><th>

Examples

</th></tr></thead><tbody><tr><td>

Task record

</td><td>

Change request or incident number. For example, `CHG0000015` or `INC0001234`.

</td><td>

“Help with the impact analysis for CHG000015”, "What is the impact of CHG0001234?", "Help me do the impact analysis for INC0001234" or "Analyze the impact of CHG0001235".

</td></tr><tr><td>

CI\_SYSID plus Change context

</td><td>

`ciid` \(sys\_id of the `cmdb_ci`\) + changeContext \(free-text description of the proposed change\)

</td><td>

"what would be the impact if I patched this server?" or "Analyze the impact of restarting server abc12345. We need to apply a kernel patch and restart".

</td></tr></tbody>
</table>    The workflow processes your request by traversing the CMDB topology and querying the LLM for impact reasoning. The workflow resolves the CI and description, performs a three-phase BFS traversal of CMDB relationships to build the upstream dependency topology, and uses an LLM to assess impact on each upstream service.

2.  Review the impact analysis result.

    The workflow returns a list of affected upstream CIs and services with the following details for each:

    -   CI name and class: The affected service or configuration item \(for example, "payment-db-primary, cmdb\_ci\_db\_instance"\).
    -   Impact level: Severity of the impact \(High, Medium, Low, or None\).
    -   Impact type: Category of impact \(Availability, Performance, Data Integrity, Functional, Security, or Operational\).
    -   Confidence: Confidence level in the assessment \(high, medium, or low\).
    -   Reason: Plain-language explanation, including redundancy awareness and propagation logic.
3.  Use the impact analysis to inform your change approval or incident decision.

    -   Prioritize services with high impact and no redundancy—these are single points of failure.
    -   Medium-impact services that could need staging, rollback procedures, or additional testing.
    -   Identify which stakeholders own high- and medium-impact services, and notify them before approval.
    -   Decide whether to proceed as planned, reschedule during a maintenance window, or modify the change request to reduce impact.
4.  Select the relevant CIs in the result to open their detail pages, or continue with your change approval workflow.

    The workflow renders the result with direct links to affected CI records in the CMDB.


**Parent Topic:**[Analyzing the impact of a change or incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-using.md)

**Related topics**  


[Analyzing the impact of a change or incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-using.md)

[Assess CMDB impact agentic workflow reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-ref.md)


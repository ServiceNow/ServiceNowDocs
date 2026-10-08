---
title: Analyze change and incident impact
description: Use the Assess CMDB impact agentic workflow to identify upstream services and CIs likely to be affected by a proposed change. Invoke the workflow in the ServiceNow Otto panel with a change record to receive a prioritized impact assessment with severity levels and reasoning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-use.html
release: zurich
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 4
keywords: [impact analysis, change impact, CMDB analysis, NowAssist, change management, ServiceNow Otto for CMDB]
breadcrumb: [Analyzing the impact of a change or incident, Using agentic workflows, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Analyze change and incident impact

Use the Assess CMDB impact agentic workflow to identify upstream services and CIs likely to be affected by a proposed change. Invoke the workflow in the ServiceNow Otto panel with a change record to receive a prioritized impact assessment with severity levels and reasoning.

## Before you begin

-   Activate the Assess CMDB impact agentic workflow, as described in [AI Agent Studio overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-agent-studio.md).
-   You have the `itil` role to read CMDB, incident, and change records
-   A change record \(change\_request or incident\) exists and is active
-   The change record has a CI set, or has exactly one affected CI
-   The resolved CI has at least one upstream dependency in the CMDB \(topological relationships\)

Role required: `itil`

## About this task

**Note:** The Assess CMDB impact agentic workflow is deactivated by default.

The workflow helps change and incident managers make informed approval decisions by automatically identifying which upstream services and CIs are at risk from a proposed change. Rather than manually tracing CMDB relationships, the workflow uses AI to reason about propagation likelihood based on the change description and dependency topology. This reasoning helps you make an informed approval decision, schedule appropriate maintenance windows, and notify relevant stakeholders before the change is implemented.

Invoke the workflow from a change record \(change request or incident\). The workflow automatically extracts the affected CI and change description from the record.

If the analysis reaches the LLM reasoning step, the invocation consumes one ServiceNow Otto credit. Calls that fail before reaching the LLM step \(for example, CI not found, no description available\) don't consume credits.

## Procedure

1.  Select the ServiceNow Otto icon \[Omitted image "otto-icon-white.svg"\] Alt text: and, in the ServiceNow Otto panel, ask the workflow about the impact of a change, providing the change record number.

    The workflow reads the CI and change description from the record. If the record has no CI set, the workflow uses the record's affected CI instead, provided there's exactly one.

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

    -   Prioritize services with high impact and no redundancy. These are single points of failure.
    -   Medium-impact services that could need staging, rollback procedures, or additional testing.
    -   Identify which stakeholders own high- and medium-impact services, and notify them before approval.
    -   Decide whether to proceed as planned, reschedule during a maintenance window, or modify the change request to reduce impact.
    \[Omitted image "otto-impact-analysis-panel.png"\] Alt text: Otto panel showing the impact analysis result with the Open in expanded view control.

4.  Select **Open in expanded view** to review the topology visualization.

    The visualization opens in an expanded view. The root CI is highlighted in purple, and upstream CIs are colored by impact level: red for high impact, orange for medium impact, and gray for CIs with no impact. Pointing to a highlighted CI shows its class, status, and the impact reasoning for that CI.

    \[Omitted image "na-cmdb-impact-visual.png"\] Alt text: Impact analysis topology visualization, showing the root CI highlighted in purple and upstream CIs colored by impact severity.

5.  Select the relevant CIs in the result to open their detail pages, or continue with your change approval workflow.

    The workflow renders the result with direct links to affected CI records in the CMDB.


**Parent Topic:**[Analyzing the impact of a change or incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-using.md)

**Related topics**  


[Analyzing the impact of a change or incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-using.md)

[CMDB impact analysis agentic workflow details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-ref.md)


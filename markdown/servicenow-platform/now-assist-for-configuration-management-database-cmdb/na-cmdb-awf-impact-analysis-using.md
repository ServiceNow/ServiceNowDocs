---
title: Analyzing the impact of a change or incident
description: The Impact analysis agentic workflow identifies the upstream services and CIs that are likely to be affected by an incident or by a proposed change. The workflow reasons about propagation likelihood based on CMDB dependency topology and the nature of the change. The workflow returns a structured list with impact levels and the reasoning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-using.html
release: brazil
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [impact analysis, change impact, CMDB, topology, NowAssist, ServiceNow Otto for CMDB, AI reasoning]
breadcrumb: [Using agentic workflows, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Analyzing the impact of a change or incident

The Impact analysis agentic workflow identifies the upstream services and CIs that are likely to be affected by an incident or by a proposed change. The workflow reasons about propagation likelihood based on CMDB dependency topology and the nature of the change. The workflow returns a structured list with impact levels and the reasoning.

**Important:**

Generative AI might produce inaccurate or incomplete information. Impact analysis output depends on the quality of the change description and CMDB relationship data. Always validate AI-generated impact assessments against your organization's change governance policies before approving a change.

The Impact analysis agentic workflow solves a key gap in change management. Today's impact assessment process relies on flat lists of topologically related services with no semantic reasoning about which services will actually be disrupted, or how severely. Change managers must trace CMDB relationships manually and apply institutional knowledge to assess blast radius.

**Note:** The Impact analysis agentic workflow is deactivated by default. Activate it from Agentic Solutions before use, as described in [AI Agent Studio overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-agent-studio.md).

## Key benefits

The workflow provides the following benefits:

-   Reduces manual CMDB relationship tracing and guesswork for change approval decisions.
-   Provides semantic reasoning about impact severity and likelihood, not just topological relationships.
-   Surfaces redundancy awareness. For example, recognizing that a 3-node web tier can absorb the loss of one node.
-   Helps Change managers and CAB members make informed approval and scheduling decisions before meetings.
-   Is invoked directly from the ServiceNow Otto panel or as part of agentic workflows.

## Required role

Access to invoke the workflow requires the `itil` role to read CMDB CI and relationship data, and to view change records.

## Workflow steps

The workflow executes three sequential steps:

-   **Step 1: Resolve input**

    Resolves the CI and a context description from a change record \(change request or incident\). The description is extracted from the NowAssist task summary \(Objective and Risk sections for change requests; Issue section for incidents\). If the summary is unavailable, the workflow uses the record's `short_description` or `description` field.

    If the change record has no CI set, the workflow resolves the CI from the record's affected CI list. This fallback requires exactly one affected CI. If the affected CI list is empty or contains more than one CI, the workflow returns an error instead of running the analysis.

-   **Step 2: Fetch topology**

    The workflow performs a three-phase breadth-first search \(BFS\) traversal of the CMDB relationship graph to build a topology subgraph:

-   **Step 3: LLM assessment**

    The workflow sends the topology graph and change context to an LLM for impact analysis. The LLM returns a structured assessment with impact level, impact type, confidence, and reasoning for each affected CI.

    **Important:** LLM reasoning accuracy depends on the richness and clarity of the change description. Short or vague descriptions produce lower-quality impact assessments.


## Invocation mode

Invoke the workflow with a change or incident record. The workflow reads the change's associated CI and extracts the change description from the record. Supported types: change\_request and incident. Other record types or cancelled changes \(change\_request state 4, incident state 8\) are rejected.

See [CMDB impact analysis agentic workflow details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-ref.md) for detailed API specifications and error handling.

## Output format

The workflow returns a structured list of impacted items. Each item includes:

-   CI name and class: Display name and CMDB class \(for example, cmdb\_ci\_linux\_server\)
-   Impact level: High, Medium, Low, or None
-   Impact type: Availability, Performance, Data Integrity, Functional, Security, Operational, or None
-   Confidence: Confidence in the assessment: High, Medium, or Low
-   Reason: Plain-language explanation including redundancy assessment and propagation reasoning

The workflow renders the result as a topology visualization. The root CI is highlighted in purple. Upstream CIs are colored by impact level: red for high impact, orange for medium impact, and gray for CIs with no impact. Pointing to a highlighted CI shows its class, status, and the impact reasoning for that CI.

\[Omitted image "na-cmdb-impact-visual.png"\] Alt text: Impact analysis topology visualization, showing the root CI highlighted in purple and upstream CIs colored by impact severity.

## Constraints and limitations

-   Maximum LLM input tokens: 15,000 tokens. Large topologies may require truncation or summarization
-   Service Mapping not integrated: Service association relationships \(svc\_ci\_assoc\) aren't included.
-   No relationship type exclusion: All relationship types are traversed. Relationship filtering is not supported.

This workflow considers only the semantics of the Impact analysis agentic workflow topology \(actual and probabilistic relationships\).

-   **[Analyze change and incident impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-use.md)**  
Use the Impact analysis agentic workflow to identify upstream services and CIs likely to be affected by a proposed change. Invoke the workflow in the ServiceNow Otto panel with a change record to receive a prioritized impact assessment with severity levels and reasoning.

**Parent Topic:**[Using agentic workflows in ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using.md)

**Related topics**  


[CMDB impact analysis agentic workflow details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-ref.md)


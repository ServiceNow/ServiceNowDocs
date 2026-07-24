---
title: Analyzing the impact of a change or incident overview
description: The analyze impact agentic workflow uses generative AI to identify which upstream services and configuration items \(CIs\) are likely to be affected by an incident or by a proposed change before it is approved. The skill reasons about propagation likelihood based on CMDB dependency topology and the nature of the change. The skill returns a structured list with impact levels and reasoning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-impact-analysis-using.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-06-29"
reading_time_minutes: 4
keywords: [impact analysis, change impact, CMDB, topology, NowAssist, Now Assist for CMDB, AI reasoning]
breadcrumb: [Use agentic workflows, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Analyzing the impact of a change or incident overview

The analyze impact agentic workflow uses generative AI to identify which upstream services and configuration items \(CIs\) are likely to be affected by an incident or by a proposed change before it is approved. The skill reasons about propagation likelihood based on CMDB dependency topology and the nature of the change. The skill returns a structured list with impact levels and reasoning.

**Important:**

Generative AI might produce inaccurate or incomplete information. Impact analysis output depends on the quality of the change description and CMDB relationship data. Always validate AI-generated impact assessments against your organization's change governance policies before approving a change.

## What is it

The analyze impact agentic workflow solves a key gap in change management: today's impact assessment process relies on flat lists of topologically related services with no semantic reasoning about which services will actually be disrupted, or how severely. Change managers must trace CMDB relationships manually and apply institutional knowledge to assess blast radius.

The analyze impact agentic workflow reads the affected CI from a change record \(or accepts a CI plus description directly\), traverses the upstream CMDB dependency graph, and uses an LLM to reason about propagation likelihood given the nature of the change and each CI's role in the topology. The result is a structured list: each upstream service or CI with an impact level \(High, Medium, Low, or None\) and a plain-language reason explaining the assessment.

**Important:** LLM reasoning accuracy depends on the richness and clarity of the change description. Short or vague descriptions produce lower-quality impact assessments.

## Key benefits

The analyze impact agentic workflow provides the following benefits:

-   Reduces manual CMDB relationship tracing and guesswork for change approval decisions.
-   Provides semantic reasoning about impact severity and likelihood, not just topological relationships.
-   Surfaces redundancy awareness. For example, recognizing that a 3-node web tier can absorb the loss of one node.
-   Helps Change managers and CAB members make informed approval and scheduling decisions before meetings.
-   Is invoked directly from the Now Assist panel or as part of agentic workflows.

## How it works

The analyze impact agentic workflow executes three sequential steps:

-   **Step 1: Resolve input**

    Resolves the CI and a context description from a change record \(change request or incident\) or from direct CI and description input. For change records, the description is extracted from the NowAssist task summary \(Objective and Risk sections for change requests; Issue section for incidents\). If the summary is unavailable, the workflow uses the record's `short_description` or `description` field.

-   **Step 2: Fetch topology**

    The workflow performs a three-phase breadth-first search \(BFS\) traversal of the CMDB relationship graph to build a topology subgraph:

-   **Step 3: LLM assessment**

    The workflow sends the topology graph and change context to an LLM for impact analysis. The LLM returns a structured assessment with impact level, impact type, confidence, and reasoning for each affected CI.


## Invocation modes

The analyze impact agentic workflow supports two invocation modes:

-   **By change record**

    Invoke with a change record ID \(sys\_id\). The workflow reads the change's associated CI and extracts the change description from the record. Supported change types: change\_request and incident. Other record types or cancelled changes \(change\_request state 4, incident state 8\) are rejected.

-   **By CI directly**

    Invoke with a CI sys\_id and a caller-supplied change description. The description is used as-is without change record lookup. Useful for agentic workflows, CI record workspace actions, or scenarios where no change record is available.


See [Analyze impact agentic workflow reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-impact-analysis-ref.md) for detailed API specifications and error handling for each mode.

## Output format

The analyze impact agentic workflow returns a structured list of impacted items. Each item includes:

-   CI name and class: Display name and CMDB class \(for example, cmdb\_ci\_linux\_server\)
-   Impact level: High, Medium, Low, or None
-   Impact type: Availability, Performance, Data Integrity, Functional, Security, Operational, or None
-   Confidence: Confidence in the assessment: High, Medium, or Low
-   Reason: Plain-language explanation including redundancy assessment and propagation reasoning

## Constraints and limitations

-   Maximum topology nodes: 250 CIs maximum per traversal. Configurable by the `sn_cmdb_gen_ai.impact_analysis.max_topology_nodes` system property.
-   Maximum LLM input tokens: 15,000 tokens. Large topologies may require truncation or summarization
-   Service Mapping not integrated: Service association relationships \(svc\_ci\_assoc\) aren't included.
-   No relationship type exclusion: All relationship types are traversed. Relationship filtering is not supported.

This workflow considers only the semantics of the analyze impact agentic workflow topology \(actual and probabilistic relationships\).

## Required role

Access to invoke the analyze impact agentic workflow requires the `itil` role to read CMDB CI and relationship data, and to view change records.

-   **[Analyze change and incident impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-impact-analysis-use.md)**  
Use the impact analysis skill to identify upstream services and CIs likely to be affected by a proposed change. Invoke the skill from a change record or directly with a CI and description to receive a prioritized impact assessment with severity levels and reasoning.

**Parent Topic:**[Using agentic workflows in Now Assist for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-using.md)


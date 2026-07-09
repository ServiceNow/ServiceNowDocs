---
title: Analyze impact agentic workflow reference
description: Reference information for the analyze impact agentic workflow, including input modes, output schema, supported record types, constraints, and system properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-impact-analysis-ref.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-06-29"
reading_time_minutes: 3
keywords: [impact analysis, reference, API, schema, CMDB, Now Assist for CMDB]
breadcrumb: [Reference, Now Assist for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Analyze impact agentic workflow reference

Reference information for the analyze impact agentic workflow, including input modes, output schema, supported record types, constraints, and system properties.

## Input modes

<table id="table_input_modes"><thead><tr><th>

Mode

</th><th>

Inputs

</th><th>

When to use

</th></tr></thead><tbody><tr><td>

Change record

</td><td>

-   `change_request` \(Change\)
-   `incident` \(Incident\)

</td><td>

Invoked from a change record, workspace action, or agentic workflow with a change record in context

</td></tr><tr><td>

CI directly

</td><td>

`ciSysId` \(sys\_id of cmdb\_ci\) + `changeDescription` \(free text\)

</td><td>

Invoked from a CI record, agentic workflow, or workspace action without a change record

</td></tr><tr><td>

CI\_SYSID and Change context

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>## Supported record types

For invocation by change record, the agentic workflow processes these record types:

-   `change_request` \(Change\)
-   `incident` \(Incident\)

Any other record class is rejected. Additionally, cancelled or closed records aren't processed:

-   Change requests in state 4 \(Canceled\) are rejected
-   Change requests in state 5 \(New\) skip LLM-based summarization; the agentic workflow uses record fields as fallback
-   Incidents in state 8 \(Closed\) are rejected

## Input resolution

For invocation by change record, the agentic workflow extracts the change description by using an AI summary of the task. The summary includes:

-   For change\_request: Objective and Risk sections from the change summary
-   For incident: Issue section from the incident summary

If the task summary is unavailable or does not match the expected schema \(for example, a New-state change request with no summary content available\), the analyze impact agentic workflow falls back to the record's `short_description` or `description` field.

## Output schema

The analyze impact agentic workflow returns a structured list of impacted items. Each item has the following schema:

|Field|Values|Description|
|-----|------|-----------|
|`sysId`|String|CI sys\_id from CMDB topology \(unique identifier; for example, `a1b2c3d4e5f6g7h8`\)|
|`ciName`|String|CI display name \(for example, "web-node-01" or "payment-gateway-prod"\)|
|`ciClass`|String|CI class name \(for example, "cmdb\_ci\_linux\_server", "cmdb\_ci\_app\_server", "cmdb\_ci\_db\_instance"\)|
|`impactLevel`|high \| medium \| low \| none|Severity of impact on this CI|
|`impactType`|availability \| performance \| data-integrity \| functional \| security \| operational \| none|Category of impact \(for example, availability loss, performance degradation\)|
|`confidence`|high \| medium \| low|Confidence in the assessment|
|`reason`|String|Plain-language explanation including redundancy assessment and propagation reasoning|

## Topology traversal

The analyze impact agentic workflow builds the dependency topology using a three-phase breadth-first search \(BFS\) through the CMDB relationship table \(`cmdb_rel_ci`\):

1.  Resolve inputs.
2.  Fetch topology.
3.  Invoke LLM.

## System properties

|Property|Default|Description|
|--------|-------|-----------|
|`sn_cmdb_gen_ai.impact_analysis.max_topology_nodes`|250|Maximum number of CI nodes to include in the CMDB topology traversal. When the limit is reached, traversal terminates and only the accumulated nodes are sent to the LLM for impact assessment.|

## Limitations

The analyze impact agentic workflow considers only the semantics of CMDB topology. It does not include data on similar past changes, ongoing incidents, upcoming scheduled changes, or business context.

LLM reasoning accuracy depends on the richness and clarity of the change description provided. Short or vague descriptions produce lower-quality impact assessments.

## Error handling

|Situation|Response|
|---------|--------|
|Change record exists but has no associated CI|Error: cannot determine topology — change record has no CI|
|Change record has no description \(and fallback fails\)|Error: change record has no description. Populate the change record's description or risk fields and try again.|
|Provided change\_id does not exist|Error: change record not found|
|Provided CI sys\_id does not exist in CMDB|Error: CI not found|
|CI exists but has no upstream dependencies|Empty impact list \(valid result, not an error\)|

## Role requirements

Access to the analyze impact agentic workflow requires the `itil` role to:

-   Read CMDB CI records and CI relationship data
-   Read change request and incident records
-   Invoke the Impact Analysis agentic workflow from the Now Assist panel

Additionally, users must have access to open the Now Assist panel from their workspace or application. Contact your administrator if you can't see the Now Assist icon.

**Parent Topic:**[Now Assist for CMDB reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-reference.md)

**Related topics**  


[Analyzing the impact of a change or incident overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-impact-analysis-using.md)

[Analyze change and incident impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-skill-impact-analysis-use.md)


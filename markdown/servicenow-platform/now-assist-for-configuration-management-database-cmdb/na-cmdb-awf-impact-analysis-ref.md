---
title: CMDB impact analysis agentic workflow details
description: Reference information for the Impact analysis agentic workflow, including input modes, output schema, supported record types, workflow tools, and constraints.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-ref.html
release: brazil
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [impact analysis, reference, API, schema, CMDB, ServiceNow Otto for CMDB]
breadcrumb: [Reference, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB impact analysis agentic workflow details

Reference information for the Impact analysis agentic workflow, including input modes, output schema, supported record types, workflow tools, and constraints.

**Note:** The Impact analysis agentic workflow is deactivated by default. Activate it from Agentic Solutions before use, as described in [AI Agent Studio overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-agent-studio.md).

## Role requirements

Access to the Impact analysis agentic workflow requires the `itil` role to perform the following actions:

-   Read CMDB CI records and CI relationship data
-   Read change request and incident records
-   Invoke the Impact Analysis agentic workflow from the ServiceNow Otto panel

Additionally, users must have access to open the ServiceNow Otto panel from their workspace or application. Contact your administrator if you can't see the ServiceNow Otto icon.

## Input modes

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
</table>## Supported record types

For invocation by change record, the workflow processes these record types:

-   `change_request` \(Change\)
-   `incident` \(Incident\)

Any other record class is rejected. Additionally, cancelled or closed records aren't processed:

-   Change requests in state 4 \(Canceled\) are rejected
-   Change requests in state 5 \(New\) skip LLM-based summarization; the agentic workflow uses record fields as fallback
-   Incidents in state 8 \(Closed\) are rejected

## Input resolution

For invocation by change record, the workflow extracts the change description by using an AI summary of the task. The summary includes:

-   For change\_request: Objective and Risk sections from the change summary
-   For incident: Issue section from the incident summary

If the task summary is unavailable or does not match the expected schema, the workflow falls back to the record's `short_description` or `description` field. For example, this fallback applies to a New-state change request with no summary content.

If the record has no CI set, the workflow resolves the CI from the record's affected CI list. This fallback requires exactly one affected CI. If the affected CI list is empty or contains more than one CI, the workflow returns an error instead of running the analysis.

## Output schema

The workflow returns a structured list of impacted items. Each item has the following schema:

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

The workflow builds the dependency topology using a three-phase breadth-first search \(BFS\) through the CMDB relationship table \(`cmdb_rel_ci`\):

1.  Resolve inputs.
2.  Fetch topology.
3.  Invoke LLM.

## Workflow tools

The workflow delegates to an agent that uses the following tools:

-   **Input validation**

    Validates the change or incident number and confirms whether a CI or affected CI is available on the record.

-   **Resolve input**

    Fetches the change context that's passed to the LLM for reasoning.

-   **Skill tool formatter**

    Formats the impact analysis result for display in the ServiceNow Otto panel.

-   **GetFullTopology**

    Loads the topology visualization. This tool invokes a skill that processes the topology in chunks, sends each chunk to the LLM for assessment, and persists the results.


## Limitations

The Impact analysis agentic workflow considers only the semantics of CMDB topology. It does not include data on similar past changes, ongoing incidents, upcoming scheduled changes, or business context.

LLM reasoning accuracy depends on the richness and clarity of the change description provided. Short or vague descriptions produce lower-quality impact assessments.

## Error handling

|Situation|Response|
|---------|--------|
|Change record exists but has no associated CI|Error: cannot determine topology — change record has no CI|
|Change record has no description \(and fallback fails\)|Error: change record has no description. Populate the change record's description or risk fields and try again.|
|Provided change\_id does not exist|Error: change record not found|
|Provided CI sys\_id does not exist in CMDB|Error: CI not found|
|CI exists but has no upstream dependencies|Empty impact list \(valid result, not an error\)|
|Change or incident record has no CI set, and its affected CI list has more than one affected CI|Error: only one affected CI is supported|
|Change or incident record has no CI set, and its affected CI list is empty|Error: cannot determine topology because no CI or affected CI is available|

**Parent Topic:**[ServiceNow Otto for CMDB reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-reference.md)

**Related topics**  


[Analyzing the impact of a change or incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-using.md)

[Analyze change and incident impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-awf-impact-analysis-use.md)


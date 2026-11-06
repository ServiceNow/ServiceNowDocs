---
title: Error log summarization skill - Triggers and Inputs
description: Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate an error log summary. A trigger initiates an action, such as when the system generates an error log summary.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/now-assist-for-software-asset-management-sam/error-log-summarization-triggers-inputs.html
release: zurich
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: reference
last_updated: "2026-11-06"
reading_time_minutes: 1
breadcrumb: [References, ServiceNow Otto for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Error log summarization skill - Triggers and Inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate an error log summary. A trigger initiates an action, such as when the system generates an error log summary.

## Triggers for the Error log summarization skill

The following table lists the trigger for the Error log summarization skill.

|Trigger|Description|
|-------|-----------|
|User-triggered|Error log summary is generated when the user manually triggers the skill by selecting **Troubleshoot** on the SaaS integration profile page.|

## Inputs for the Error log summarization skill

The following table lists the inputs for the Error log summarization skill.

|Input|Description|
|-----|-----------|
|Outbound HTTP Logs \[sys\_outbound\_http\_log\]|4xx and 5xx outbound request and response details, scoped by hostname, job sys\_id, and time window.|
|Flow Execution Context \[sys\_flow\_context\]|Most recent errored flow or subflow execution context for the failing job or validate-connection action.|
|Action Type Definition \[sys\_hub\_action\_type\_definition\]|Resolves the internal name and scope of the action into the flow source sys\_id that is used for context lookup.|
|Integration Profile \[samp\_sw\_subscription\_profile\]|Profile metadata and custom properties such as action name, scope, validate timestamps, and troubleshooting parameters that scope the log queries.|
|Step-Level Execution Reports|Per-step inputs, outputs, and error details that are fetched through FlowExecutionSummaryUtil for the errored context.|

**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/references.md)


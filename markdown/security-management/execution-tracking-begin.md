---
title: Execution Tracking - Begin Flow Action
description: The Execution Tracking - Begin flow action starts the auditing process for a Security Operations Integration flow that operates on observables.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Execution Tracking - Begin Flow Action

The Execution Tracking - Begin flow action starts the auditing process for a Security Operations Integration flow that operates on observables.

The Execution Tracking - Begin flow action can be used with any flow to begin recording the progress of the flow in an audit.

## Results

Possible results for this flow action are:

|Result|Description|
|------|-----------|
|Success|An audit record is created.|

## Input variables

Input variables determine the initial behavior of the flow action.

<table id="table_pgm_tfy_jr"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

capabilityId

</td><td>

System identifier of the Integration Capability being executed.

</td></tr><tr><td>

isImpl

</td><td>

Flag that specifies whether auditing is done for an Integration Capability flow or an Integration Capability implementation flow. Possible values are: -   false - denotes auditing on an abstract Integration Capability flow such as Sightings Search. \(default.\)
-   true - denotes auditing on an Integration Capability implementation flow. For example, Splunk or Elasticsearch.

</td></tr><tr><td>

taskId

</td><td>

System identifier for any task associated with the flow.

</td></tr><tr><td>

observableList

</td><td>

One or more observable SysIDs to perform the desired action. Used as a flow input.

</td></tr><tr><td>

flowContextId

</td><td>

System identifier of the associated flow context record. Supplied by the system.

</td></tr><tr><td>

flowName

</td><td>

Name of the flow. Supplied by the system.

</td></tr><tr><td>

parentCapabilityExcutionId

</td><td>

System identifier of the audit record that launched the implementation flow. Only required for Integration Capability implementation flows such as Splunk, Elasticsearch, and VirusTotal.

</td></tr></tbody>
</table>## Output variables

The output variables contain data that can be used in subsequent actions.

|Variable|Description|
|--------|-----------|
|capabilityExecutionId|System identifier of the audit record.|

-   [Get Supported Security Capabilities action](../../security-operations-integrations/reference/get-supported-security-capabilities-activity.md)
-   [Capability Execution Tracking- No Impls action](../../security-operations-integrations/reference/execution-tracking-noimpls-activity.md)

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](common-wf-activities.md)


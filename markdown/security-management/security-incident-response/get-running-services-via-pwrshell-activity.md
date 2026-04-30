---
title: Get Running Services - WMI Enrichment
description: The Security Incident Response - Get Running Services flow gathers running services on a configuration item added to a security incident.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Security Incident Response - Get Running Services Flow, Security Incident Response Orchestration flows and actions, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Get Running Services - WMI Enrichment

The **Security Incident Response - Get Running Services** flow gathers running services on a configuration item added to a security incident.

The **Get Running Services - WMI Enrichment** flow action is launched automatically to retrieve running services information for a Windows host.

## Input variables

Input variables determine the initial behavior of the flow action.

|Variable|Description|
|--------|-----------|
|target \[string\]|The fully qualified domain name \(FQDN\) of the target system.|

## Output variables

The output variables contain data that can be used in subsequent activities.

<table id="table_bnj_jfy_jr"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

response \[string\]

</td><td>

A JSON string representing the current running services on the target system.

 JSON data includes:

 -   **name**

The name of the service

-   **pid**

The process identifier of the running service

-   **service\_type**

\(Optional\) The type of running service.

-   **start\_name**

The system name for the service

-   **path**

The file path of the running service executable

-   **start\_mode**

The start mode of the running service.

-   **display\_name**

The name of the running service as it appears to the user


</td></tr></tbody>
</table>## Restrictions

The MID Server must support **PowerShell**.

SHA-256 hash requires PowerShell V4.

**Parent Topic:**[Security Incident Response - Get Running Services Flow](../../security-incident-response-orchestration/task/get-running-services-workflow.md)


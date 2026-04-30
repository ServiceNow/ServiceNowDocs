---
title: Get Network Statistics via netstat Flow Action
description: The Security Common Orchestration - Get Network Statistics via netstat flow action retrieves the network statistics for an affected resource on a Windows-based system. This flow action can accelerate the investigation and remediation process.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Get Network Statistics via netstat Flow Action

The Security Common Orchestration - Get Network Statistics via netstat flow action retrieves the network statistics for an affected resource on a Windows-based system. This flow action can accelerate the investigation and remediation process.

The Get Network Statistics via netstat flow action can be used with any flow to retrieve network statistics from a Windows-based system. The machine is queried with the **netstat** command including the **-a** and **-o** parameters. To enhance the output data, **get-process** command is also invoked.

## Results

Possible results for this flow action are:

|Result|Description|
|------|-----------|
|Success|Network statistics were retrieved in JSON format.|
|Failure|An error occurred while attempting to retrieve network statistics. More error information is available in the flow action output error.|

|Variable|Description|
|--------|-----------|
|target \[string\]|The fully qualified domain name \(FQDN\) or IP address of the target system.|

## Output variables

The output variables contain data that can be used in subsequent activities.

<table id="table_bnj_jfy_jr"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

response \[string\]

</td><td>

A JSON string representing the current running processes on the target machine.

 JSON data includes:

 -   **pid**

Process identifier

-   **local \_port**

Local port for the network transaction

-   **state**

Status of the TCP connection.

**Note:** This field is null for UDP connections.

-   **local\_address**

Local fully qualified domain name \(FQDN\) or IP address

-   **remote\_address**

Remote fully qualified domain name \(FQDN\) or IP address

-   **protocol**

TCP or UDP

-   **remote\_port**

Remote port of the network transaction

-   **path**

The file path of the process executable

-   **hash**

The hash value of the process executable. The hash is in SHA-256 for PowerShell V4 or higher. Otherwise, the hash is in MD5.


</td></tr></tbody>
</table>## Restrictions

The MID Server must support PowerShell.

SHA-256 hash requires PowerShell V4.

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](../../security-operations-common/concept/common-wf-activities.md)


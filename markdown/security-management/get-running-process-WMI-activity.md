---
title: Get running processes via WMI activity
description: TheGet Running Processes workflow activity retrieves the running processes of a configuration item on a Windows-based system. This activity can accelerate the investigation and remediation process.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration Flow Actions, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Get running processes via WMI activity

The**Get Running Processes** workflow activity retrieves the running processes of a configuration item on a Windows-based system. This activity can accelerate the investigation and remediation process.

The **Get Running Processes via WMI** activity can be used with any workflow to retrieve running processes on a Windows-based system.

## Input variables

Input variables determine the initial behavior of the activity.

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

A JSON string representing the current running processes on the target system.

 JSON data includes:

 -   **pid**

The process identifier

-   **name**

The name of the process


 Also, if available:

 -   **Owner**

The name of the process owner

-   **owner\_sid**

The system identifier of the process owner

-   **owner\_domain**

The domain of the process owner

-   **path**

The file path of the process executable

-   **hash**

The hash value of the process executable. The hash is in SHA-256 for PowerShell V4 or higher. Otherwise, the hash is in MD5.


</td></tr></tbody>
</table>## Restrictions

The MID Server must support **PowerShell**.

SHA-256 hash requires PowerShell V4.

**Parent Topic:**[Common Security Operations integration flows and orchestration Flow Actions](../../security-operations-common/concept/common-wf-activities.md)


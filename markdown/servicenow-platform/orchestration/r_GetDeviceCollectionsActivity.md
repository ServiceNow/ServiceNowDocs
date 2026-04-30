---
title: Get Device Collections activity
description: The Get Device Collections activity returns the list of available device collections on a Microsoft System Center Configuration Manager \(SCCM\) host.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SCCM activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Get Device Collections activity

The Get Device Collections activity returns the list of available device collections on a Microsoft System Center Configuration Manager \(SCCM\) host.

The Get Device Collections activity uses the [Powershell activity template](../../orchestration-activity-designer/task/t_CreateAPowershellActivity.md#) to access the collections on the SCCM server. The activity is configured to use a MID Server with Powershell capabilities and to run a MID Server script called GetDeviceCollections.ps1 that returns the device collections on the server. This script filters the results of the GET, so that only specific attributes are returned for the device collections on the SCCM server. Filtering the results in this manner controls the size of the payload, while providing the most desirable device collection data. The list of available collections is returned as an array in a JSON object.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **System Center Configuration Manager \(SCCM\)**.

**Note:** The Get Device Collections activity does not use pre-processing scripts.

## Input variables

|Variable|Description|
|--------|-----------|
|sccmServer|The fully qualified domain name \(FQDN\) of the SCCM server..|

## Output variables

<table id="table_o5d_wpm_xs"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

deviceCollections

</td><td>

The **deviceCollections** array contains these attributes:-   **id**: Primary key of the SCCM device collection.
-   **name**: Name of the SCCM device collection.
-   **collectionType**: Type of SCCM collection. In this case, the value is **device**.
-   **localMemberCount**: Count of device collection members visible at the local SCCM site.
-   **memberCount**: Count of all device collection members.
-   **deviceCollection**: Object containing the data set of attributes listed here for this device collection. Use the post-processing script to parse additional data from this set to use.

</td></tr><tr><td>

error

</td><td>

Variable that contains the activity output error message.

</td></tr></tbody>
</table>## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully retrieved a list of device collections available on the SCCM host.|
|Failure|Activity failed to retrieve a list of device collections available on the SCCM host.|

**Parent Topic:**[SCCM activity pack](../concept/c_SCCMActivityPack.md)


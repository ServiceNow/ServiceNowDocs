---
title: Get User Collections activity
description: The Get User Collections activity returns the list of available user collections on a Microsoft System Center Configuration Manager \(SCCM\) server.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SCCM activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Get User Collections activity

The Get User Collections activity returns the list of available user collections on a Microsoft System Center Configuration Manager \(SCCM\) server.

The Get User Collections activity uses the [Powershell activity template](../../orchestration-activity-designer/task/t_CreateAPowershellActivity.md#) to access the user collections on the SCCM server. The activity is configured to use a MID Server with Powershell capabilities and to run a MID Server script called GetUserCollections.ps1 that returns the user collections on the host. This script filters the results of the GET, so that only specific attributes are returned for the user collections on the SCCM server. Filtering the results in this manner controls the size of the payload, while providing the most desirable user collection data. The list of available collections is returned as an array in a JSON object.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **System Center Configuration Manager \(SCCM\)**.

**Note:** The Get User Collections activity does not use pre-processing scripts.

## Input variables

|Variable|Description|
|--------|-----------|
|sccmServer|The fully qualified domain name \(FQDN\) of the SCCM server.|

## Output variables

<table id="table_pkz_csm_xs"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

userCollections

</td><td>

The **userCollections** array contains these attributes:-   **id**: Primary key of the SCCM user collection.
-   **name**: Name of the SCCM user collection.
-   **collectionType**: Type of SCCM collection. In this case, the value is **user**.
-   **localMemberCount**: Count of user collection members visible at the local SCCM site.
-   **memberCount**: Count of all user collection members.
-   **userCollection**: Object containing the data set of attributes listed here for this user collection. Use the post-processing script to parse additional data from this set to use.

</td></tr><tr><td>

error

</td><td>

Variable that contains the activity output error message.

</td></tr></tbody>
</table>## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully retrieved the list of available user collections on an SCCM host.|
|Failure|Activity failed to retrieve the list of available user collections on an SCCM host.|

**Parent Topic:**[SCCM activity pack](../concept/c_SCCMActivityPack.md)


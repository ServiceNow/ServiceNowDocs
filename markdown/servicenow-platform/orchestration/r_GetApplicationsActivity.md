---
title: Get Applications activity
description: The Get Applications activity returns a list of all the applications available on a Microsoft System Center Configuration Manager \(SCCM\) server.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [SCCM activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Get Applications activity

The Get Applications activity returns a list of all the applications available on a Microsoft System Center Configuration Manager \(SCCM\) server.

The Get Applications activity uses the [Powershell activity template](../../orchestration-activity-designer/task/t_CreateAPowershellActivity.md#) to access the applications on the SCCM server. The activity is configured to use a MID Server with Powershell capabilities and to run a MID Server script called GetApplications.ps1. This script filters the results of the GET, so that only specific attributes are returned for the applications on the SCCM server. Filtering the results in this manner controls the size of the payload, while providing the most desirable application data. The list of available applications is returned as an array in a JSON object.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **System Center Configuration Manager \(SCCM\)**.

**Note:** The Get Applications activity does not use a pre-processing script.

## Input variables

|Variable|Description|
|--------|-----------|
|sccmServer|The fully qualified domain name \(FQDN\) of the SCCM server.|

## Output variables

The output variables for the Get Applications activity contain an array of objects called **applications** and an error message. Each object in the array contains the attributes in this table.

<table id="table_ytv_2pm_xs"><thead><tr><th>

Variables

</th><th>

Description

</th></tr></thead><tbody><tr><td>

applications

</td><td>

The **applications** array contains these attributes:-   **id**: Primary key of the SCCM application.
-   **ciUniqueId**: Unique ID of the SCCM application.
-   **name**: Name of the application.
-   **manufacturer**: Manufacturer of the application.
-   **version**: Version of the application.
-   **isDeployable**: True/false value indicating if this application is deployable.
-   **isDeployed**: True/false value indicating if this application is already deployed.
-   **numberOfUsersWithApp**: Count of users with this application installed.
-   **numberOfDevicesWithApp**: Count of devices on which this application is installed.
-   **application**: Object containing the data set listed above for this application. Use the script to parse additional data from this set that you might need.

</td></tr><tr><td>

error

</td><td>

Variable that contains the activity output error message.

</td></tr></tbody>
</table>## Conditions

|Variables|Description|
|---------|-----------|
|Success|Activity successfully retrieved the list of applications available on the SCCM host.|
|Failure|Activity failed to retrieve the list of applications available on the SCCM host.|

**Parent Topic:**[SCCM activity pack](../concept/c_SCCMActivityPack.md)


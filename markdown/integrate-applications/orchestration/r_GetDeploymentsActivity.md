---
title: Get Deployments activity
description: The Get Deployments activity returns the list of deployments performed by Orchestration using a Microsoft System Center Configuration Manager \(SCCM\) server.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [SCCM activity pack, Orchestration activity packs, Classic Orchestration, Creating integrations with applications]
---

# Get Deployments activity

The Get Deployments activity returns the list of deployments performed by Orchestration using a Microsoft System Center Configuration Manager \(SCCM\) server.

The Get Deployments activity uses the [Powershell activity template](../../orchestration-activity-designer/task/t_CreateAPowershellActivity.md#) to access the deployments on the SCCM server. The activity is configured to use a MID Server with Powershell capabilities and to run a MID Server script called GetDeployments.ps1 that returns the deployments on the host. This script filters the results of the GET, so that only specific attributes are returned for the deployments on the SCCM server. Filtering the results in this manner controls the size of the payload, while providing the most desirable deployment data. The list of available deployments is returned as an array in a JSON object.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **System Center Configuration Manager \(SCCM\)**.

**Note:** The Get Deployments activity does not use pre-processing scripts.

## Input variables

|Variable|Description|
|--------|-----------|
|sccmServer|The fully qualified domain name \(FQDN\) of the SCCM server.|

## Output variables

<table id="table_g2l_kqm_xs"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

deployments

</td><td>

The **deployments** array contains these attributes:-   **id**: Primary key of the SCCM application.
-   **applicationId**: Primary key of the SCCM application.
-   **softwareName**: Name of the software that will be deployed.
-   **collectionId**: Primary key of the SCCM collection.
-   **collectionName**: Name of the SCCM collection.
-   **desiredConfigType**: Possible values are: **Install** \(1\) and **Uninstall** \(2\).
-   **deploymentIntent**: Intended purpose of the deployment. Possible values are: **Available** \(1\) and **Required** \(2\) .
-   **numberSuccess**: Number of clients that successfully installed the deployment.
-   **numberErrors**: Number of clients with an error when installing the deployment.
-   **deployment**: Object containing the data set of attributes listed here for this deployment. Use the post-processing script to parse additional data from this set that you might need..

</td></tr><tr><td>

error

</td><td>

Variable that contains the activity output error message.

</td></tr></tbody>
</table>## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully retrieved the list of deployments performed by Orchestration using an SCCM host.|
|Failure|Activity failed to retrieve the list of deployments performed by Orchestration using an SCCM host.|

**Parent Topic:**[SCCM activity pack](../concept/c_SCCMActivityPack.md)


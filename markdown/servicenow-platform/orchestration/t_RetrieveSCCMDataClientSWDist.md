---
title: Retrieve SCCM data for client software distribution
description: Retrieve the collections and the list of applications available for deployment from your SCCM servers.A Discovery workflow populates ServiceNow tables with collection, application, and deployment data retrieved from SCCM servers.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring SCCM, Client software distribution from SCCM, Client Software Distribution, Orchestration applications, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Retrieve SCCM data for client software distribution

Retrieve the collections and the list of applications available for deployment from your SCCM servers.

## Before you begin

**Role required**: sn\_client\_sf\_dist.csd\_admin or admin

Before starting this procedure:

-   Set up your Microsoft System Center Configuration Manager \(SCCM\) server, create the applications and collections, and configure the deployments you need. For information, see your SCCM documentation.
-   [Configure a user](t-config-SCCM-deployment-manager.md) with the Application Deployment Manager role on the SCCM server.
-   Set up the MID Server to communicate with the SCCM server.
-   Add Powershell credentials to the ServiceNow Credentials \[discovery\_credentials\] table for the SCCM user who has the Application Deployment Manager role.

## About this task

To populate the Client Software Distribution application with SCCM data:

## Procedure

1.  Navigate to **All** &gt; **Client Software Distribution** &gt; **SCCM** &gt; **SCCM Server Instance**.

2.  Click **New**.

3.  In the SCCM Server Instance form, identify the server by name and provide the fully qualified domain name.

4.  Click **Submit**.

    The new SCCM server appears in the list.

5.  Open the new SCCM record and click **Discover now** under **Related links**.

    The system runs the Discover SCCM workflow that retrieves the application, collection, and deployment data from the SCCM server.

    ![SCCM server instance record](../image/SCCMServerInstance.png "Retrieving SCCM data with Discovery")


**Parent Topic:**[Configuring SCCM](../concept/configuring-sccm.md)

## SCCM server Discovery for client software distribution

A Discovery workflow populates ServiceNow tables with collection, application, and deployment data retrieved from SCCM servers.

Users run the **Discover SCCM** workflow from an [SCCM Server Instance record](t_RetrieveSCCMDataClientSWDist.md#) to populate the following ServiceNow tables:

<table id="table_lxp_vcp_ks"><thead><tr><th>

Table

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

SCCM Application \[sn\_client\_sf\_dist\_sccm\_application\]

</td><td>

-   name
-   publisher
-   version
-   model
-   sccm\_server

</td></tr><tr><td>

SCCM Collection \[sn\_client\_sf\_dist\_sccm\_collection\]

</td><td>

-   name
-   type
-   sccm\_server

</td></tr><tr><td>

SCCM Deployment \[sn\_client\_sf\_dist\_sccm\_deployment\]

</td><td>

-   application
-   collection
-   type

</td></tr></tbody>
</table>**Note:** For details about the custom activities used in this workflow to extract data from an SCCM server, see [Orchestration SCCM activity pack](../../../administer/orchestration-activities/concept/c_SCCMActivityPack.md).


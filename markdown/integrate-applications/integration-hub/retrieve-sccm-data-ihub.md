---
title: Retrieve SCCM data for client software distribution
description: Retrieve the collections and the list of applications available for deployment from your SCCM servers.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring SCCM, Client software distribution from SCCM, Client Software Distribution using Integration Hub, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Retrieve SCCM data for client software distribution

Retrieve the collections and the list of applications available for deployment from your SCCM servers.

## Before you begin

**Role required**: sn\_client\_sf\_dist.csd\_admin or admin

Before starting this procedure:

-   Set up your Microsoft System Center Configuration Manager \(SCCM\) server, create the applications and collections, and configure the deployments you need. For information, see your SCCM documentation.
-   [Configure the Application Administrator role on the SCCM server](https://www.servicenow.com/docs/access?context=t-config-SCCM-deployment-manager&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) with the Application Deployment Manager role on the SCCM server.
-   Set up the MID Server to communicate with the SCCM server.
-   Add Powershell credentials to the ServiceNow Credentials \[discovery\_credentials\] table for the SCCM user who has the Application Deployment Manager role.

## About this task

To populate the Client Software Distribution application with SCCM data:

## Procedure

1.  Navigate to **All** &gt; **Client Software Distribution** &gt; **SCCM** &gt; **SCCM Server Instance**.

2.  Click **New**.

3.  In the SCCM Server Instance form, identify the server by name and select the connection and credential alias.

    **Note:** Leave the **Fully qualified domain name** field empty.

4.  Click **Submit**.

    The new SCCM server appears in the list.

5.  Open the new SCCM record and click **Discover now** under **Related links**.

    The system runs the Discover SCCM flow that retrieves the application, collection, and deployment data from the SCCM server.

    ![Retrieving SCCM data with Discovery](../images/sccm-ihub.png)


-   **[SCCM server Discovery for client software distribution](../reference/sccm-server-disc-ihub.md)**  
Discovery flow populates ServiceNow tables with collection, application, and deployment data retrieved from SCCM servers.

**Parent Topic:**[Configuring SCCM](../concept/configure-sccm-ihub.md)


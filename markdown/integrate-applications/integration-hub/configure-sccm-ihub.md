---
title: Configuring SCCM
description: Follow the SCCM configuration procedures in the order shown.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Client software distribution from SCCM, Client Software Distribution using Integration Hub, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Configuring SCCM

Follow the SCCM configuration procedures in the order shown.

**Note:** Ensure that user must be able to establish remote PowerShell sessions with the MECM server. The spoke scripts use **Microsoft.PowerShell32** configuration for creating sessions. For user permissions, see [User permissions](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_remote_requirements?view=powershell-7.4#user-permissions) in [Microsoft Learn](https://learn.microsoft.com/en-us/).

-   **[Configure the Application Administrator role on the SCCM server](../tasks/csd-conf-sccm.md)**  
To deploy software using ServiceNow® Client Software Distribution \(CSD\), ensure that an SCCM administrative user has the correct permissions to deploy software and that PowerShell is properly configured.
-   **[Update the SCCM cmdlet libraries](../tasks/csd-cmdlet-lib.md)**  
Ensure that the System Center Configuration Manager SCCM Cmdlet Library is up-to-date.
-   **[Configure the MID Server for SCCM activities](../tasks/csd-mid-sccm.md)**  
To use a MID Server with Microsoft System Center Configuration Management \(SCCM\) activities, configure it to communicate with the SCCM server.
-   **[Create Connection and Credential alias for SCCM deployments](../tasks/create-win-credentials-ihub.md)**  
Microsoft System Center Configuration Manager \(SCCM\) requires the appropriate credentials to deploy applications using the Client Software Distribution application.
-   **[Retrieve SCCM data for client software distribution](../tasks/retrieve-sccm-data-ihub.md)**  
Retrieve the collections and the list of applications available for deployment from your SCCM servers.
-   **[Set up a software model for an SCCM application](../tasks/csd-sw-model.md)**  
Using the applications discovered on the SCCM server, set up a software model used by the Software Asset Management application to manage licenses.
-   **[Define an SCCM configuration](../tasks/csd-sccm-collections.md)**  
To create catalog items for SCCM software deployment or to configure your instance to revoke software through SCCM, you must first associate that software with a collection through an SCCM configuration.
-   **[Create a catalog item for an SCCM application](../tasks/create-cat-item-ihub.md)**  
Create a catalog item for an application you want to offer for distribution from the service catalog using the applications discovered on the SCCM server.

**Parent Topic:**[Client software distribution from SCCM](csd-from-sccm-ihub.md)


---
title: CSD 2.0 for Microsoft Endpoint Configuration Manager
description: Use the CSD 2.0 along with the Microsoft Endpoint Configuration Manager spoke to deploy and revoke software deployments from Microsoft Endpoint Configuration Manager and manage distributions on hosts.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# CSD 2.0 for Microsoft Endpoint Configuration Manager

Use the CSD 2.0 along with the Microsoft Endpoint Configuration Manager spoke to deploy and revoke software deployments from Microsoft Endpoint Configuration Manager and manage distributions on hosts.

To use the Microsoft Endpoint Configuration Manager spoke with CSD 2.0, you must activate Microsoft Endpoint Configuration Manager spoke and CSD 2.0.

The Microsoft Endpoint Configuration Manager spoke contains actions that CSD 2.0 uses to deploy software from a service catalog request and manage user and device collections on Microsoft Endpoint Configuration Manager servers. In addition, CSD 2.0 can manage license counts for deployed software, revoke software deployed by Microsoft Endpoint Configuration Manager without user interaction, and manage lease periods.

**Note:** For systems deploying software from Microsoft Endpoint Configuration Manager, the **Lease end** field is only available if the configuration specifies an uninstall collection.

-   **[Verify the Microsoft Endpoint Configuration Manager spoke records](../task/csd2-ver-endpt.md)**  
Verify that the spoke is integrated with CSD 2.0 after setting up and configuring the Microsoft Endpoint Configuration Manager spoke and create server instance record to use Microsoft Endpoint Configuration Manager spoke with CSD 2.0.
-   **[Store details of the provider server](../task/csd2-endpt-disc-apps.md)**  
Create a server instance record to discover applications and store details of the provider server.
-   **[Set up a software model for the Microsoft Endpoint Configuration Manager application](../task/csd2-sw-model.md)**  
Using the applications discovered on the Microsoft Endpoint Configuration Manager server, set up a software model to manage licenses.
-   **[Define the Microsoft Endpoint Configuration Manager configuration](../task/csd2-sccm-collections.md)**  
Associate that software with a collection through a Microsoft Endpoint Configuration Manager configuration to create catalog items for Microsoft Endpoint Configuration Manager software deployment or to configure your instance to revoke software through Microsoft Endpoint Configuration Manager.
-   **[Create a catalog item for the Microsoft Endpoint Configuration Manager application](../task/csd2-create-cat.md)**  
Create a catalog item for an application you want to offer for distribution from the service catalog using the applications discovered on the Microsoft Endpoint Configuration Manager server.
-   **[Deployment process](../reference/csd2-sccm-deploy.md)**  
Order an application from a CSD 2.0 catalog item in the service catalog triggers the Order Client Software flow.

**Parent Topic:**[Client Software Distribution 2.0 application](csd-app-2.md)


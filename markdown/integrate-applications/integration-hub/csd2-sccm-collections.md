---
title: Define the Microsoft Endpoint Configuration Manager configuration
description: Associate that software with a collection through a Microsoft Endpoint Configuration Manager configuration to create catalog items for Microsoft Endpoint Configuration Manager software deployment or to configure your instance to revoke software through Microsoft Endpoint Configuration Manager.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CSD 2.0 for Microsoft Endpoint Configuration Manager, Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Define the Microsoft Endpoint Configuration Manager configuration

Associate that software with a collection through a Microsoft Endpoint Configuration Manager configuration to create catalog items for Microsoft Endpoint Configuration Manager software deployment or to configure your instance to revoke software through Microsoft Endpoint Configuration Manager.

## Before you begin

Before you create a Microsoft Endpoint Configuration Manager configuration record, make sure you have discovered the Microsoft Endpoint Configuration Manager applications, collections, and deployments, and set up the necessary software models.

Role required: sn\_ms\_epcfgmgr\_spk.Microsoft Endpoint Manager Admin or admin

## About this task

The Microsoft Endpoint Configuration Manager configuration process associates software with Microsoft Endpoint Configuration Manager collections. To deploy software from a Microsoft Endpoint Configuration Manager server, the user or device must be a member of a Microsoft Endpoint Configuration Manager collection associated with an install deployment. CSD 2.0 enables you to revoke unentitled software using the Microsoft Endpoint Configuration Manager server when that software can be removed using an uninstall collection. Users requesting revokable software from the Service Catalog also have the ability to define lease start and stop dates and request lease extensions.

## Procedure

1.  Navigate to **Microsoft Endpoint Configuration Manager** &gt; **Configurations**.

2.  Click **New**.

3.  On the form, fill these values.

<table id="table_dk3_n1k_zrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the Microsoft Endpoint Configuration Manager software configuration record.

</td></tr><tr><td>

Application

</td><td>

Name of an application hosted on the Microsoft Endpoint Configuration Manager server.

</td></tr><tr><td>

Install Collection

</td><td>

Name of the collection associated with the install deployment for the selected application on the Microsoft Endpoint Configuration Manager server. Only those collections associated with the application are available for selection.

</td></tr><tr><td>

Uninstall Collection

</td><td>

Name of the collection associated with the uninstall deployment for the selected application on the Microsoft Endpoint Configuration Manager server. Only those collections associated with the application are available for selection. You must specify an uninstall collection to: -   Define a lease end date for deployed software.
-   Enable lease extensions.
-   Revoke software from a user's machine.


</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[CSD 2.0 for Microsoft Endpoint Configuration Manager](../concept/csd2.md)


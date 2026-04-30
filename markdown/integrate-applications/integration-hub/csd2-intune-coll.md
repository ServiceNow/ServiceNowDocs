---
title: Define the Microsoft Intune configuration
description: Associate that software with a group through a Microsoft Intune configuration to create catalog items for Microsoft Intune software deployment or to configure your instance to revoke software through Microsoft Intune.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CSD 2.0 for Microsoft Intune, Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Define the Microsoft Intune configuration

Associate that software with a group through a Microsoft Intune configuration to create catalog items for Microsoft Intune software deployment or to configure your instance to revoke software through Microsoft Intune.

## Before you begin

Before you create a Microsoft Intune configuration record, make sure you have discovered the Microsoft Intune applications, groups, and deployments, and set up the necessary software models.

Role required: sn\_ms\_intune\_spoke.microsoft\_intune\_admin or admin

## About this task

The Microsoft Intune configuration process associates software with Microsoft Intune groups. To deploy software from a Microsoft Endpoint Configuration Manager server, the user or device must be a member of a Microsoft Intune group associated with an install deployment. CSD 2.0 enables you to revoke unentitled software using the Microsoft Intune server when that software can be removed using an uninstall group. Users requesting revokable software from the Service Catalog also have the ability to define lease start and stop dates and request lease extensions.

## Procedure

1.  Navigate to **Microsoft Intune** &gt; **Configurations**.

2.  Click **New**.

3.  On the form, fill these values.

<table id="table_dk3_n1k_zrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the Microsoft Intune software configuration record.

</td></tr><tr><td>

Application

</td><td>

Name of an application hosted on the Microsoft Intune server.

</td></tr><tr><td>

Install Group

</td><td>

Name of the group associated with the install deployment for the selected application on the Microsoft Intune server. Only those groups associated with the application are available for selection.

</td></tr><tr><td>

Uninstall Group

</td><td>

Name of the group associated with the uninstall deployment for the selected application on the Microsoft Intune server. Only those groups associated with the application are available for selection. You must specify an uninstall collection to: -   Define a lease end date for deployed software.
-   Enable lease extensions.
-   Revoke software from a user's machine.


</td></tr><tr><td>

Deployment Type

</td><td>

Entity for which software deployment or revocation is needed.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[CSD 2.0 for Microsoft Intune](../concept/csd2-ms-intune.md)


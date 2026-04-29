---
title: Install Microsoft Word add-in for ServiceNow Contracts
description: You can activate the Microsoft Word add-in for ServiceNow Contracts plugin \(sn\_cm\_word\_addin\) if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Install Microsoft Word add-in for ServiceNow Contracts

You can activate the Microsoft Word add-in for ServiceNow Contracts plugin \(sn\_cm\_word\_addin\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Microsoft Word add-in for ServiceNow Contracts plugin \(sn\_cm\_word\_addin\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Configure the Microsoft Word add-in for ServiceNow Contracts](snlc-config-word-addin.md)**  
As an admin, configure the Microsoft Word add-in for ServiceNow Contracts.

**Parent Topic:**[Configure Contract Management Pro for Legal Service Delivery](../concept/snlc-config-sn-legal-contracts.md)


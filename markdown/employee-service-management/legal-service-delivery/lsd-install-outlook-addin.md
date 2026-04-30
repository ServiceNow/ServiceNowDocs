---
title: Activate Microsoft Outlook Add-In for Legal Service Delivery
description: You can activate the Microsoft Outlook Add-In for Legal Service Delivery plugin \(sn\_lg\_outlook\) for Legal Service Delivery if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: xanadu
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Microsoft Outlook Add-In for Legal Service Delivery, Microsoft Outlook Add-In for Legal Service Delivery, Integration of Legal Service Delivery with third-party applications, Legal Service Delivery, Employee Service Management]
---

# Activate Microsoft Outlook Add-In for Legal Service Delivery

You can activate the Microsoft Outlook Add-In for Legal Service Delivery plugin \(sn\_lg\_outlook\) for Legal Service Delivery if you have the admin role.

## Before you begin

Microsoft Outlook Add-In for Legal Service Delivery requires a separate subscription from the rest of the ServiceNow AI Platform.

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: sn\_lg\_outlook.admin

## About this task

Roles are installed with Microsoft Outlook Add-In for Legal Service Delivery:

For more information, see [Microsoft Outlook Add-In for Legal Service Delivery reference](../concept/lsd-outlook-addin-refrence.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Microsoft Outlook Add-In for Legal Service Delivery plugin \(sn\_lg\_outlook\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configure Microsoft Outlook Add-In for Legal Service Delivery](../concept/lsd-outlook-addin-configure.md)


---
title: Activate Virtual Agent for Workplace Service Delivery
description: Activate Virtual Agent for Workplace Service Delivery to provide user assistance to employees through a chat interface.
locale: en-US
release: yokohama
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Workplace Core, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Activate Virtual Agent for Workplace Service Delivery

Activate Virtual Agent for Workplace Service Delivery to provide user assistance to employees through a chat interface.

## Before you begin

Role required: admin

## About this task

**Note:** You must have a subscription for Virtual Agent before you can activate the Glide Virtual Agent plugin.

-   Activate the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) that provides the Virtual Agent framework.

    You can activate the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) if you have the admin role. This plugin automatically activates other necessary plugins if they are not already active.

-   Install the Workplace Core plugin \(sn\_wsd\_core\).

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Glide Virtual Agent plugin \(com.glide.cs.chatbot\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from ServiceNow store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store.

3.  Select **Install** and in the Activate Plugin dialog box, select **Activate**.

    **Important:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

4.  In the Application installation dialog box, review the application dependencies.

    If your application requires other applications, install them first if they are not already installed.

    Installing your application also automatically installs the dependent applications or plugins if they are not installed already.


**Parent Topic:**[Configure Workplace Core](../concept/configure-wsd.md)

**Related topics**  


[Install Workplace Core](install-workplace-service-delivery.md)

[Providing your workplace data](../concept/providing-your-workplace-data-wsd.md)

[Configuring spreadsheets to import workplace data](../concept/importing-workspace-data-wsd.md#)


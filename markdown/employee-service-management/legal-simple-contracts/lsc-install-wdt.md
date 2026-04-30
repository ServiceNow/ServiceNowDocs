---
title: Activate Word Document Templates
description: You can activate the Word Document Templates plugin \(sn\_doc\_word\) if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application activates related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: yokohama
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Legal Simple Contracts, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Activate Word Document Templates

You can activate the Word Document Templates plugin \(sn\_doc\_word\) if you have the admin role. The application activates related ServiceNow® Store applications and plugins if they are not already installed.

## About this task

The Word Template \[sn\_doc\_word\_template\] table is installed with Word Document Templates.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Word Document Templates plugin \(sn\_doc\_word\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).



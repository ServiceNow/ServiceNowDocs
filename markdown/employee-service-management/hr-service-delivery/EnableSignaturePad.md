---
title: Activate the Signature Pad plugin
description: To activate signature pad in your application, activate the Signature Pad plugin \[com.snc.signaturepad\]. The Signature Image \[signature\_image\] table installs with this plugin.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Signature pad for HR, HR document templates, E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Activate the Signature Pad plugin

To activate signature pad in your application, activate the Signature Pad plugin \[com.snc.signaturepad\]. The Signature Image \[signature\_image\] table installs with this plugin.

## Before you begin

Role required: admin

## About this task

To purchase a subscription, contact your ServiceNow account manager. After purchasing the subscription, activate the plugin within the production instance.

You can evaluate the feature on a sub-production instance without charge by requesting it from the HI Customer Service System.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).



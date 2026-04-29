---
title: Activate Self-Service Analytics
description: Activate the Self-Service Analytics Core plugin \(com.snc.self\_service\_analytics\_core\) if you have the admin role. This plugin activates related plugins if they are not already active.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Self-Service Analytics, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activate Self-Service Analytics

Activate the Self-Service Analytics Core plugin \(com.snc.self\_service\_analytics\_core\) if you have the admin role. This plugin activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

The Self-Service Analytics Core plugin provides the Self-Service Analytics framework for configuring deflection contexts and activity patterns to collect the case reduction \(deflection\) metrics. The metrics are used in the Self-Service Analytics dashboard.

The Self-Service Analytics Core plugin activates these related plugins if they are not already active.

<table id="table_l3s_4n1_nlb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Subscriptions and Activity Feed Framework\[com.snc.activity\_subscriptions\]

</td><td>

Provides a generic set of artifacts to handle subscriptions for any defined subscribable object. Any entity can be defined as a subscribable object and a set of subscribers can subscribe to the objects. When a event occurs related to the subscribable object, activities can be tracked and subscribers can be notified.

</td></tr></tbody>
</table>**Note:** The Self-Service Analytics Core plugin is also installed when you activate the Platform Analytics Solution for Self-Service Analytics for Customer Service. For more information, see [Activate the Platform Analytics Solution for Self-Service Analytics for Customer Service](https://www.servicenow.com/docs/access?context=ssa-solution-install-init&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Configure Self-Service Analytics](config-ssa.md)


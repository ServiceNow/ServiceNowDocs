---
title: Activate Analytics Pack for Contract Management Pro
description: You can activate the Analytics Pack for Contract Management Pro plugin \(com.sn\_cm\_pa\) if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Platform Analytics Solutions, Manage, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Activate Analytics Pack for Contract Management Pro

You can activate the Analytics Pack for Contract Management Pro plugin \(com.sn\_cm\_pa\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

Activate the full, subscription version of Performance Analytics on the instance where you are activating this Platform Analytics Solution. You can activate Performance Analytics on a non-production instance without purchasing a subscription. For more information, see [Activate your Performance Analytics subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

Review the [Analytics Pack for Contract Management Pro](https://store.servicenow.com/sn_appstore_store.do#!/store/application/88191096438402100a899afecab8f219) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

**Note:**

Before purchasing a subscription, you can evaluate this feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: admin

## About this task

Roles and scheduled jobs items are installed with Analytics Pack for Contract Management Pro.

For more information, see [Components installed with Analytics Pack for Contract Management Pro](../reference/cncore-comp-analytics-pack-cmpro.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Analytics Pack for Contract Management Pro plugin \(com.sn\_cm\_pa\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Platform Analytics Solutions for Contract Management Pro](../../../use/application-content-packs/concept/cncore-analytics-pa.md)


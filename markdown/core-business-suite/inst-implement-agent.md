---
title: Install Implementation agent
description: Install the Implementation Agent to enable an Admin Home dashboard where you can access and set up Core Business Suite.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Core Business Suite]
---

# Install Implementation agent

Install the Implementation Agent to enable an Admin Home dashboard where you can access and set up Core Business Suite.

## Before you begin

For information on using a centralized Admin Home dashboard to set up and manage applications, see [Setup Hub](https://www.servicenow.com/docs/access?context=ia-landing&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Note:** Core Business Suite guided setup is supported only on Australia patch 1 and later. Verify that your instance meets this requirement before installing the Implementation Agent.

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Implementation agent \(sn\_ia\) application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    The available versions are displayed.

3.  Review the available versions displayed.

4.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

5.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

6.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

Set up the Core Business Suite. For more information, see [Install Core Business Suite Foundation](set-up-cbs.md).

**Parent Topic:**[Configure Core Business Suite Foundation](../concept/configure-cbs.md)


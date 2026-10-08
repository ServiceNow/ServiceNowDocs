---
title: Activate the ServiceNow Cowork plugin
description: You can activate the ServiceNow Cowork plugin \(sn\_app\_cowork\) for ServiceNow Cowork if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they aren't already installed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/activate-servicenow-cowork-plugin.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow Cowork, Enable AI experiences]
---

# Activate the ServiceNow Cowork plugin

You can activate the ServiceNow Cowork plugin \(sn\_app\_cowork\) for ServiceNow Cowork if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren't already installed.

## Before you begin

ServiceNow Cowork requires a separate subscription from the rest of the ServiceNow AI Platform.

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the ServiceNow Cowork plugin \(sn\_app\_cowork\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).


**Parent Topic:**[Configuring ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/servicenow-cowork-configuring.md)


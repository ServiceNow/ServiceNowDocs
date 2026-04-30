---
title: Activate data privacy \(Classic\)
description: You can activate the data privacy plugin \(com.glide.data\_privacy\) for Platform Security if you have the admin role. If the application doesn't include demo data or it doesn't install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they aren't already installed.
locale: en-US
release: yokohama
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2025-02-04"
reading_time_minutes: 1
breadcrumb: [Data privacy \(Classic\), Data Privacy, Platform Privacy]
---

# Activate data privacy \(Classic\)

You can activate the data privacy plugin \(com.glide.data\_privacy\) for Platform Security if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren't already installed.

## Before you begin

Data privacy requires a separate subscription from the rest of the ServiceNow AI Platform®.

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:** Before purchasing a subscription, you can evaluate Data Privacy\(Classic\) and Data Discovery with a 30 day trial period. After your trial expires you will no longer be able to discover data or run anonymization jobs in without a license.

Role required: admin

## About this task

The following items are installed with data privacy:

-   Plugins
-   Roles
-   Tables

For more information, see [Installed with data privacy \(Classic\)](../../security/reference/installed-with-data-privacy.md#).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Data Privacy plugin \(com.glide.data\_privacy\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).



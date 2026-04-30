---
title: Activating Data Discovery
description: The application installs Data Discovery and related ServiceNow Store applications and plugins if they aren't already installed.
locale: en-US
release: yokohama
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Discovery, Platform Privacy]
---

# Activating Data Discovery

The application installs Data Discovery and related ServiceNow® Store applications and plugins if they aren't already installed.

## Before you begin

Data discovery requires a separate subscription from the rest of the ServiceNow AI Platform.

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Installing the Data Discovery Store App will auto install the Data Discovery APIs plugin

Role required: admin

## About this task

The following items are installed with data discovery:

-   Roles
-   Tables

For more information on the roles and tables installed, see [Data Discovery roles](../reference/data-discovery-roles.md#) and [Default data patterns](../reference/default-data-patterns.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Data Discovery plugin \(sn\_data\_discovery\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).



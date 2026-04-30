---
title: Activate Sitemap Generator
description: You can activate the Sitemap Generator plugin \(sn\_ux\_seo\_sitemap\) for Service Portal if you have the admin role.
locale: en-US
release: yokohama
product: Sitemap Generator
classification: sitemap-generator
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Sitemap Generator, Improving search engine optimization for portals, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Activate Sitemap Generator

You can activate the Sitemap Generator plugin \(sn\_ux\_seo\_sitemap\) for Service Portal if you have the admin role.

## Before you begin

Role required: admin

## About this task

Scheduled jobs and tables are installed with Sitemap Generator.

For more information, see [Components installed with Sitemap Generator](../reference/installed-with-sitemap-generator.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Sitemap Generator plugin \(sn\_ux\_seo\_sitemap\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Components installed with Sitemap Generator](../reference/installed-with-sitemap-generator.md)**  
Several types of components are installed with activation of the Sitemap Generator plugin, including tables and scheduled jobs.

**Parent Topic:**[Sitemap Generator](../concept/sitemap-generator.md)


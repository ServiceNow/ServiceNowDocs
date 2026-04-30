---
title: Activate the sitemap configuration and definition records for the Knowledge Portal
description: Include knowledge articles in your sitemap by activating the sitemap configuration and definition records.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activate the sitemap configuration and definition records for the Knowledge Portal

Include knowledge articles in your sitemap by activating the sitemap configuration and definition records.

## Before you begin

-   [Activate Sitemap Generator](https://www.servicenow.com/docs/access?context=activate-sitemap-generator&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)
-   Verify that an unauthenticated user can access the knowledge base article by accessing it as a guest user.
-   Verify that the Public option is selected on the Knowledge Article View form.

Role required: admin

## About this task

Beginning with the Zurich release, the Sitemap Generator configuration is available with the base system and is inactive by default.

## Procedure

1.  Navigate to **All** &gt; **Sitemap Generator** &gt; **Sitemap Configuration**.

2.  In the UX Sitemap Configurations \[sys\_ux\_seo\_sitemap\_config\] table, select the sitemap\_config\_KB record.

3.  Enable the generation of sitemaps.

    1.  On the form, select the **Active** check box.

    2.  In the Sitemap Config Definition related list, double-click the **Type** field and select the **true** option from the list.

    3.  Select the Save icon \(![Save icon](../image/save-km.png)\).

4.  Select **Update**.


## Result

All active sitemaps regenerate once in a day and include content from any of their active sitemap definitions.

**Parent Topic:**[Configuring Knowledge Management](../concept/configuring-knowledge-management.md)


---
title: Activate the sitemap configuration and definition records for the Consumer Service Portal
description: Include knowledge articles and catalogs in your sitemap by activating the sitemap configuration and definition records.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure the Customer and Consumer Service Portals, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Activate the sitemap configuration and definition records for the Consumer Service Portal

Include knowledge articles and catalogs in your sitemap by activating the sitemap configuration and definition records.

## Before you begin

-   [Activate Sitemap Generator](https://www.servicenow.com/docs/access?context=activate-sitemap-generator&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)
-   Verify that an unauthenticated user can access the knowledge base article and catalogs by accessing it as a guest user.
-   Verify that the Public option is selected on the Knowledge Article form or Service Catalog page form.

Role required: admin

## About this task

Beginning with the Yokohama release, the Sitemap Generator configuration is available with the base system and is inactive by default.

## Procedure

1.  Navigate to **All** &gt; **Sitemap Generator** &gt; **Sitemap Configuration**.

2.  In the UX Sitemap Configurations \[sys\_ux\_seo\_sitemap\_config\] table, select the sitemap\_config\_CSP record.

3.  Enable the generation of sitemaps.

    1.  On the form, select the **Active** check box.

    2.  In the Sitemap Config Definition related list, double-click the **Type** field and select the **true** option from the list.

    3.  Select the Save icon \(![Save icon](../image/save.png)\).

4.  Select **Update**.


## Result

All active sitemaps regenerate once in a day and include content from any of their active sitemap definitions.


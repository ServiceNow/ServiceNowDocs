---
title: Activate the sitemap configuration and definition records for the Consumer Service Portal
description: Include knowledge articles and catalogs in your sitemap by activating the sitemap configuration and definition records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/customer-service-management/activate-sitemap-confi-csp.html
release: xanadu
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure the Customer and Consumer Service Portals, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Activate the sitemap configuration and definition records for the Consumer Service Portal

Include knowledge articles and catalogs in your sitemap by activating the sitemap configuration and definition records.

## Before you begin

-   [Activate Sitemap Generator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-user-interface/sitemap-generator/activate-sitemap-generator.md)
-   Verify that an unauthenticated user can access the knowledge base article and catalogs by accessing it as a guest user.
-   Verify that the Public option is selected on the Knowledge Article form or Service Catalog page form.

Role required: admin

## About this task

Beginning with the Xanadu release, the Sitemap Generator configuration is available with the base system and is inactive by default.

## Procedure

1.  Navigate to **All** &gt; **Sitemap Generator** &gt; **Sitemap Configuration**.

2.  In the UX Sitemap Configurations \[sys\_ux\_seo\_sitemap\_config\] table, select the sitemap\_config\_CSP record.

3.  Enable the generation of sitemaps.

    1.  On the form, select the **Active** check box.

    2.  In the Sitemap Config Definition related list, double-click the **Type** field and select the **true** option from the list.

    3.  Select the Save icon \(\[Omitted image "save.png"\] Alt text: Save icon\).

4.  Select **Update**.


## Result

All active sitemaps regenerate once in a day and include content from any of their active sitemap definitions.


---
title: Configure catalog item standards property
description: Enable or disable the Catalog Item Standards feature by configuring the "Catalog item standards" property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/configure-catalog-item-standards-property.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-07-06"
reading_time_minutes: 1
breadcrumb: [Catalog item standards for catalog item generation, AI Authoring for Catalog Builder reference, AI Authoring for Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure catalog item standards property

Enable or disable the Catalog Item Standards feature by configuring the "Catalog item standards" property.

## Before you begin

Role required: system administrator

## About this task

The "Catalog item standards" property controls whether best practices from the Catalog Best Practices knowledge article are passed to the LLM during catalog generation. By default, this property is enabled. You can disable it if you don't want best practices to be applied during catalog item creation.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Properties**.

2.  Locate the "Catalog item standards" property in the list.

    The property is displayed with a toggle that shows the current state \(enabled or turned off\).

3.  Select the toggle to enable or turn off the feature:

    -   Enabled: Best practices are passed to the LLM and applied during catalog generation. Users are prompted to confirm deviations from best practices.
    -   Turned off: Best practices aren't passed to the LLM. ServiceNow Otto does not apply best practices or prompt users about deviations.
    The Catalog item standards property is configured. Your setting takes effect immediately for all new catalog generation requests using ServiceNow Otto.

    If you enabled the property, confirm that your best practices are published in the Catalog Best Practices article.


**Parent Topic:**[Catalog item standards for catalog item generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/guidance-for-catalog-item-creation.md)

**Related topics**  


[Catalog item standards for catalog item generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/guidance-for-catalog-item-creation.md)

[Catalog Item Standards scope and examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/catalog-item-standards-scope-and-examples.md)


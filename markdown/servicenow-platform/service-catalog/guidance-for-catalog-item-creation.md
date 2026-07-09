---
title: Catalog item standards for catalog item generation
description: The Catalog Item Standards knowledge base contains a knowledge base article. This article called Catalog Best Practices, has best practices that help Now Assist provide guidance during catalog item creation in Catalog Builder.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/guidance-for-catalog-item-creation.html
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-07-03"
reading_time_minutes: 2
breadcrumb: [Catalog item generation reference, Now Assist in Catalog Builder, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Catalog item standards for catalog item generation

The Catalog Item Standards knowledge base contains a knowledge base article. This article called Catalog Best Practices, has best practices that help Now Assist provide guidance during catalog item creation in Catalog Builder.

When users describe the catalog item they want to create, Now Assist uses published best practices to suggest approaches that improve consistency, performance, and usability of catalog items.

When the feature is enabled, Now Assist compares catalog generation requests with the published standards. If it detects a deviation or identifies a more effective approach, it implements the catalog item and then prompts user with the violations or deviations.

The Catalog Item Standards knowledge base contains the published version of the knowledge article, Catalog Item Standards containing best practices, which is used by the LLM. Note that the latest published version of the article is used, and draft is not considered.

**Note:** Only catalog admins can view or edit the standards content.

## Property toggle configuration

The Catalog item standards property controls whether published catalog item standards are shared with the LLM during catalog item creation. The property is:

-   Available under catalog properties
-   Accessible only to system administrator \[admin\]
-   Enabled by default

When the property is turned off, catalog item standards aren’t sent to the LLM with catalog generation requests. When users create catalog items using Now Assist, the following flow applies:

-   If the Catalog item standards property is enabled, the latest published version of the best practices in the Catalog Best Practices article is passed to the LLM with the catalog generation request.
-   Now Assist creates the required item, but after creating the item, the system provides guidance on applicable best practices. For example, when a mandatory variable is created without help text, the system recommends adding help text for the mandatory part to improve usability.

-   **[Configure catalog item standards property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/configure-catalog-item-standards-property.md)**  
Enable or disable the Catalog Item Standards feature by configuring the "Catalog item standards" property.
-   **[Add and publish best practices to the article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/add-and-publish-custom-catalog-item-best-practices.md)**  
Add your organization's custom best practices to the Catalog Best Practices article and publish them to make them available to the LLM.
-   **[Catalog Item Standards scope and examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/catalog-item-standards-scope-and-examples.md)**  
This reference describes the in-scope best practices that can be used for catalog item generation. It provides examples of in-scope and out-of-scope best practices and documents the rules for how best practices are applied.

**Parent Topic:**[Catalog item generation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/catalog-item-generation-reference.md)

**Related topics**  


[Catalog Item Standards scope and examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/catalog-item-standards-scope-and-examples.md)


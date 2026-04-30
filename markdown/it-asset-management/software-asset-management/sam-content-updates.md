---
title: Content updates for Software Asset Management
description: The Software Asset Management Content Service provides content updates to your instance twice every week that you can use to normalize your data.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Software Asset Management Content Service, Explore, Software Asset Management, IT Asset Management]
---

# Content updates for Software Asset Management

The Software Asset Management Content Service provides content updates to your instance twice every week that you can use to normalize your data.

The following types of content can be updated as part of a content update:

-   Categories
-   Discovery maps
-   Normalization suggestions
-   Product classifications
-   Product license exception rules
-   Product names
-   Product types
-   Publishers
-   Suite definitions
-   Software model life cycles
-   Software model suggestions
-   Custom software product suggestions
-   Common Platform Enumeration \(CPE\) normalization rule

**Note:** Software models aren’t updated when a publisher's name is updated as part of the content updates. The software model isn't updated because its display name is removed from the core company's reference. However, if a product moves to a different publisher, then the software model gets updated during content updates when the product goes from one core company to the other core company. The publisher name is updated for new software models but not for existing software models.

Product types can be updated on a product’s edition level using the Custom Product License Exception Rules \[samp\_cust\_prod\_lic\_excep\_rules\] table. For cases where certain editions are non-licensable, the product type gets updated automatically if the exception rule is defined in the Product License Exception Rules \[samp\_prod\_lic\_excep\_rules\] table or the Custom Product License Exception Rules \[samp\_cust\_prod\_lic\_excep\_rules\] table. However, if a product is non-licensable, an exception rule can’t be created for ​a licensable edition. For this case, you must raise a case with the Content Service team​ with supporting documentation and the team reviews ​whether the edition must be tagged as licensable.

The **SAM - Apply latest content changes** scheduled job runs and processes the content updates. After the content download is complete, the updated content is pulled from the staging columns to the corresponding target columns. Related downstream records are also updated.

A query runs and identifies what transactional data in your instance must be updated with the new content. After the changes are identified, the changes are then propagated to your instance.

Another scheduled job, **SAM - Create suites for a software model**, runs and propagates suite component and life cycle changes to your software models. If you don't want content changes applied to a software model, then you can clear the **Allow automated content updates** flag on the Software Model form. By default, the flag is selected to enable automated content updates to all software models.

**Note:** If a content update adds life-cycle data, it can't be deleted from the software model, but you can deactivate it. Any life-cycle data that is added as part of a content update has the source set to **Servicenow**.

Use the Software Models with deactivated discovery maps report to show software models that are pointing to any deactivated discovery maps.

To see the changes that have been made to the software library, review the SAM Content Audit \[sam\_content\_audit\] table.

**Note:** Content updates don't have an impact on any custom products or custom discovery maps.

For more information on how to send your content to ServiceNow, see [Enable sharing information with Software Asset Management content service](../task/t_EnableSAMContentService.md). For more information on content updates, see [KB0824127](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0824127).

**Parent Topic:**[Software Asset Management Content Service](c_SAMContentService.md)


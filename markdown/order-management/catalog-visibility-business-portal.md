---
title: Configuring product catalog visibility on the Business Portal
description: Only authorized customers can view the product catalog on the Business Portal by default. After setting up your product catalog and pricing, use the CustomerPortalCatalogAccessUtil script include to extend catalog visibility to additional users.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-17"
reading_time_minutes: 1
breadcrumb: [Business Portal, Configure, Sales Customer Relationship Management]
---

# Configuring product catalog visibility on the Business Portal

Only authorized customers can view the product catalog on the Business Portal by default. After setting up your product catalog and pricing, use the CustomerPortalCatalogAccessUtil script include to extend catalog visibility to additional users.

When customers access the Business Portal, the product catalog is visible by default to users who have the sn\_customerservice.customer role and are registered in the ServiceNow CRM software. This default visibility is controlled by the CustomerPortalCatalogAccessUtil script.

To grant product catalog visibility to other users, use the CustomerPortalCatalogAccessUtil script to extend access to those users. Navigate to **All** &gt; **Activity Subscriptions** &gt; **Administration** &gt; **Script Includes**. In the **Name** column, search for CustomerPortalCatalogAccessUtil.

You must also set up your product catalog and configure pricing to help ensure that the correct products and prices are available to customers on the portal. For more information, see [Configuring product offerings and catalogs](som-managing-product-catalogs.md) and [Configuring product pricing](som-managing-product-pricing.md).


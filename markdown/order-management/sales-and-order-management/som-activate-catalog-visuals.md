---
title: Activate the display of product catalog visuals
description: Turn on the display of product images shown in the product tiles of product catalogs by using the sn\_prd\_pm.show\_product\_visuals\_on\_catalog\_ui system property.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales and Order Management]
---

# Activate the display of product catalog visuals

Turn on the display of product images shown in the product tiles of product catalogs by using the **sn\_prd\_pm.show\_product\_visuals\_on\_catalog\_ui** system property.

## Before you begin

Role required: admin

## About this task

The **sn\_prd\_pm.show\_product\_visuals\_on\_catalog\_ui** system property controls the images displayed in commercial product catalogs. This property doesn’t apply to service catalogs or product inventory catalogs.

## Procedure

1.  Navigate to **All** and in the filter enter `sys_properties.list`.

2.  Open the **sn\_prd\_pm.show\_product\_visuals\_on\_catalog\_ui** system property.

3.  In the **Value** field, enter `true` to activate the display of product offering images in the product catalog.

4.  Select **Update**.

    The product offering visuals are loaded in the catalog. If a product offering doesn't have a visual, the text **Image not available** is presented in the product offering tile instead.



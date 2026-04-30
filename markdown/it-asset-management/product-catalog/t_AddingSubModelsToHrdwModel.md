---
title: Add substitute models to a hardware model
description: On a hardware model record, you can add substitutes to track what hardware models can be substituted for another hardware model.
locale: en-US
release: zurich
product: Product Catalog
classification: product-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create hardware models, Models, Product Catalog, IT Asset Management]
---

# Add substitute models to a hardware model

On a hardware model record, you can add substitutes to track what hardware models can be substituted for another hardware model.

## Before you begin

Role required: model\_manager

## About this task

For example, a 19" monitor can be a valid substitute for a 17" monitor. Note that substitutions are directional so, in this case, a 17" monitor is not a substitution for a 19" monitor. Information about valid substitute models is useful when you select models while creating transfer orders.

When you select substitute models, note the following conditions.

-   Substitute models can be used with work management transfer orders. Substitute models are not used in procurement part sourcing.
-   Hardware models included in bundled models cannot be added as substitutes.

## Procedure

1.  Navigate to **All** &gt; **Product Catalog** &gt; **Product Model** &gt; **Hardware Models**.

2.  Click a hardware model **Name**.

3.  Click **Add Substitution**.

4.  In the **Collection** list on the left, double-click a hardware model.

    The hardware model is added to the **List** on the right.

5.  Click **Save**.

    The model is listed in the **Substitutes** related list.


**Parent Topic:**[Create hardware models](t_CreatingHardwareModels.md)

**Related topics**  


[Add compatible models to a hardware model](t_AddingCompModelsToHrdwreModel.md)

[Models](../concept/c_Models.md)

[Bundled models](../concept/c_CreatingBundledModels.md)

[Manage transfer orders](https://www.servicenow.com/docs/access?context=c_TransferOrders&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)

[Procurement](../../procurement/concept/c_Procurement.md)


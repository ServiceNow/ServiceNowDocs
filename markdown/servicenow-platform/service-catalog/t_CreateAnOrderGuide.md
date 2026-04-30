---
title: Create an order guide
description: You can create an order guide with a two-step or three-step ordering process.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Order guides, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an order guide

You can create an order guide with a two-step or three-step ordering process.

## Before you begin

Role required: catalog\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Order Guides**.

2.  Click **New**.

3.  Fill in the fields as appropriate.

    For more information about the fields and their descriptions on the Order guide form, see [Order guide form](../reference/order-guide-form.md).

4.  Right-click the form header and click **Save**.

5.  In the Rule base related list, define the rules that determine which items are included in an order.

    For more information, see [Create a rule](t_CreateARule.md).

6.  Configure the sequence in which the items in a rule base of an order guide must be fulfilled by selecting the **Generate sequence** button.

    For more information, see [Configure a sequence to fulfill items in order guides](generate-order-guide-sequence.md).

7.  In the Variables related list, define any variables required.


-   **[Configure a sequence to fulfill items in order guides](generate-order-guide-sequence.md)**  
Configure a sequence in Playbooks to fulfill items in order guides. Once you define a sequence, you don't have to manually check whether required items have been fulfilled before fulfilling their dependent items.

**Parent Topic:**[Order guides](../concept/c_ServiceCatalogOrderGuides.md)


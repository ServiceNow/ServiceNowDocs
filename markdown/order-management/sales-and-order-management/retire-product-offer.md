---
title: Retire a remote catalog item
description: Retire a product offering or service specification used in a remote catalog, which automatically retires the corresponding remote record producer. When the remote record producer is retired, the remote catalog item is removed automatically from the service catalog on the consumer instance.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Service Exchange Order Management for Providers, Order Management for providers with Service Exchange, Extending Order Management with ServiceNow applications and integrations, Sales Customer Relationship Management]
---

# Retire a remote catalog item

Retire a product offering or service specification used in a remote catalog, which automatically retires the corresponding remote record producer. When the remote record producer is retired, the remote catalog item is removed automatically from the service catalog on the consumer instance.

## Before you begin

Role required: sn\_prd\_pm.product\_catalog\_admin and sn\_prd\_pm.product\_catalog\_manager

## Procedure

1.  In the CSM Configurable Workspace on the provider instance, select the **List** ![](../image/Lists.png) view.

2.  Navigate to the published product offering or service specification to be retired.

    -   To retire a product offering, navigate to **Offerings** &gt; **Product Offerings** and select the product offering to be retired.
    -   To retire a service specification, navigate to **Specifications** &gt; **Service specifications** and select the service specification to be retired.
3.  Select **Retire**.

    The product offering or service specification is set to the Retired state. The state of the associated record producer for the item changes from Published to Retired, and the product catalog item is deleted automatically from the service catalog.



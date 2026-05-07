---
title: Configuring Fallout Management
description: As a provider, you can use Fallout Management to identify, investigate, and resolve order processing issues so that orders can continue processing through to completion.Define your own enterprise-specific fallout types to identify, resolve, and investigate order processing issues so that they can continue processing through to completion.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Order management, Configure, Sales Customer Relationship Management]
---

# Configuring Fallout Management

As a provider, you can use Fallout Management to identify, investigate, and resolve order processing issues so that orders can continue processing through to completion.

The fallout type is a category that indicates the type of fallout activity. Billing Issue, Inventory Allocation Failure, and Provisioning Failure fallout types are standard in the ServiceNow AI Platform. You can define additional ones, according to the requirements of your enterprise. To learn more about managing order task fallout, see [Managing order fallout](fallout-management-overview.md).

**Parent Topic:**[Configuring Order Management](order-mgt-configuring.md)

## Create additional fallout types

Define your own enterprise-specific fallout types to identify, resolve, and investigate order processing issues so that they can continue processing through to completion.

### Before you begin

Role required: admin

### About this task

The fallout type is a category that indicates the type of fallout activity. Billing Issue, Inventory Allocation Failure, and Provisioning Failure fallout types are standard in the ServiceNow AI Platform. You can define additional ones, as per the requirements of your enterprise. To learn more about managing order task fallout, see [Managing order fallout](fallout-management-overview.md).

### Procedure

1.  Log in to the ServiceNow instance.

2.  In the application navigator, enter `sn_fallout_mgmt_fallout_type.list`.

3.  Select **New**.

4.  In the **Name** field, enter the name of the fallout type.

5.  Add a brief description in the **Description** field.

6.  Select **Submit**.



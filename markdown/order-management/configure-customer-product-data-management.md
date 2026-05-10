---
title: Configure customer product data management
description: Learn how to use the sn\_ind\_tmt\_orm.enable\_prod\_invt\_for\_order\_management system property to either create sold products or product inventory records after an order is completed and fulfilled.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure order fulfillment, Order management, Configure, Sales Customer Relationship Management]
---

# Configure customer product data management

Learn how to use the sn\_ind\_tmt\_orm.enable\_prod\_invt\_for\_order\_management system property to either create sold products or product inventory records after an order is completed and fulfilled.

## Before you begin

Role required: admin

## About this task

The following table lists the values that you can set for the sn\_ind\_tmt\_orm.enable\_prod\_invt\_for\_order\_management system property depending on whether you want to create an entry in the Sold Products \[sn\_install\_base\_sold\_product\] table or Product Inventory \[sn\_prd\_invt\_product\_inventory\] table after an order is fulfilled.

|Value|Description|
|-----|-----------|
|True|Create a record in the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table. This is the default setting.|
|False|Create a record in the Sold Products \[sn\_install\_base\_sold\_product\] table.|

**Note:** You can choose to create either sold products or product inventory records, but not both.

## Procedure

1.  Log in to the ServiceNow instance.

2.  Select **All**.

3.  Switch the application scope to Order Management.

4.  Enter `sys_metadata.list` in the Filter text box.

5.  On the Application Files list view, search and select the `sn_ind_tmt_orm.enable_prod_invt_for_order_management` property from the Display name column.

6.  On the System Property form, specify a value in the **Value** depending on how you want to create inventory records.

7.  Select **Update**.


**Parent Topic:**[Configure order fulfillment](../../tmt-order-mgt/concept/configure-order-fulfillment.md)

**Related topics**  


[Creation of sold product and product inventory records](../../tmt-order-mgt/concept/order-mgt-sold-product-creation.md)

[Managing post-fulfillment order changes](../../tmt-order-mgt/concept/managing-orders.md)

[Product data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/product-data.md)


---
title: Modifications in the checkout form
description: You can modify the checkout form to use an alternate description field or to add request item number for each line.Add the request item number to display this number as an extra column on the checkout form. By default, the request item number is not displayed in the list.Use an alternate description field to describe your category item in the checkout form. By default, the short\_description column of the catalog item appears as the item description.
locale: en-US
release: xanadu
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Legacy flexible checkout and delivery forms, Cart layout, Service Catalog customization, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Modifications in the checkout form

You can modify the checkout form to use an alternate description field or to add request item number for each line.

By default, the checkout forms list the **Description**, **Delivery Date**, **Stage**, **Price**, **Quantity,** and **Total** columns. An example of default checkout form is shown:

![Screenshot for checkout default](../image/CheckoutDefault.png "Checkout default")

**Parent Topic:**[Legacy flexible checkout and delivery forms](c_FlexibleCheckoutAndDeliveryForms.md)

## Add the request item number on checkout form

Add the request item number to display this number as an extra column on the checkout form. By default, the request item number is not displayed in the list.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Properties**.

2.  Locate the property: **Show the request item number for each line item on the checkout screen \(default false\)**.

3.  Select the **Yes** check box to add the number column to the checkout form.

    ![Screenshot for checkout number](../image/CheckoutNumber.png "Checkout number")


## Use an alternate description field on the checkout form

Use an alternate description field to describe your category item in the checkout form. By default, the **short\_description** column of the catalog item appears as the item description.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Policy** &gt; **Properties**.

2.  Locate the property **Field name to use for the description column of the checkout form. If blank, the default \(short\_description\) is used**.

3.  Enter the name of the alternative field \(a column in the Catalog Item `[sc_cat_item]` table\) and save it.

    For example, if you've selected **name**:

    ![Screenshot for checkout name.](../image/CheckoutName.png "Checkout name")



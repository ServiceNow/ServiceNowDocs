---
title: Service Catalog checkout models
description: The service catalog defaults to one-step checkout model, but also allows two-step checkout. Administrators and users with the catalog\_admin role can enable and configure the two-step checkout model and control how the delivery address is populated.You can enable the two-step checkout to specify a recipient, delivery address, and special instructions for an order.Administrators can control how the delivery address is populated. By default the delivery address is defined by the client script called set location.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Catalog request fulfillment, Service Catalog configuration, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service Catalog checkout models

The service catalog defaults to one-step checkout model, but also allows two-step checkout. Administrators and users with the catalog\_admin role can enable and configure the two-step checkout model and control how the delivery address is populated.

The service catalog defaults to a one-step checkout model. When a user clicks **Proceed to checkout** or **Order now**, items in the shopping cart are ordered and the order summary or status screen appears. The one-step checkout model runs in the following order:

**Press Checkout** &gt; **Order Summary**

The service catalog also supports a two-step checkout model. Under this model, when a user clicks **Proceed to checkout** or **Order now**, an order confirmation screen appears. You can edit the order, choose a delivery location, or upload an attachment before submitting the order. The two-step checkout model runs in the following order:

**Press Checkout Order** &gt; **Confirmation Screen** &gt; **Submit Order** &gt; **Order Summary**.

Access check for a catalog item is performed during its checkout. This check is also applicable in scripts and APIs.

**Parent Topic:**[Service Catalog request fulfillment](request-fulfillment.md)

## Enable the two-step checkout process

You can enable the two-step checkout to specify a recipient, delivery address, and special instructions for an order.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Properties**.

2.  Locate the property Use the two step catalog checkout model \(default false\).

3.  Select the **Yes** check box to enable the two-step process.

4.  Locate the property Show the 'Back to Catalog' button on the two step checkout screen.

5.  Select the **Yes** check box to provide a button that navigates back to the catalog from the order confirmation screen \(default\).

    Clear the check box to hide the button.


## Specify requester location

Administrators can control how the delivery address is populated. By default the delivery address is defined by the client script called set location.

When the two-step checkout process is enabled, the `set location` script retrieves the address of the user and enters formatted details in the Deliver to field.


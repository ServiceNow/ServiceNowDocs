---
title: Providing Order and Shipping Confirmation URLs to Punchout Suppliers
description: When integrating with a punchout supplier, customers are required to provide specific URLs for Order Confirmation and Shipping Confirmation.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure punchout for third-party site purchases, Configuring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Providing Order and Shipping Confirmation URLs to Punchout Suppliers

When integrating with a punchout supplier, customers are required to provide specific URLs for Order Confirmation and Shipping Confirmation.

These URLs must be configured correctly to confirm seamless communication between the customer's instance and the punchout supplier’s system.

<table id="table_ny3_1j2_52c"><thead><tr><th>

URL name

</th><th>

URL format

</th></tr></thead><tbody><tr><td>

Order Confirmation URL

</td><td>

`instance-name`/api/sn\_spend\_intg/punchout/orderconfirmation/`sys_id`

</td></tr><tr><td>

Shipping Confirmation URL

</td><td>

`instance-name`/api/sn\_spend\_intg/punchout/shippingconfirmation/`sys_id`

</td></tr></tbody>
</table>Where:

-   `instance-name` is the customer’s instance name.
-   `sys_id` is the unique system ID of the punchout supplier record stored in the Supplier \(sn\_fin\_supplier\) table.


**Parent Topic:**[Configure punchout for third-party site purchases](../task/configure-supplier-punchout.md)


---
title: Purchase order expected delivery date
description: The purchase order record and the purchase order line item record both contain the Expected delivery date field.
locale: en-US
release: xanadu
product: Procurement
classification: procurement
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a purchase order, Procurement purchase order management for assets, Procurement, IT Asset Management]
---

# Purchase order expected delivery date

The purchase order record and the purchase order line item record both contain the **Expected delivery** date field.

The **Expected delivery** field can be edited on both records. Editing the field on one record can change the field on the other record.

-   If you add an expected delivery date to the purchase order and the expected delivery date field on the purchase order line item is blank, the date on the purchase order is added automatically to the purchase order line item.
-   If you add an expected delivery date on the purchase order line item and the expected delivery date field on the purchase order is blank, the date on the purchase order line item is added automatically to the purchase order.
-   If the purchase order and the purchase order line item have the same expected delivery date and you change the date on the purchase order, the date is changed automatically on the purchase order line item.
-   If you change the date on the purchase order line item to a date that is later than the one specified on the purchase order, the date on the purchase order is changed to the new date. The expected delivery date of a purchase order line item cannot be later than the expected delivery date on the associated purchase order.
-   If you change the date on the purchase order line item to a date that is earlier than the date specified on the purchase order, the date on the purchase order remains the same.

**Parent Topic:**[Create a purchase order](../task/t_CreateAPurchaseOrder.md)


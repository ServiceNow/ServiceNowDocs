---
title: Configure a reservable view on a reservable module
description: Assign different views on a reservable mobile. The workplace items of the module can be viewed in the configured views while making a reservation on the Reservation portal.
locale: en-US
release: yokohama
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a reservable view, Configure, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Configure a reservable view on a reservable module

Assign different views on a reservable mobile. The workplace items of the module can be viewed in the configured views while making a reservation on the Reservation portal.

## Before you begin

The Workplace Reservation Management by default assigns the following views to a reservable module until they are set to False.

-   Card view
-   Schedule view

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Reservable Module**.

2.  Select the reservable module to which you want to assign a reservable view.

3.  On the form, scroll down to the Reservable Views related list.

4.  Click **Edit...**.

5.  On the Edit members form, set the filter option **Active** to **True**.

6.  Select the reservable view by doing the following:

    1.  Select the time slot from the **Collection** column on the left.

    2.  Move the selection to the **Reservable Views List** column on the right.

        To move the time slot, use the add/remove icon \(![Add remove reservable views icon](../image/add-remove-icon.png)\).

    3.  Click **Save**.

7.  To set a default reservable view, set the **is default** value of the reservable view as **True**.

    Ensure that except the selected default reservable view, the value of all other reservable views are set to **False**.

8.  To specify an order in which the reservable views must be displayed on the portal, do the following:

    1.  Select the Preview icon \(![preview icon](../image/info-icon.png)\).

    2.  Click **Open Record**.

    3.  On the Reservable Module View Configuration form, specify the **Order**.

    4.  Click **Update**.

    5.  Repeat the same procedure until you specify the order for every reservable view.


## Result

The reservable view is added to the module. The workplace items of the module can be viewed in the selected view.

**Parent Topic:**[Create a reservable view](create-a-reservable-view.md)


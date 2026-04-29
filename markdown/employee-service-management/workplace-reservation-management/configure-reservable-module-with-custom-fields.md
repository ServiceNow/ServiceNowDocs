---
title: Configure reservable module with additional details
description: The application enables you configure a reservable module with additional details based on your organization's requirements.
locale: en-US
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure a reservable module, Configure Workplace Reservation Management portal, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Configure reservable module with additional details

The application enables you configure a reservable module with additional details based on your organization's requirements.

## Before you begin

Verify that you have the following details.

-   Workplace data for your organization
-   Data of workspaces that can be marked as available
-   Record producer with the additional details fields. Refer to [Create a record producer to add additional details](create-a-record-producer-to-add-additional-fields.md).

Role required: sn\_wsd\_rsv.admin

## About this task

Configure a reservable module to use the additional details fields that you want to display on the reservation form when employees make a reservation. The fields appear under an additional details section, along with the existing form fields provided by the application based on your configuration. For more information about the reservable module configuration, refer to [Configure a reservable module](config-reservable-module.md).

The additional details are displayed when an employee requests a single, multi, recurring and a group reservation. The details entered in the additional details are also displayed in the Reservation summary of the reservation.

To add custom fields:

-   You must create a record producer with the fields. Refer to [Create a record producer to add additional details](create-a-record-producer-to-add-additional-fields.md).
-   Link the reservable module with the record producer.

## Procedure

1.  Navigate to **All** &gt; **Workplace Reservation Management** &gt; **Administration** &gt; **Reservable Module**.

2.  Select **New** if you want to create a reservable module.

    To fill the form, refer to [Configure a reservable module](config-reservable-module.md).

3.  Select the reservable module to which you want to add additional details.

4.  On the Reservable module form, select **Reservation Widget Configuration**.

5.  In the **Additional details record producer**, select the record producer that you created with the additional details.

6.  Select **Update**.


## Result

The reservable module is configured with additional details.

**Parent Topic:**[Configure a reservable module](config-reservable-module.md)


---
title: Configure badging data choices
description: The Badging Data Choices table \(sn\_wsd\_wc\_badging\_data\_choice\) contains the badging status details for Swipe-in and Swipe-out event types. You can create multiple badging states and assign the appropriate event type.
locale: en-US
release: zurich
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2025-09-01"
reading_time_minutes: 1
breadcrumb: [Configure, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Configure badging data choices

The Badging Data Choices table \(sn\_wsd\_wc\_badging\_data\_choice\) contains the badging status details for Swipe-in and Swipe-out event types. You can create multiple badging states and assign the appropriate event type.

## Before you begin

**Note:** The application comes with pre-filled values for CheckIn\_AccessGranted and CheckOut\_AccessGranted status and you can’t modify or delete these values. However, you can create multiple statuses and set the event type as required.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Badging Choices**.

2.  Select **New**.

3.  On the form, fill in the fields:

<table id="table_dc3_kqd_52c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status

</td><td>

The badging data status. For example, Access Granted.

</td></tr><tr><td>

Application

</td><td>

Name of the application. Default value: Workplace Connectors.

</td></tr><tr><td>

Value

</td><td>

The minimum or maximum value of the specified badging status. Enter the value within the range 1–99.

</td></tr><tr><td>

Type

</td><td>

Option to select the event types:-   Swipe-in
-   Swipe-out


</td></tr></tbody>
</table>
**Parent Topic:**[Configure Workplace Connectors](../concept/configure-workplace-connectors.md)

**Previous topic:**[Configure data Sources and schedule imports](import-data-connector.md)

**Next topic:**[Setup Workplace Connectors for badging data](../concept/setup-workplace-connectors.md)


---
title: Employee attendance data
description: The Employee Attendance data \[sn\_wsd\_wc\_employee\_attendance\_data\] is the target table that contains the employee badging data and employee access records.
locale: en-US
release: australia
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setup Workplace Connectors for badging data, Configure Workplace Connectors, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Employee attendance data

The Employee Attendance data \[sn\_wsd\_wc\_employee\_attendance\_data\] is the target table that contains the employee badging data and employee access records.

## Before you begin

The **Process Provider Data Record** scheduled job runs periodically \(every five minutes\) and loads the badging data into the Employee Attendance table. It collects the data from the source table \(badging data\) and transforms it in the required format before loading it in the target \(Employee Attendance Data\) table.

Role required: sn\_wsd\_wc.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Connectors** &gt; **Badging Readers** &gt; **Employee Attendance Data**.

2.  Select **New**.

3.  Fill in the form fields.

<table id="table_s51_kqn_vbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User

</td><td>

Option to select the user from the workplace profile.

</td></tr><tr><td>

Location

</td><td>

Option to select workplace locations.Ihe user workplace profile, the **Location** field must be updated with the correct location and the **Workplace entity** column is mapped to the user workplace profile.

</td></tr><tr><td>

Event type

</td><td>

Option to select the event types: -   Swipe-in
-   Swipe-out
Select **Swipe-in**.

</td></tr><tr><td>

State

</td><td>

Option to select the badging data state: -   Access Granted
-   Access Denied
-   Blocked
Select **Access Granted**.

</td></tr></tbody>
</table>    The Employee Attendance table data is loaded to the Attendance Analytics table to generate space occupancy metrics in Workplace Central. For more information, see [Attendance Analytics](attendance-analytics.md).


**Parent Topic:**[Setup Workplace Connectors for badging data](../concept/setup-workplace-connectors.md)

**Previous topic:**[Configure a webhook event](configure-webhook-restapi.md)

**Next topic:**[Attendance Analytics](attendance-analytics.md)


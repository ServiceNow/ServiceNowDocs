---
title: Configure inventory-based scheduling for a center
description: Configure scheduling based on available inventory for a center.
locale: en-US
release: australia
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure inventory-based scheduling for a center

Configure scheduling based on available inventory for a center.

## Before you begin

Navigate to **Vaccine Administration Management** &gt; **Administration** &gt; **Properties**, and make sure that the **Enables vaccine inventory management** property \(**sn\_vaccine\_sm.enable\_inventory\_management**\) is selected.

**Warning:** Once you have enabled the property and your inventory-based configurations are live, avoid disabling the property to help prevent any data inconsistencies.

Role required: sn\_vaccine\_sm.admin or sn\_vaccine\_sm.inventory\_manager

## About this task

Configure scheduling based on available inventory for a center. Inventory-based scheduling enables you to limit appointment booking based on the available inventory for that day. For example, say that a center has 200 available doses and 500 available appointment slots for a particular day. Because there are only 200 doses, appointment booking would be capped at 200 appointments for that day.

When you receive a vaccine supply lot at a particular center, you can provide details about the lot for the vaccine type, number of doses, expiration date, and so on. You can add it to your inventory. You can then automate or manually distribute the inventory over a specified date range. You can also manually track wasted doses.

**Important:** This feature is only available for user-scheduled appointments. It isn’t currently supported for mass booking.

## Procedure

1.  Navigate to **Vaccine Administration Management** &gt; **Administration** &gt; **Programs**.

2.  Open a program record.

3.  In the Center related list, open a vaccination center record.

4.  In the Vaccine Supply Lots related list, create a new record for each vaccine supply lot that you receive at that location.

    1.  Click **New**.

    2.  On the form, fill in the fields.

<table id="table_oxx_5nf_v4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lot number

</td><td>

Number of the lot.

</td></tr><tr><td>

Vaccine model

</td><td>

Vaccine model of the lot.

</td></tr><tr><td>

Center

</td><td>

Program center that the lot is located.

</td></tr><tr><td>

Available from

</td><td>

Date that the lot is available from.

</td></tr><tr><td>

Expires on

</td><td>

Date that the lot expires, as specified by the manufacturer.

</td></tr><tr><td>

Notes

</td><td>

Notes about the lot.

</td></tr><tr><td>

Total number of doses

</td><td>

Total number of doses in the lot. This number must be manually calculated by the inventory manager.

</td></tr><tr><td>

State

</td><td>

State of the lot:

-   **Not available**
-   **Available**


</td></tr></tbody>
</table>    3.  Select and hold \(or right-click\) the form header and click **Save**.

    4.  To confirm that the lot was received and is included in the inventory for that location, click **Make Available**.

5.  To distribute the lot automatically.

    1.  Open the vaccine supply lot record.

    2.  Click **Distribute**.

        The lot is evenly distributed over a specified number of business days based on the location's appointment scheduling configuration. For example, say that the lot is distributed over seven days at a center that is closed on Saturday and Sunday. If the lot distribution begins on Monday, then it’s evenly distributed over the next seven business days \(Monday through Friday of that week, and then the following Monday and Tuesday\).

        **Note:**

        By default, the number is set to seven days. To change the number of days, navigate to **Vaccine Administration Management** &gt; **Administration** &gt; **Properties**, and update the **Number of days to distribute a lot** property \(**sn\_vaccine\_sm.im\_lot\_distribution\_day\_count**\).

        When you distribute the lot automatically, you have the option to manually adjust the allocated doses for an individual day. Open the Vaccine Availability by Lot record for the day that you want to update the doses for, and then update the **Allocated Doses** field.

6.  To distribute the lot manually.

    1.  Open the vaccine supply lot record.

    2.  In the Vaccine Availability related list, click **New**.

    3.  On the form, fill in the fields.

<table id="table_pqz_g4f_v4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Center

</td><td>

Center that the vaccine is available from.

</td></tr><tr><td>

Available on

</td><td>

Date that the vaccine is available from.

</td></tr><tr><td>

Vaccine model

</td><td>

Vaccine model of the program.

</td></tr><tr><td>

Allocated doses

</td><td>

This field value is automatically set.

</td></tr><tr><td>

Booked doses

</td><td>

This field value is automatically set.

</td></tr><tr><td>

Used doses

</td><td>

This field value is automatically set.

</td></tr><tr><td>

Wasted doses

</td><td>

Number of wasted doses per day. This number must be manually entered by the inventory manager.

</td></tr><tr><td>

Notes

</td><td>

Notes about the availability of the vaccine.

</td></tr></tbody>
</table>    4.  Select and hold \(or right-click\) the form header and click **Save**.

    5.  In the Availability By Lot related list, click **New**.

    6.  On the form, fill in the fields.

<table id="table_xyz_5wh_v4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Supply Lot

</td><td>

Lot to associate with the vaccine availability.

</td></tr><tr><td>

Available On

</td><td>

Date that the vaccine is available from. The date must be within the availability and expiration range of the associated lot.

</td></tr><tr><td>

Allocated Doses

</td><td>

Number of allocated doses. The number of allocated doses must be less than the total number of doses available in the associated lot.

</td></tr><tr><td>

Notes

</td><td>

Notes about the vaccine availability for this lot.

</td></tr></tbody>
</table>    7.  Click **Submit**.

    8.  To create more records for vaccine availability, repeat the Availability By Lots procedure, as needed.


**Parent Topic:**[Configuring Vaccine Administration Management](../concept/vaccine-mgmt-config.md)


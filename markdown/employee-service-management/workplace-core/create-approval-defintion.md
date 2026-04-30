---
title: Create an approval definition
description: Add an approval definition so that you can implement an approval process that is over that definition. The approval is applied on reservations that match the conditions.
locale: en-US
release: xanadu
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a workplace performer criteria, Manage workplace safety activities, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Create an approval definition

Add an approval definition so that you can implement an approval process that is over that definition. The approval is applied on reservations that match the conditions.

## Before you begin

**Important:** Starting with Workplace Reservation Management version 2.1.2, the approval options function as follows:

-   For existing customers, it was possible to configure approval functionality on the Reservable module to approve reservations. After the upgrade, this possibility remains the same until a new approval definition is configured using the following procedure. After you configure a new approval definition, the approval process will run based on the upgrade.

    After the upgrade, disable the **WSD Reservation Approval Flow** in the **Flow designer**.

-   For new customers, the following procedure explains how to configure an approval definition to approve a reservation.

Role required: sn\_wsd\_core.admin

## Procedure

1.  Navigate to **Workplace Core** &gt; **Administration** &gt; **Approval Definitions**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_vbd_scp_fsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the approval definition.

</td></tr><tr><td>

Applicable to

</td><td>

Table on which the approval definitions must be applied.

</td></tr><tr><td>

Application

</td><td>

Application for which you are creating the approval definition. This field is automatically set.

</td></tr><tr><td>

Active

</td><td>

Option to activate the approval definition.

</td></tr><tr><td>

Order

</td><td>

Order in which the approval definition must be implemented. For example, if you the selected Reservation table in the **Applicable to** field and there a reservation matches more than one approval definition, then the approval definition with the lowest order is applied. However, do not maintain approval definitions with the same order.

</td></tr><tr><td>

Conditions

</td><td>

Option to add filter conditions based on which the approval definition must be implemented. The conditions are applied on the table selected in the **Applicable to** field. To add a condition, select **Add filter condition**. To add an OR clause, select **Add "OR" clause**.For example, if the Reservation table is selected in the **Applicable to** field, then the approval definition is implemented on the reservations that match the filter conditions.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Result

The approval definition is created for the reservation table. If a reservation matches more than one approval definition, then the approval definition with the lowest order is applied.

## What to do next

Add approvers to approve the reservations that match the approval definition. For more information, refer to [Add a workplace approval configuration](add-workplace-approval-configuration.md).

**Parent Topic:**[Create a workplace performer criteria](create-workplace-performer-criteria.md)


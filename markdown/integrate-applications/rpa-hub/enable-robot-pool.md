---
title: Enable robot pool for a bot process in RPA Hub
description: Enable robot pool for a bot process in RPA Hub to effectively allocate robots for it's execution and for distribution of work load.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Enable robot pool for a bot process in RPA Hub

Enable robot pool for a bot process in RPA Hub to effectively allocate robots for it's execution and for distribution of work load.

## Before you begin

Familiarize yourself with robot pool concepts. For more information, see [Robot pool in RPA Hub](../concept/robot-pool-rpa.md).

Create a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

Create a robot pool. For more information, see [Create a robot pool in RPA Hub](create-robot-pool.md).

Associate a queue to the bot process. For more information, see [Associate a queue to the bot process from the related list](associate-queue-botprocess.md).

If an RPA developer and RPA support user are a part of the Managed by Group, then they can view and edit these fields.

RPA business user can view these fields.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open a bot process.

5.  On the **Details** tab, in the Robot Pool section, fill in the fields.

<table id="table_d2k_vjy_5xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable Robot Pool

</td><td>

Option to enable the robot pool for the bot process.On enabling this option, the **Assign Robots** tab on the bot process is hidden.

For more information about robot pool, see [Robot pool in RPA Hub](../concept/robot-pool-rpa.md).

</td></tr><tr><td>

Robot Pool

</td><td>

Robots that you can allocate dynamically from a selected robot pool.Select a robot pool from a list of existing robot pool names.

This field appears only when the **Enable Robot Pool** option is selected.

</td></tr><tr><td>

Allocation Type

</td><td>

Robots that you can allocate based on the Service Level Agreement \(SLA\) of the work items or the percentage of efficiency gain. Select the allocation type:

-   **SLA Based**: Allocation of robots from the pool based on the SLA of the work item. The work items are sorted and prioritized based on the SLA.

If you select the allocation type as SLA Based, ensure that the work items must contain a Service Level Agreement \(SLA\).

-   **Percentage Reduction**: Allocation of robots from the pool based on the efficiency percentage.
The default value is SLA Based.

This field appears only when **Enable Robot Pool** option is selected.

</td></tr><tr><td>

Percentage Reduction

</td><td>

This field appears only when **Percentage Reduction** is selected from the **Allocation Type** field.Reduce the total execution time of a bot process by allocating more robots by a selected percentage.

For example, if there are 100 work items assigned to a bot process. It might take 100 minutes to execute the bot process. If you want to reduce that time to 75 minutes, you define a value 25 in this field.

After you provide a value in this field, multiple robots are allocated to distribute the work load. Thus, the automation performs faster by that percentage.

The default value is 25.

Robots are allocated to distribute the workload, based on the percentage you select:

-   If you select a value from 5 to 50, 2 robots are allocated.
-   If you select 55, 60, or 65, 3 robots are allocated.
-   If you select 70 or 75, 4 robots are allocated.
-   If you select 80, 6 robots are allocated.
-   If you select 85, 7 robots are allocated.


</td></tr></tbody>
</table>

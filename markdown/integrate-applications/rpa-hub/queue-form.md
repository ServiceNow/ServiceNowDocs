---
title: Queue form in RPA Hub
description: Use the Work Queue form to create a queue. A queue lists the work items that you want the robot to process.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [RPA Hub reference, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Queue form in RPA Hub

Use the Work Queue form to create a queue. A queue lists the work items that you want the robot to process.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the work queue.

</td></tr><tr><td>

Is Work Item Name Unique

</td><td>

Option to select if the name of each item in this queue is unique.

</td></tr><tr><td>

Application

</td><td>

\[Auto generated\] Application containing this record.Role required to view this field: admin.

</td></tr><tr><td>

Maximum Attempts

</td><td>

Number of attempts for failed work items.Enter a value between 1 and 99 \[maximum value from system properties\].

 The default value is 1.

 Roles required to edit this field: RPA release manager and RPA admin.

</td></tr><tr><td>

Attempt Delay \(mins\)

</td><td>

Maximum delay, in minutes, before the work item is attempted again.The default value is 0.

 Roles required to edit this field: RPA release manager and RPA admin.

 This field appears only when the value of the **Maximum Attempts** field is more than 1.

</td></tr><tr><td>

Description

</td><td>

Brief description of the work queue.

</td></tr><tr><td class="sub-head" colspan="2">

Purge-Work Items

</td></tr><tr><td>

Purge Status

</td><td>

Status of the work items that need to get purged.

</td></tr><tr><td>

Purge After \(days\)

</td><td>

Number of days after which the work items get deleted based on the date of creation.

</td></tr><tr><td class="sub-head" colspan="2">

Average Handling Time \(AHT\) - Work ItemsWork items with Success status and that are not purged, are included for AHT calculation.

</td></tr><tr><td>

Include All Work Items

</td><td>

Successful work items that are considered for the Average Handling Time \(AHT\) calculation.For more information about robot pool, see [Robot pool in RPA Hub](../concept/robot-pool-rpa.md).

</td></tr><tr><td>

Work Item Count

</td><td>

Number of recent successful work items that are considered for the Average Handling Time \(AHT\) calculation.Enter a value between 20 and 1000.

The default value is 100.

This field appears only when the value of the **Include All Work Items** option is cleared.

For more information about robot pool, see [Robot pool in RPA Hub](../concept/robot-pool-rpa.md).

</td></tr><tr><td class="sub-head" colspan="2">

Compose

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Work notes for the work queue.

</td></tr><tr><td>

Additional Comments

</td><td>

Additional comments related to the work queue.

</td></tr></tbody>
</table>**Parent Topic:**[RPA Hub reference](rpa-hub-reference.md)

**Related topics**  


[Create a queue in RPA Hub](../task/create-queue.md)

[Using auto-retry functionality for your failed work items in RPA Hub](../concept/auto-retry-wqi-rpa.md)

[Work item form in RPA Hub](work-queue-form.md)

[Queue implementation in RPA Hub](../concept/queues-implement-rpa.md)


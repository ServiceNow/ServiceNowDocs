---
title: View maintenance requests in RPA Hub
description: After a scheduled maintenance event card is accepted or rejected on the robot calendar, a maintenance request is created for tracking.Use the Maintenance request form to track the status of the scheduled maintenance \(SM\) days on the robot calendar. After a scheduled maintenance event card is accepted or rejected on the robot calendar by an RPA release manager or an admin, then a maintenance request is created for tracking.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Monitor, RPA Hub, Workflow Data Fabric]
---

# View maintenance requests in RPA Hub

After a scheduled maintenance event card is accepted or rejected on the robot calendar, a maintenance request is created for tracking.

## Before you begin

Ensure that the RPA business user, RPA developer, and RPA support user are in the Managed by Group list of the bot process which is associated to the request. This is applicable with the associated CI is a bot process.

Role required: sn\_rpa\_fdn.rpa\_business\_user, sn\_rpa\_fdn.rpa\_support\_user, sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_release\_manager, or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Monitor**, select **Maintenance Requests**.

4.  Open a maintenance request to view the details.


**Parent Topic:**[Monitoring automations](../concept/monitoring-automations-rpa.md)

**Related topics**  


[Manage scheduled maintenance days in RPA Hub](manage-sm-request-rpa.md)

[Scheduled maintenance days in RPA Hub](../concept/sm-days-rpa.md)

## Maintenance request form in RPA Hub

Use the Maintenance request form to track the status of the scheduled maintenance \(SM\) days on the robot calendar. After a scheduled maintenance event card is accepted or rejected on the robot calendar by an RPA release manager or an admin, then a maintenance request is created for tracking.

<table id="table_ucf_k2x_2rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated number of the maintenance request.

</td></tr><tr><td>

Change request

</td><td>

Associated change request.

</td></tr><tr><td>

Planned Start Date

</td><td>

Planned start date and time of the scheduled maintenance.

</td></tr><tr><td>

Planned End Date

</td><td>

Planned end date and time of the scheduled maintenance.

</td></tr><tr><td>

State

</td><td>

State of the maintenance request:-   **Pending** - An MR is created when you accept the associated SM event card.
-   **In Progress** - When the planned start date begins, the MR is executed. The life cycle stage status of the configuration item \(robot or bot process\) moves to In Maintenance state.
-   **Complete** - When the MR completes execution of the configuration item \(robot or bot process\). When the associated CR is closed, then the life cycle stage status of the Configuration Item \(CI\) moves to Published state.
-   **Canceled** - When an MR is canceled. For more information about canceling an MR, see [Scheduled maintenance days in RPA Hub](../concept/sm-days-rpa.md) and [Manage scheduled maintenance days in RPA Hub](manage-sm-request-rpa.md).
-   **Failed** - When a CI \(robot or bot process\) fails due to any issue.

When the system tries to update the CI to either in Published or In Maintenance, but unable to update. Then the MR fails.

-   **Rejected** - When you reject the associated SM event card.

</td></tr><tr><td>

Configuration Item

</td><td>

Name of the associated bot process or robot.

</td></tr><tr><td>

Class

</td><td>

Type of the configuration item. For example, bot process or robot.

</td></tr></tbody>
</table>**Note:** Maintenance Request \(MR\) is unique for Change Request \(CR\), except for **Canceled** and **Failed** states.


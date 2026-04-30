---
title: Manage scheduled maintenance days in RPA Hub
description: Track scheduled maintenance days on the Robot Calendar tab to manage your current and future automations.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Manage scheduled maintenance days in RPA Hub

Track scheduled maintenance days on the **Robot Calendar** tab to manage your current and future automations.

## Before you begin

Ensure you’re familiar with scheduled maintenance days concepts. For more information, see [Scheduled maintenance days in RPA Hub](../concept/sm-days-rpa.md).

Create a change request from the **Change** module. For more information, see [Create a change request](https://www.servicenow.com/docs/access?context=t_CreateAChange&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US). Ensure to do the following tasks while creating a change request:

-   On the Change Request \(CR\) form, in the **Configuration item** field, select the associated bot process, robot, or machine \(for which the robot is associated when a machine name look up is enabled\). Also, select an assignment group.
-   On the Schedule tab, enter the planned scheduled maintenance start and end dates along with time, in **Planned start date** and **Planned end date** fields, respectively. Ensure that the **Planned start date** is not empty.
-   After you save the change request, select **Request Approval** to move it to the Assess state.
-   Next, approve the change request. For more information, see [Process a change request](https://www.servicenow.com/docs/access?context=t_ProcessAChangeRequest&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US). To view the scheduled maintenance on a robot calendar, the change request can either be in either Scheduled, Implement, or Review states.

Ensure to enable the **sn\_rpa\_fdn.enable\_unattended\_robot\_machine\_name\_lookup** system property, to map the robot to the virtual machine.

Ensure to map the logged-in user timezone in the RPA timezone for scheduled maintenance reflection on the robot calendar.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  On the RPA Hub workspace home page, select a change request depending on the configuration item \(CI\):

    -   If the CI is a robot, select a change request from the **Changes to robots** section.
    -   If the CI is a bot process, select a change request from the **Changes to bot processes** section.
3.  From the Configuration Item column, select the associated robot or the bot process.

    The associated robot form or the bot process form opens.

4.  Navigate to the robot calendar from the form header, depending on the CI:

    -   If the CI is a robot, select **Robot Calendar**.
    -   If the CI is a bot process, select **Show Robot Calendar**.
5.  If the CI is a bot process, in the **Select the robot to view the calendar** dialog box, select a robot from the Robot list and then, select **Continue**.

    If the robot pool feature is enabled, all the robots associated to that pool appear in the Robots list. Else, all the robots in the assigned robots appear in the Robots list.

6.  On the **Robot Calendar** tab, perform any of the following tasks:

<table id="table_zc4_qxr_zxb"><thead><tr><th>

Option

</th><th>

Action

</th><th>

Result

</th></tr></thead><tbody><tr><td>

To create a scheduled maintenance on the robot calendar, if the associated CI is either in Build or In Maintenance state.

</td><td>

Select a scheduled maintenance \(SM\) event card and select **Accept**.

</td><td>

A maintenance request \(MR\) is created with Pending state.The executions are stopped until the CR is closed.

</td></tr><tr><td>

To create a scheduled maintenance on the robot calendar, if the associated CI is in Published state.

</td><td>

-   Select an SM event card and select **Accept**.
-   In the **Do you want to accept the CR?** confirmation dialog box, select **Accept**.


</td><td>

An MR is created with Pending state. The associated CI moves to In Maintenance state during the planned scheduled maintenance time frame. The executions are stopped until the CR is closed. Then, the CI automatically moves to the Published state.

</td></tr><tr><td>

To remove a scheduled maintenance from the robot calendar.

</td><td>

Select an SM event card and select **Reject**.

</td><td>

An MR is created with Rejected state.

</td></tr><tr><td>

To cancel a scheduled maintenance day on the robot calendar.

</td><td>

-   Select an accepted SM event card and select **Cancel Maintenance**.
-   In the **Cancel Maintenance Request?** confirmation dialog box, select **Cancel**.


</td><td>

If the MR is In Progress state, it is updated to complete state. If the MR is in Pending state, it is canceled, then the CI moves to Published state automatically.

</td></tr></tbody>
</table>7.  To view the maintenance request for tracking, select the maintenance request.

8.  To view the updates of the CI, perform the following steps:

    1.  Navigate to the CI \(robot or bot process\).

    2.  Open the record.

    3.  In the **Activity** and **Compose** fields, view the notifications of the source of the CI from where it is published or is in use.


**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

**Related topics**  


[View maintenance requests in RPA Hub](view-mr-rpa.md)

[Maintenance request form in RPA Hub](../reference/mr-form-rpa.md)


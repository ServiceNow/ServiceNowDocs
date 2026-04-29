---
title: View the process jobs of a bot process in RPA Hub
description: View a list of execution logs of a bot process in RPA Hub.Use the Process job form to view a list of the execution logs of a bot process.A process job represents the execution of a bot process on a robot.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Success, Failed, Canceled, Skipped, Abandoned, Running, RPA Hub]
breadcrumb: [Monitor, RPA Hub, Workflow Data Fabric]
---

# View the process jobs of a bot process in RPA Hub

View a list of execution logs of a bot process in RPA Hub.

## Before you begin

Create a bot process. For more information, see [Configuring a bot process record in RPA Hub](../concept/create-botprocess.md).

Role required: sn\_rpa\_fdn.rpa\_release\_manager, sn\_rpa\_fdn.rpa\_support\_user, sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_business\_user, or sn\_rpa\_fdn.rpa\_admin

## About this task

A process job represents the execution of a bot process on a robot.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Build**, select **Bot Process**.

4.  Open a bot process to view the related process jobs.

5.  On the **Process Jobs** tab, select the process job that you want to view.

    For more information, see [Process job states in RPA Hub](view-process-jobs-botprocess.md#).

6.  Open a process job record to view an associated automation log.

7.  In the Automation Logs tab, view the details.


**Parent Topic:**[Monitoring automations](../concept/monitoring-automations-rpa.md)

## Process job form in RPA Hub

Use the Process job form to view a list of the execution logs of a bot process.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the process job.

</td></tr><tr><td>

Process

</td><td>

Name of the associated bot process.

</td></tr><tr><td>

Robot

</td><td>

Assigned robot that is running on the bot process.

</td></tr><tr><td>

State

</td><td>

State of the process job:-   Success
-   Failed
-   Running
-   Skipped
-   Canceled
-   Abandoned

For more information about process job states and their scenarios, see [Process job states in RPA Hub](view-process-jobs-botprocess.md#).

</td></tr><tr><td>

Storage

</td><td>

Storage location of the logs:-   **Instance**
-   **Robot Machine**

</td></tr><tr><td>

Triggered By

</td><td>

Source of the trigger.-   **Schedule**- If the automation is triggered via a schedule.
-   **API**- If the automation is triggered by a flow
-   **Manual**- If the attended automation is triggered by a user or if the unattended automation is triggered by **Start Process**.
-   **Embedded Task Automation**- If the attended automation is triggered from the ServiceNow form.

For more information, see [Embedded Task Automation \(ETA\) in RPA Hub](../concept/embedded-task-auto-rpa.md).


</td></tr><tr><td>

Execution Log Status

</td><td>

Status on the availability of the execution logs:-   **No Logs**
-   **Sync in progress**
-   **Complete**

 The available logs are viewed on the RPA Desktop Design Studio.

</td></tr><tr><td>

Graceful Stop

</td><td>

Indicates whether the Graceful Stop is executed or not.If it is marked true, the associated bot process is stopped gracefully instead of stopping abruptly.

</td></tr><tr><td>

Started At

</td><td>

Start date and time of the process job.

</td></tr><tr><td>

Completed At

</td><td>

End date and time of the process job.

</td></tr><tr><td>

Duration

</td><td>

Time taken to complete the automation.

</td></tr><tr><td>

Message

</td><td>

Any information or error message returned by the robot.

</td></tr></tbody>
</table>**Related topics**  


[View the process jobs of a bot process in RPA Hub](view-process-jobs-botprocess.md#)

[View process jobs for all bot processes in RPA Hub](view-process-jobs.md)

## Process job states in RPA Hub

A process job represents the execution of a bot process on a robot.

<table id="table_olx_3hf_xcc"><thead><tr><th>

State

</th><th>

Scenario

</th></tr></thead><tbody><tr><td>

Running

</td><td>

When a bot process is being executed by a robot, the status of the process job is updated to **Running**.

</td></tr><tr><td>

Canceled

</td><td>

When a bot process execution is canceled manually, the process job status is updated to **Canceled**.If Bot process 1 is already executing, and Bot process 2 with force start enabled is triggered, then the process job status of Bot process 1 is updated to **Canceled**, and the process job status of Bot process 2 is updated to **Running**.

</td></tr><tr><td>

Success

</td><td>

After a bot process is executed successfully by a robot, the process job status is updated to **Success**.

</td></tr><tr><td>

Failed

</td><td>

When a bot process execution fails to complete, the process job status is updated to **Failed**.

</td></tr><tr><td>

Skipped

</td><td>

Consider the following scenarios when more than one bot processes are triggered for the same unattended robot:-   If Bot process 1 is already executing and Bot process 2 with force start disabled is triggered, then the process job status of Bot process 2 is updated to **Skipped**.
-   If two bot processes, BP1 and BP2, are scheduled to run on the same robot at the same time and BP2 has lower priority \(higher priority order number\), then the process job status of BP2 is updated to **Skipped**.
-   If two bot processes, BP1 and BP2, with the same priority order are scheduled to run on the same robot at the same time, then only one of the bot process would be selected randomly for running and the process job status of the other one is updated to **Skipped**.
-   If Bot process 1 is triggered and robot is waiting to login, and in the mean time Bot process 2 is triggered, then process job status of Bot process 2 is updated to **Skipped**.
-   The **Start process** action is invoked for Bot process 1. Until the execution starts, if other bot processes are triggered then the process jobs of all other start process requests are updated to **Skipped**.
-   When a robot comes back to responsive state, it will start to receive start process requests that were triggered when the robot was in the unresponsive state. The latest request which falls under the configured threshold is updated to **Running** and all the older requests are updated to **Skipped**.

</td></tr><tr><td>

Abandoned

</td><td>

-   For any robot type, if a bot process was previously executing and the process job status was not updated to **Completed**, and a new process job is created, then the status of the previously executing process job is updated to **Abandoned**.
-   When a process job is running, the robot state is moved from **Busy** state to any other state.

For example, when a process job is executing locally in the robot machine, a robot may fail to update RPA Hub with its heartbeat call due to network failure, certificate authentication failure, machine user profile corruption, and so on.

In all such scenarios, when the robot calls the RPA Hub after an interruption, and then updates its status from **Busy** or **Disconnected** to **Available**, then the status of the last known process job is changed to **Abandoned**.


</td></tr></tbody>
</table>
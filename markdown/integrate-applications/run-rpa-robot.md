---
title: Run an automation using Unattended Robot
description: Run an unattended robot to execute the unattended automations that are triggered either by a schedule, API, or manually.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use, Unattended Robot, Workflow Data Fabric]
---

# Run an automation using Unattended Robot

Run an unattended robot to execute the unattended automations that are triggered either by a schedule, API, or manually.

## Before you begin

Create a package. For more information, see [Create a package to assign to a bot process](../../rpa-hub/task/create-package.md#).

Create a robot. For more information, see [Robots in RPA Hub](../../rpa-hub/concept/robots-rpa-hub.md).

Create a bot process. Select the **Process Type** field as **Unattended** on the Bot process form, while you’re creating a bot process. For more information, see [Configuring a bot process record in RPA Hub](../../rpa-hub/concept/create-botprocess.md) and [Bot Process form in RPA Hub](../../rpa-hub/task/select-botprocess.md#).

Ensure that the following conditions are met to execute a robot:

-   The life cycle stage status of the associated bot process must be **Published**.
-   The life cycle stage status of the executing robot must be **In-Use**.

\(Optional\) To run your bot process on regular intervals, create a schedule within a bot process. For more information, see [Create a schedule within a bot process in RPA Hub](../../rpa-hub/task/create-schedule-botprocess.md).

Create a credential group and assign it to a bot process. For more information, see [Create a credential group in RPA Hub](../../rpa-hub/task/create-credential-group.md#) and [Associate a credential group to a bot process in RPA Hub](../../rpa-hub/task/map-credential-groups-to-bot-process.md).

Assign a robot to a bot process. For more information, see [Assign a robot to a bot process in RPA Hub](../../rpa-hub/task/assign-robots.md).

Assign a process robot credential within a bot process. For more information, see [Assign a process robot credential within a bot process in RPA Hub](../../rpa-hub/task/assign-process-robot-cred-botprocess.md).

Ensure that the licenses are available. For more information, see [Robot license distribution in RPA Hub](../../rpa-hub/concept/license-rpa-hub.md).

Establish a connection between a robot and ServiceNow RPA Hub instance. For more information, see [Set up Unattended Robot](set-up-rpa-runtime.md).

\(Optional\) Create a process parameter within a bot process. For more information, see [Create a process parameter within a bot process in RPA Hub](../../rpa-hub/task/create-process-parameter-botprocess.md#).

Role required: sn\_rpa\_fdn.rpa\_robot and snc\_internal

**Note:** If the Attended Robot tries to connect to an Federal Information Processing Standards \(FIPS\)-enabled instance, the robot user must have the `snc_internal` role.

## About this task

You can also start an unattended bot process manually from the RPA Hub. For more information, see [Start an unattended bot process in RPA Hub](../../rpa-hub/task/start-bot-process.md).

In this task, you can run an unattended robot in two ways.

## Procedure

1.  To run an unattended robot, do any one of the following actions.

<table id="choicetable_ag1_lyx_jrb"><thead><tr><th align="left" id="d226965e264">

Option

</th><th align="left" id="d226965e267">

Action

</th></tr></thead><tbody><tr><td id="d226965e273">

**Based on the schedule you define in the bot process**

</td><td>

1.  Connect with a robot to execute the bot process. For more information, see [Set up Unattended Robot](set-up-rpa-runtime.md).
2.  Review the schedule within a bot process. For more information, see [Create a schedule within a bot process in RPA Hub](../../rpa-hub/task/create-schedule-botprocess.md).

The Unattended Robot runs the execution based on the schedule defined.

 For more information about the scheduled and manual triggers, see [Execution priority of bot processes in RPA Hub](../../rpa-hub/concept/bot-process-prioritization-order-rpa-hub.md).

</td></tr><tr><td id="d226965e332">

**Based on the API via Start Process subflow**

</td><td>

Review the Start Process subflow in Workflow Studio. For more information, see [Workflow Studio actions and subflow in RPA Hub](../../rpa-hub/reference/rpa-hub-actions.md).The Unattended Robot runs the execution based on the subflow that triggers the Start Process in Workflow Studio.

</td></tr></tbody>
</table>    **Important:** A process job record gets created as soon as the unattended robot starts initiating the bot process in the robot machine. The **Message** field is updated during the different stages of the process that provides insight and visibility regarding the status of your bot process. For more information on the different fields of a process job record, see [Process job form in RPA Hub](../../rpa-hub/task/view-process-jobs-botprocess.md#).


**Parent Topic:**[Using Unattended Robot](../concept/using-rpa-runtime.md)

**Related topics**  


[Open Service and Runtime logs](../../rpa-studio/task/open-logs-rpa-studio.md)


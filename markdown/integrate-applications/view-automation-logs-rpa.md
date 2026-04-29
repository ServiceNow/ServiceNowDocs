---
title: View automation logs in RPA Hub
description: Automation logs are series of succession stages or a series of checkpoints that occur during the execution of a bot process. It enables monitoring and auditing the automation process. These logs are generated from the robot for unattended and attended bot processes.Use the Automation Logs form to view a list of the automation logs captured for a bot process.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Monitor, RPA Hub, Workflow Data Fabric]
---

# View automation logs in RPA Hub

Automation logs are series of succession stages or a series of checkpoints that occur during the execution of a bot process. It enables monitoring and auditing the automation process. These logs are generated from the robot for unattended and attended bot processes.

## Before you begin

Ensure that the **Track Automation Logs** check box on the Bot Process form is enabled. For more information, see [Bot Process form in RPA Hub](select-botprocess.md#).

Ensure to use the log component in the associated automation and populate the required details in RPA Desktop Design Studio. For more information about the component, see [Use the Log component](../../rpa-studio/task/use-general-log.md).

Role required: sn\_rpa\_fdn.rpa\_business\_user, sn\_rpa\_fdn.rpa\_support\_user, sn\_rpa\_fdn.rpa\_developer, sn\_rpa\_fdn.rpa\_release\_manager, or sn\_rpa\_fdn.rpa\_admin

## About this task

Automation logs help in tracking the execution state of robots ensuring that automation processes run smoothly. The detailed logs show each step completed by the robot and any errors encountered. Reports are generated in real-time.

For example, when a robot executes an Invoice Processing bot process, view the following messages in the **Message** field of an automation log:

-   Bot started the invoice processing automation.
-   Emails retrieved successfully.
-   Invoice data extraction in progress.
-   Invoice categorization initiated.
-   Update to accounting system in progress.
-   Invoice processed successfully.

The automation logs store up to 8,000 records that are latest. Every 5 minutes, older records beyond this limit are automatically deleted.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  Navigate to the automation logs in one of the following ways.

<table id="choicetable_kgc_jxm_frb"><thead><tr><th align="left" id="d234571e159">

Option

</th><th align="left" id="d234571e162">

Action

</th></tr></thead><tbody><tr><td id="d234571e168">

**From Bot Process menu**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Bot Process**.
2.  Select a bot process.
3.  On the Process Jobs tab, open a process job record.
4.  On the Automation Logs tab, view an associated automation log.


</td></tr><tr><td id="d234571e201">

**From Process Job menu**

</td><td>

1.  On the **Lists** tab, under **Monitor**, select **Process Jobs**.
2.  Open a process job record.
3.  On the Automation Logs tab, view an associated automation log.


</td></tr><tr><td id="d234571e231">

**From Automation Logs menu**

</td><td>

1.  On the **Lists** tab, under **Monitor**, select **Automation Logs**.
2.  Open an automation log to view more details.


</td></tr></tbody>
</table>
**Parent Topic:**[Monitoring automations](../concept/monitoring-automations-rpa.md)

## Automation Logs form in RPA Hub

Use the Automation Logs form to view a list of the automation logs captured for a bot process.

### Automation logs overview

Automation logs help in tracking the execution state of robots ensuring that automation processes run smoothly. The detailed logs show each step completed by the robot and any errors encountered. Reports are generated in real-time.

<table id="table_fvm_wyz_czb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Log Level

</td><td>

Type of log level:-   Error
-   Exception
-   Info
-   Warning

</td></tr><tr><td>

Sequence Number

</td><td>

Auto generated number as per the order of the automation log record, created during the current process job execution across all process jobs.For example, an automation log created for process job PJ1 is 1 and the automation log created for process job PJ2 is 2.

</td></tr><tr><td>

Message

</td><td>

Message from the automation logs.

</td></tr><tr><td>

Created

</td><td>

Date and time at which the automation log record is created in RPA Hub.

</td></tr><tr><td>

Process Job

</td><td>

Associated Process Job number.

</td></tr></tbody>
</table>
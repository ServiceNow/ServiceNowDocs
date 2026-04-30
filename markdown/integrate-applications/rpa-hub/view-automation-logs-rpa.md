---
title: View automation logs in RPA Hub
description: Automation logs is series of succession stages or a series of checkpoints that occur during the execution of a bot process. It enables monitoring and auditing the automation process. These logs are generated from the robot for unattended and attended bot processes.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# View automation logs in RPA Hub

Automation logs is series of succession stages or a series of checkpoints that occur during the execution of a bot process. It enables monitoring and auditing the automation process. These logs are generated from the robot for unattended and attended bot processes.

## Before you begin

Ensure that the **Track Automation Logs** check box on the Bot Process form is enabled. For more information, see [Bot Process form in RPA Hub](../reference/bot-process-form.md).

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

<table id="choicetable_kgc_jxm_frb"><thead><tr><th align="left" id="d218530e149">

Option

</th><th align="left" id="d218530e152">

Action

</th></tr></thead><tbody><tr><td id="d218530e158">

**From Bot Process menu**

</td><td>

1.  On the **Lists** tab, under **Build**, select **Bot Process**.
2.  Select a bot process.
3.  On the Process Jobs tab, open a process job record.
4.  On the Automation Logs tab, view an associated automation log.


</td></tr><tr><td id="d218530e191">

**From Process Job menu**

</td><td>

1.  On the **Lists** tab, under **Monitor**, select **Process Jobs**.
2.  Open a process job record.
3.  On the Automation Logs tab, view an associated automation log.


</td></tr><tr><td id="d218530e221">

**From Automation Logs menu**

</td><td>

1.  On the **Lists** tab, under **Monitor**, select **Automation Logs**.
2.  Open an automation log to view more details.


</td></tr></tbody>
</table>
**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

**Related topics**  


[Automation Logs form in RPA Hub](../reference/automation-logs-form-rpa.md)


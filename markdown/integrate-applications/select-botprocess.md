---
title: Associate a bot process to a bot process configuration record
description: Select a bot process configuration record to associate it with a bot process. This action creates a bot process record in RPA Hub.Use the Bot Process form to associate it to the bot process configuration and populate the remaining fields required for a bot process.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 18
keywords: [associate bot process to bot process configuration record, rpa Hub, assign bot process to bot process configuration record, bot process settings, attended bot process, unattended bot process, bot process rpa hub, bot process configuration rpa hub]
breadcrumb: [Configuring a bot process record, Use, RPA Hub, Workflow Data Fabric]
---

# Associate a bot process to a bot process configuration record

Select a bot process configuration record to associate it with a bot process. This action creates a bot process record in RPA Hub.

## Before you begin

Create a package. For more information, see [Create a package to assign to a bot process](create-package.md#).

Create a robot. For more information, see [Robots in RPA Hub](../concept/robots-rpa-hub.md).

Configure the related system property to view the activity stream. For more information, see [Display an activity stream for bot processes and robots in RPA Hub](display-activity-stream-sys-property-rpahub.md).

Before you can access a bot process, ensure that the RPA business user \(sn\_rpa\_fdn.rpa\_business\_user\), RPA developer \(sn\_rpa\_fdn.rpa\_developer\), or the RPA support user \(sn\_rpa\_fdn.rpa\_support\_user\) are in the Managed by Group list.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

A bot process is a predefined sequence of actions that a robot follows to accomplish a specific task or achieve a particular goal.

A bot process configuration record contains the bot process settings. The bot process configuration record is mapped to a bot process record. It is a one to one mapping. You can only select one bot process record to associate with a bot process configuration record. You can't edit a bot process configuration record that is associated with a bot process.

When you retire a bot process record, you can't associate the related bot process configuration record to other bot processes.

You can create a bot process configuration record in two ways. The first way is when you create and save a bot process configuration record.

The second way is when you move an update set from a lower environment to a higher environment, an orphan bot process configuration record is created. After you select the **Assign Configuration** button and its record, the bot process record that is associated to the bot process configuration is created.

For more information about migrating your metadata from a lower environment to a higher environment, see [Migrating your data from a lower environment to a higher environment in RPA Hub](../concept/migrate-data-rpa-hub.md).

## Procedure

1.  You can associate a bot process to a bot process configuration record by choosing one of these options.

<table id="choicetable_nkf_c3k_xvb"><thead><tr><th align="left" id="d607662e162">

Option

</th><th align="left" id="d607662e165">

Action

</th></tr></thead><tbody><tr><td id="d607662e171">

**Perform this task in workspace**

</td><td>

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.
2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).
3.  On the **Lists** tab, under **Build**, select **Bot Process**.
4.  In the form header, select the down arrow in the **Create Configuration** button.

![Down arrow in the Create Configuration button.](../image/down-arrow-create-config-rpa.png "Down arrow in the Create Configuration button")

5.  Select **Assign Configuration**.
6.  Select a bot process configuration record to associate it with a bot process.
7.  Select **Submit**.
8.  On the form, fill in the fields.

For a description of the field values, see [Bot Process form in RPA Hub](select-botprocess.md#).

9.  Select **Save**.
10. On the **Details** tab, in **Activity** and **Compose** fields, view the activity of the form, work notes, and additional comments.


</td></tr><tr><td id="d607662e282">

**Perform this task in the classic environment**

</td><td>

1.  Switch to the classic environment.
2.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **Build** &gt; **Bot Process**.
3.  In the form header, select **New**.
4.  Select a bot process configuration record to associate it with a bot process.
5.  Select **Submit**.
6.  On the form, fill in the fields.

For a description of the field values, see [Bot Process form in RPA Hub](select-botprocess.md#).

7.  Select **Save**.


</td></tr></tbody>
</table>
## What to do next

You can add other details that pertain to the bot process, such as the business applications, credential groups, robots, process robot credential sets, schedules, process parameters, attended users, or groups. For more information, see [Adding details to your bot process in RPA Hub](../concept/post-req-bot-process-rpa.md).

**Parent Topic:**[Configuring a bot process record in RPA Hub](../concept/create-botprocess.md)

**Related topics**  


[Create a bot process configuration record in RPA Hub](create-botprocess-config.md#)

[Bot process configuration form in RPA Hub](create-botprocess-config.md#)

[Edit a bot process in RPA Hub](edit-botprocess.md)

[Publish a bot process in RPA Hub](publish-bot-process.md)

[Retire a bot process in RPA Hub](retire-bot-process.md)

[View Audit History](https://www.servicenow.com/docs/access?context=c_HistorySets&version=australia&pubname=australia-platform-security&ft:locale=en-US)

## Bot Process form in RPA Hub

Use the Bot Process form to associate it to the bot process configuration and populate the remaining fields required for a bot process.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Bot Process

</td></tr><tr><td>

Name

</td><td>

Unique name of the bot process.

</td></tr><tr><td>

Process Type

</td><td>

Type of the bot process:-   **Unattended**: Automations that don’t require any human intervention.
-   **Attended**: Automations that require human intervention.

</td></tr><tr><td>

Bot Process Configuration

</td><td>

\[Auto-generated\] Associated bot process configuration of the bot process.

</td></tr><tr><td>

Order

</td><td>

Priority order of execution for the bot process. -   **1**: Highest priority
-   **999999**: Least priority

If more than one unattended bot process is scheduled to start at the same time, the one with the highest priority runs, and the others are marked as **Skipped**.

If multiple bot processes have the same priority and schedule, one bot process is chosen at random to run.For more information, see [Execution priority of bot processes in RPA Hub](../concept/bot-process-prioritization-order-rpa-hub.md).

The default value is set to `1`.

RPA business user can view this field.

This field appears only when **Unattended** is selected from the **Process Type** field.

</td></tr><tr><td>

Package

</td><td>

Associated package of the bot process.For an unattended bot process, associate an unattended type package.

For an attended bot process, associate an attended type package.

Only published packages can be associated.

</td></tr><tr><td>

Package Version

</td><td>

Version of the active package in use. Only published package versions can be associated.

</td></tr><tr><td>

Life Cycle Stage Status

</td><td>

\[Auto-generated\] Life cycle stage status of bot process configuration.

</td></tr><tr><td>

Run Time Threshold \(mins\)

</td><td>

Expected duration for the bot process to run.The default value is 60 minutes.

This field appears only when **Unattended** is selected from the **Process Type** field.

RPA business user can view this field.

This field is required.

</td></tr><tr><td>

Job Purging \(days\)

</td><td>

Number of days after which the job data is deleted.

</td></tr><tr><td>

Managed by

</td><td>

IT owner of the business process.This field appears only for an existing record.

Roles required to edit this field: RPA release manager and RPA admin.

</td></tr><tr><td>

Owned by

</td><td>

Business user who is part of the managed by a group and is responsible for the business process.This field appears only for an existing record.

This field depends on what you entered in the **Managed By Group** field.

If an entry in the **Managed By Group** field is populated, then only those users who are a part of the **Managed By Group** field and have an RPA business user role can be added to the **Owned By** field.

If the **Managed by Group** field is empty, then the **Owned By** field is read-only.

Roles required to edit this field: RPA release manager and RPA admin.

</td></tr><tr><td>

Enable Embedded Task Automation

</td><td>

Option to trigger the attended bot process \(automation\) from the associated ServiceNow form that is mapped in the attended configuration record. For more information about the attended configuration record, see [Attended Configuration form in RPA Hub](../reference/attended-config-form-rpa.md).On enabling the **Embedded Task Automation** check box, two additional tabs, **Process Field Parameters** and **Attended Configuration**, are displayed on the bot process form.

For more information about Embedded Task Automation, see [Embedded Task Automation \(ETA\) in RPA Hub](../concept/embedded-task-auto-rpa.md).

</td></tr><tr><td>

Description

</td><td>

Description of the bot process.

</td></tr><tr><td class="sub-head" colspan="2">

Session Settings

</td></tr><tr><td>

Keep Monitor Active

</td><td>

Option to keep the monitor active of the machine where the robot is running the bot process.This field appears only when **Unattended** is selected from the **Process Type** field.

</td></tr><tr><td>

Auto Session Restore

</td><td>

Option to restore the state of the robot to the initial stage before the automation is executed.This field appears only when **Unattended** is selected from the **Process Type** field.

</td></tr><tr><td>

Force Start

</td><td>

Option to force start a bot process on a robot to override any other bot process already running on it.

 If the **Force Start** option is enabled for a bot process P1 and if bot process P2 is running on the same robot, P2 stops and P1 executes. Then, the process job of P2 moves to **Canceled** state.

 The **Force Start** option does not override the **Order** field. The **Force Start** option is applicable for the existing running bot processes and is not applicable for the bot processes that are yet to be launched.

 This field appears only when **Unattended** is selected from the **Process Type** field.

</td></tr><tr><td>

Enable Desktop In Desktop

</td><td>

Option to enable attended automation to run in Desktop In Desktop window. This option creates a new session on the same machine and the automation can be executed on this session without interrupting actual manual work on the main session.On enabling this option, the **End Desktop In Desktop on Complete** check box is also selected.

This field appears only when **Attended** is selected from the **Process Type** field.

</td></tr><tr><td>

End Desktop In Desktop on Complete

</td><td>

Option to close the Desktop In Desktop window after the bot process execution is completed.

 This option is automatically selected when you select **Enable Desktop In Desktop**. To leave the Desktop In Desktop window open after the bot process completes, clear the check box.

 This field appears only when **Attended** is selected from the **Process Type** field.

</td></tr><tr><td>

Screen Resolution

</td><td>

Screen resolution for the Desktop In Desktop window.This field appears only when **Attended** is selected from the **Process Type** field.

</td></tr><tr><td class="sub-head" colspan="2">

Log Settings

</td></tr><tr><td>

Track Execution Logs

</td><td>

Option to enable the tracking of process execution logs.After you enable this check box, the logs are captured when an automation is executed by either an attended or an unattended robot. These logs help in understanding the errors and the end-to-end logging of automation execution.

If process jobs are purged, then the corresponding execution logs are purged.

By using the Attach feature in RPA Desktop Design Studio, these execution logs can be used to replay the automation to understand where the automation has failed. For example, at which component the automation has failed or details of the inputs passed to that component.

**Note:** The **Attach** feature doesn't support Flat file output type.

</td></tr><tr><td>

Synchronize Execution Logs \(seconds\)

</td><td>

Frequency, in seconds, for execution logs to synchronize.This field appears only when the **Track Execution Logs** option is selected.

If you select **Robot Machine** in the **Storage** field, then this field is hidden.

</td></tr><tr><td>

Storage

</td><td>

**Note:** This field appears only when the **Track Execution Logs** option is selected.

 Storage location options for the execution logs:

-   **Instance**: Only error information is logged in the execution log, on the instance.

If you select **Instance**, then the value for the **Log Level** field is set to Error and it can't be edited.

-   **Robot Machine**: The log files are stored in the robot machine where the automation is executed.

If you select **Robot Machine**, then you can view two options to select from the **Log Level** field - **Error** or **Verbose**.

To view the end-to-end execution logs of all the components, select **Robot Machine** from the **Storage** field and then select **Verbose** from the **Log Level** field.

For optimum utilization of disk space in the robot machine, the existing logs are purged, based on the **sn\_rpa\_fdn.purge\_client\_logs** system property setting.


 If you select **Robot Machine**, then

-   **Synchronize Execution Logs** field is hidden.
-   The execution logs are stored in the machine on which the attended or unattended robot is installed.

</td></tr><tr><td>

Output Type

</td><td>

Output type of the execution log file. This log file is generated during the robot execution on the machine. There are two types of output:-   **DB File**: Default value. It's a lite database file that stores the process job metadata and the process automation execution details. After the process job completion, you can attach the DB file using the **Attach** option in the RPA Desktop Design Studio project to replay the automation on the design surface.
-   **Flat File**: It's a file format that stores the process job metadata and the process automation execution details in plain text. It stores the execution data in a JSON format.

This **Output Type** field appears when the **Track Execution Logs** option is selected and when the **Robot Machine** is selected from the **Storage** field.

If a bot process, with Flat File as the Output Type, is triggered, then the execution log file is added to the process job folder in .txt format in the given locations. Similarly, for DB output type you will view .db format in the given locations.

The location of both the flat files and the DB files is in the machine on which the attended or unattended robot is installed.

-   During execution: `Users\<Userprofile>\ServiceNow RPA Logs\.executionlogs\{InstanceName}\{ProcessJob number}`.

For example, `Users\john.smith\ServiceNow RPA Logs\.executionlogs\{InstanceName}\PJB0001165`.

-   After execution is complete: `Users\<Userprofile>\ServiceNow RPA Logs\.executionlogs\{InstanceName}\.archive\{ProcessJob number}`.

For example: `Users\john.smith\ServiceNow RPA Logs\.executionlogs\{InstanceName}\.archive\PJB0001165`.


The content in the flat files is in JSON format. The following image gives the content structure.

When you choose the **Flat File** option to store the execution logs, two flat files are generated and stored in the locations given.

-   `ExecutionJobMetadata.txt`: Contains information on the process job such as the Process ID, Robot ID, and the log level. The image shows the structure of the content in the file.

![Execution metadata.](../../rpa-studio/image/execution-metadata.png "Structure of content in Flat File")

-   File name in the format `ddMMMyyyy HHmmss.txt` \(For example, `28Dec2023 125036.txt`\): Contains the execution log entries. For example, the file gives the name of the Activity, component execution start and end time, duration, and the result in boolean, if applicable.

The flat files follow the rules on data purging set in the **sn\_rpa\_fdn.purge\_client\_logs** system property. For more information about the system property, see [Configure RPA Hub properties](../reference/rpahub-sys-properties.md).

**Important:** In RPA Desktop Design Studio, if you mark one or more input or output ports of one or more components or methods in an automation as **Mark Data as Sensitive**, the flat file does not log the execution data of its corresponding process job. Instead, in the JSON file the data corresponding to the port appears as **SENSITIVE**. The following image gives an example.

![Port indicated as sensitive.](../../rpa-studio/image/flat-file-sensitive.png "Port indicated as sensitive")

For more information about marking an input or output port as **Mark Data as Sensitive**, see [Configure port properties](../../rpa-studio/task/configure-input-port-properties.md)

Since the actual data for the execution logs contain abundant data, the required data is only preserved. The content in text file is JSON type.​

To modify the value of this field for an existing bot process, ensure that the associated bot process is **In Maintenance** state.

</td></tr><tr><td>

Log Level

</td><td>

Select a log level to capture:-   **Error**-

Only error information is stored during automation execution.

-   **Verbose**-

Error information and end-to-end component execution logs, such as inputs and outputs and execution steps with timestamps are stored during automation execution. When you select **Verbose**, the flat files record details of the execution of all components in the automation. If the size of the flat file exceeds 10 MB while the process job executes, the flat file continues to split into multiple flat files with the log sequence appended in the file-naming convention until it executes the complete automation. The naming conventions of such files are `<timestamp>_<LogSequence>`.

This option appears only when Robot machine is selected as storage type.


This field appears only when the **Track Execution Logs** option is selected.

</td></tr><tr><td>

Track Automation Logs

</td><td>

Track automation logs that are generated by the robot. The robot logs the automation execution in automation logs. The logs help the RPA users to track the automation progress.For more information about viewing the automation logs, see [View automation logs in RPA Hub](view-automation-logs-rpa.md#).

To view automation logs of a bot process, in RPA Desktop Design Studio, use the Log component in the associated automation and populate the required details.

For more information about the Log component, see [Use the Log component](../../rpa-studio/task/use-general-log.md).

</td></tr><tr><td class="sub-head" colspan="2">

Access

</td></tr><tr><td>

Managed by Group

</td><td>

Group that can access the bot process.

</td></tr><tr><td class="sub-head" colspan="2">

Robot PoolRoles required to edit this field: RPA release manager and RPA admin.

If an RPA developer and RPA support user are a part of the Managed by Group, then they can view and edit these fields.

RPA business user can view these fields.

</td></tr><tr><td>

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

</td></tr><tr><td class="sub-head" colspan="2">

Compose

</td></tr><tr><td>

Work notes \(Private\)

</td><td>

Work notes for the bot process.View the changes executed on the associated package, package version, process parameter, shared parameter, queue, and schedule.

</td></tr><tr><td>

Additional Comments

</td><td>

Additional comments that are related to the bot process.

</td></tr></tbody>
</table>**Related topics**  


[Create a bot process configuration record in RPA Hub](create-botprocess-config.md#)

[Configuring a bot process record in RPA Hub](../concept/create-botprocess.md)


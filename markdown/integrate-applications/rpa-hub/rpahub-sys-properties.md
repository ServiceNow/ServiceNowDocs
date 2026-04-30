---
title: Configure RPA Hub properties
description: You can access system properties for RPA Hub by navigating to All Robotic Process Automation Administration Properties .
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 13
breadcrumb: [Configuring RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Configure RPA Hub properties

You can access system properties for RPA Hub by navigating to **All** &gt; **Robotic Process Automation** &gt; **Administration** &gt; **Properties**.

<table id="table_fd2_bdj_lsb"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Role required \(to edit\)

</th></tr></thead><tbody><tr><td>

Enable auto assignment of Attended Robot.sn\_rpa\_fdn.allow\_rda\_robot\_auto\_assignment

</td><td>

Auto assigns robot licenses to users from the bot process, on a first come first serve basis.-   Type: Yes \| No
-   Default value: No

For more information, see [Run an automation using Attended Robot](../../rda-runtime/task/run-rda-robot.md).

</td><td>

admin, sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Sets the instance and robot machine authentication mechanism.sn\_rpa\_fdn.instance\_authentication

</td><td>

Select an authentication type:-   **mTLS**: Mutual Transport Layer Security. As a prerequisite, install the user certificate.

For more information about installing a user certificate, if you have the admin role, see [Install the user-generated certificates](../../rpa-core/concept/use-user-certificates-rpa.md#).

-   **Basic**: Authentication happens based on user name and password.

</td><td>

admin, sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Enable auto session restore.sn\_rpa\_fdn.process.auto\_session\_restore

</td><td>

Restores auto session.-   Type: Yes \| No
-   Default value: No

If it is set to Yes, then the **Auto Session Restore** check box on a new bot process form is selected by default. There is no impact to the existing bot processes, when this system property value is changed.

For more information about the bot process form, see [Bot Process form in RPA Hub](bot-process-form.md).

If enabled, when the unattended robots log in or unlock the machine to start the automation, then the machine session is restored to the original state \(log off or locked\) after the automation is completed.

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Enable the code quality check at the instance level.sn\_rpa\_fdn.enable\_code\_quality\_check

</td><td>

Enables the code quality check at the instance level.-   Type: Yes \| No
-   Default value: Yes

If it is set to Yes, then the configure the **sn\_rpa\_fdn.restrict\_package\_by\_severity** and **sn\_rpa\_fdn.code\_quality\_check\_timeout** system properties appropriately.

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Sets restriction on publishing package from RPA Desktop Design Studio and publishing bot process in RPA Hub, if the package contains any of the defined selection. This property is effective only when code quality check feature is enabled.sn\_rpa\_fdn.restrict\_package\_by\_severity

</td><td>

Sets a restriction on publishing package from RPA Desktop Design Studio and publishing bot process in RPA Hub. This property is effective only when code quality check feature is enabled.Select a restriction type:

-   **No restriction** - Enables packages to publish from RPA Desktop Design Studio regardless of the code quality result. The packages with error or warning can also be published from the RPA Desktop Design Studio. Enables the publishing of bot processes regardless of the code quality result of the associated package version.
-   **Error** - Restricts packages with Code Quality Result as 'Error' to publish from RPA Desktop Design Studio. Restricts publishing of bot process if it is using the package versions whose code quality check is marked as error.
-   **Error or Warning** - Restricts packages with Code Quality Result as 'Error' or 'Warning' to publish from RPA Desktop Design Studio. Restricts publishing of bot process if it is using the package versions whose code quality check is marked as 'Error' or 'Warning'.

Default value: **No restriction**

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Maximum duration, in minutes, for the completion of the code quality check. Ensure to enter a positive integer value. This property is effective only when code quality check feature is enabled.sn\_rpa\_fdn.code\_quality\_check\_timeout

</td><td>

Limit the processing time for code quality check. Enter a maximum duration, in minutes, for the completion of the code quality check. Ensure to enter a positive integer value. This property is effective only when code quality check feature is enabled.-   Type: integer
-   Default value: 5

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Enable this to ensure the security of the published packages via code signing, where the package is digitally verified.sn\_rpa\_fdn.code\_signing\_required

</td><td>

Ensures the security of the packages that are published from the RPA Desktop Design Studio.

 -   Type: Yes \| No
-   Default value: No

 It is validated by the Unattended Robot and Attended Robot.

</td><td>

admin

</td></tr><tr><td>

Mark this as true in order to enable manual upload of automation package.sn\_rpa\_fdn.allow\_manual\_upload\_of\_automation\_package

</td><td>

Enables RPA release managers to manually upload the automation package \(zip file\).-   Type: Yes \| No
-   Default value: No

This property helps in controlling direct upload of attachments in the existing package version record.

</td><td>

admin

</td></tr><tr><td>

Enable this to ignore certificate expiry while publishing digitally signed package/package version created with RPA Desktop Design Studio.

 sn\_rpa\_fdn.ignore\_certificate\_expiry\_date

</td><td>

Ensures that the package is published to the instance from RPA Desktop Design Studio even after the code signing certificate is expired.

 -   Type: Yes \| No
-   Default value: No

</td><td>

admin

</td></tr><tr><td>

Enable to reference unattended robot's machine name from CMDB tables.

 sn\_rpa\_fdn.enable\_unattended \_robot\_machine\_name\_lookup

</td><td>

Enables you to select one of the available machines in the CMDB table.-   Type: Yes \| No
-   Default value: No

 If you enable this property as Yes, then configure the **sn\_rpa\_fdn.machine\_name\_reference\_fields** system property appropriately.

**Note:** If you enable this system property and if there are any existing robot records, to use them, retire the robot and create a new record.

</td><td>

admin

</td></tr><tr><td>

Provide names of CI tables to reference unattended robot's machine name.

 sn\_rpa\_fdn.machine\_name\_reference\_fields

</td><td>

CI table names to reference the machine name of an unattended robot.-   Type: Comma separated list
-   Default value: `cmdb_ci_hardware`

</td><td>

admin

</td></tr><tr><td>

Frequency, in seconds, to sync the execution logs.sn\_rpa\_fdn.process.sync\_execution\_logs

</td><td>

Defines the frequency, in seconds, for execution logs to synchronize.-   Type: integer
-   Default value: 60

When a new bot process is created, the default value you define in this system property appears in the **Synchronize Execution Logs \(seconds\)** field. There is no impact to the existing bot processes, when this system property value is changed.

This system property is only applicable only for those bot processes where the **Track Execution Logs** check box is enabled. The logs are saved locally and are synced based on the interval set in this property.

For more information about the bot process form, see [Bot Process form in RPA Hub](bot-process-form.md).

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Maximum limit for frequency, in seconds, to sync the execution logs.sn\_rpa\_fdn.process.sync\_execution\_logs\_max\_value

</td><td>

Defines the maximum limit for frequency, in seconds, for execution logs to synchronize.

-   Type: integer
-   Default value: 300

 This system property is only applicable only for those bot processes where the **Track Execution Logs** check box is enabled and the value for the **Storage** field is **Instance**.

 For more information about the bot process form, see [Bot Process form in RPA Hub](bot-process-form.md).

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Enable tracking of execution logs.sn\_rpa\_fdn.process.track\_execution\_log

</td><td>

Tracks the execution logs.-   Type: Yes \| No
-   Default value: No

If it is set to Yes, then the **Track Execution Logs** check box on a new bot process form is selected by default. There is no impact to the existing bot processes, when this system property value is changed.

After you enable the **Track Execution Logs** check box on a bot process form, the logs are captured when an automation is executed by either an attended or an unattended robot. These logs help in understanding the errors and the end-to-end logging of automation execution.

For more information about execution logs, see [Bot Process form in RPA Hub](bot-process-form.md).

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Maximum days to retain process job.sn\_rpa\_fdn.max\_purge\_days\_process\_job

</td><td>

Defines the maximum days to retain a process job.-   Type: integer
-   Default value: 90

In a bot process record, process jobs are purged based on this system property.

Based on this system property, the maximum value for the **Job Purging \(days\)** field in a bot process is defined.

For more information about the bot process form, see [Bot Process form in RPA Hub](bot-process-form.md).

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Default value for the number of days to retain process job logs.sn\_rpa\_fdn.process.job\_purge\_days

</td><td>

Defines the number of days to retain job logs.-   Type: integer
-   Default value: 30

In a bot process record, process jobs are purged based on this system property.

When a new bot process is created, the default value you define in this system property appears in the **Job Purging \(days\)** field.

For more information about the bot process form, see [Bot Process form in RPA Hub](bot-process-form.md).

</td><td>

ServiceNow employee

</td></tr><tr><td>

Enable attended automation to run in desktop-in-desktop.sn\_rpa\_fdn.process.rda\_run\_in\_desktop\_in\_desktop

</td><td>

Ensures the attended automations to run in a Desktop In Desktop window.-   Type: Yes \| No
-   Default value: No

If it is set to Yes, then the **Enable Desktop In Desktop** check box on a new bot process form is selected by default.

If it is set to No, then the **Enable Desktop In Desktop** check box on a new bot process form is not selected by default.

For more information about the bot process form, see [Bot Process form in RPA Hub](bot-process-form.md).

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Enable the robot to force start.sn\_rpa\_fdn.process.force\_start

</td><td>

Forces the robot to start. -   Type: Yes \| No
-   Default value: No

If it is set to Yes, then the **Force Start** check box on a new bot process form is selected by default.

For more information about the bot process form, see [Bot Process form in RPA Hub](bot-process-form.md).

For example, a robot R1 is assigned to multiple bot processes BP1 and BP2, and R1 is currently executing BP1. Then, if BP2, whose **sn\_rpa\_fdn.process.force\_start** system property is set to Yes, is triggered forcefully and BP1 is terminated.

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Keep bot monitor active.sn\_rpa\_fdn.process.keep\_monitor\_active

</td><td>

Ensures that the bot monitor is active. -   Type: Yes \| No
-   Default value: Yes

This system property is set at the instance level. This property is not set at the automation level.

If it is set to Yes, then the **Keep Monitor Active** check box on a new bot process form is selected by default. Also the system is unlocked even after locking it.

If it is set to No, then the robot machine is locked \(based on idle time settings as per the organization\), when the automation doesn't have any foreground actions such as SendKeys or Mouse click.

For more information about the bot process form, see [Bot Process form in RPA Hub](bot-process-form.md).

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

List of screen resolutions in desktop-in-desktop.sn\_rpa\_fdn.process.rda\_screen\_resolution

</td><td>

Lists the screen resolutions in a Desktop In Desktop window.-   Type: string
-   Default value: 1920x1080

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Expected duration for the bot process to run.sn\_rpa\_fdn.process.runtime\_threshold

</td><td>

Defines the expected duration for the bot process to run.-   Type: integer
-   Default value: 60

If a value is defined here, then the same value appears in the **Run Time Threshold \(mins\)** field on a new bot process form.

For more information about the bot process form, see [Bot Process form in RPA Hub](bot-process-form.md).

The value in the **Runtime Threshold \(Mins\)** field on the bot process form and the configuration in this system property are used for plotting the event duration in the robot calendar.

For more information about the robot calendar, see [Using the robot calendar for RPA Hub](../concept/robot-calendar-rpa.md).

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Enable work item name to be unique.sn\_rpa\_fdn.queue.is\_queue\_item\_name\_unique

</td><td>

Ensures that the work item name is unique.-   Type: Yes \| No
-   Default value: Yes

If it is set to Yes, then the **Is Work Item Name Unique** check box on a new queue form is selected by default. There is no impact to the existing queue records.

For more information about the queue form, see [Queue form in RPA Hub](queue-form.md).

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Maximum value of max attempts field on work queues.sn\_rpa\_fdn.queue.maximum\_attempts\_max\_value

</td><td>

Defines the maximum value of the **Maximum Attempts** field in the Queue form.-   Type: integer
-   Default value: 99
-   Maximum value: 99

</td><td>

admin, sn\_rpa\_fdn.rpa\_release\_manager, or sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Sets the default number of days to retain work items.sn\_rpa\_fdn.queue.purge\_days

</td><td>

Defines the default value of the **Purge After \(days\)** fields in the Queue form.-   Type: integer
-   Default value: 30

</td><td>

ServiceNow employee

</td></tr><tr><td>

Maximum number of days to retain work items.sn\_rpa\_fdn.max\_purge\_days\_work\_queue\_item

</td><td>

Defines the maximum value of the **Purge After \(days\)** fields in the Queue form.-   Type: integer
-   Default value: 90

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Maximum duration after the last heart beat for robot to turn unresponsive. The value must be between 5 and 30 minutes.sn\_rpa\_fdn.robot.unresponsive

</td><td>

Defines the maximum duration after the last heartbeat for the robot to turn unresponsive. The value must be between 5 and 30 minutes.-   Type: integer
-   Default value: 5

If a robot is unresponsive, then the scheduled automations will not execute on that machine.

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Sets the default value of the order field in the bot process. 1 being the highest and 999999 the lowest.sn\_rpa\_fdn.process.order

</td><td>

Defines the default value of the **Order** field in the bot process.1 is the highest and 999999 is the lowest default value.

 -   Type: integer
-   Default value: 1

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Maximum days to retain alert triggers. The value must be between 1 and 30.sn\_rpa\_fdn.alert.trigger\_purge\_days

</td><td>

Defines the maximum days to retain alert triggers. The value must be from 1 through 30.-   Type: integer
-   Default value: 10

</td><td>

ServiceNow employee

</td></tr><tr><td>

Maximum days to retain alert notifications. The value must be between 1 and 60.sn\_rpa\_fdn.alert.purge\_days

</td><td>

Defines the maximum days to retain alert notifications. The value must be from 1 through 60.-   Type: integer
-   Default value: 30

</td><td>

ServiceNow employee

</td></tr><tr><td>

Maximum number of days to retain client logs. The value must be between 1 and 90.sn\_rpa\_fdn.purge\_client\_logs

</td><td>

Defines the limit for maximum days to retain client logs \(product and execution logs\). Based on this values, clients delete the files in robot machine. The value must be from 1 through 90.-   Type: integer
-   Default value: 7

 After 7 days, in this scenario, the logs are automatically purged from your local folder.

</td><td>

admin, sn\_rpa\_fdn.rpa\_admin

</td></tr><tr><td>

Set to fetch the robots in the **Assign bot process** section of the RPA Desktop Design Studio, whose machine name matches the one on which the Studio is running.sn\_rpa\_fdn.restrict\_robots\_in\_assign\_bot\_process\_by\_machine\_name

</td><td>

Restrict robots in **Assign bot process** section by machine name.-   Type: Yes \| No
-   Default value: No

If this value is set to Yes, then you can impersonate as robot from the RPA Desktop Design Studio on that specific robot machine, along with the users added in the Assigned Studio Users tab in the Robot form, if any.

If this value is set to No, then the users added in the Assigned Studio Users tab in the Robot form can impersonate as robot from the RPA Desktop Design Studio. For more information about adding the assigned studio users, see [Add assigned studio users to an unattended robot](../task/assigned-studio-users-rpa.md).

For more information about assign bot process to an automation project, see [Assign bot process to an automation project](../../rpa-studio/task/assign-bot-process.md).

</td><td>

sn\_rpa\_fdn.rpa\_admin

</td></tr></tbody>
</table>
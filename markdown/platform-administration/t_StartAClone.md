---
title: Request a clone
description: Request a clone to copy data from a production instance to a non-production instance or to copy data between non-production instances.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-03-25"
reading_time_minutes: 7
breadcrumb: [System clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Request a clone

Request a clone to copy data from a production instance to a non-production instance or to copy data between non-production instances.

## Before you begin

Role required: admin

## About this task

Clone Admin Console overview video 

The ServiceNow AI Platform uses data from the most recent, daily backup of the source instance when cloning. Backups that are used for cloning are a maximum of 36 hours old. System Clone begins the initial preparation, including selecting the latest backup to use, only at the date and time processing is scheduled to start.

If cloning from a source backup fails, the system uses the legacy clone engine instead. The legacy clone engine cannot preserve data from extended tables, relationships, hierarchies between tables, and dot-walked queries. You may want to restore the target instance from a backup and then reschedule the clone in such cases.

**Note:**

-   For instances that use an Oracle database, see [KB0538884 - System Clone Support for Oracle Customers](https://support.servicenow.com/kb_view.do?sysparm_article=KB0538884).

-   You can automate cloning by scheduling it in the Options pane.

-   You cannot initiate a clone request when the source instance is in debug mode. If the source instance is in debug mode, contact Customer Service and Support to turn off debug mode before you submit a clone request.


## Procedure

1.  Log in to the instance that you want to clone.

    This instance becomes the source instance of the clone request.

2.  [Clone Target Registration and Authentication](t_CreateACloneTarget.md) record for each target instance that you want to receive clone data.

3.  Verify the list of tables that are excluded from cloning and [add or remove tables to exclude](t_ExcludeATableFromCloning.md) from the target instance.

4.  Verify the list of tables and system properties that you want saved on the target instance with the following.

    You can use [data preservers](../concept/data-preservation.md#). You can also [create or modify data preservers](../concept/data-preservation.md#), as needed.

    The legacy clone engine does not support data preservers for these records:

    -   Tables that extend the Task table
    -   Relationships
    -   Hierarchies
    -   Dot-walked queries
    If you are preserving any data that the legacy clone engine does not support, verify that there is a recent backup of the target instance available. If the clone-from-backup-process fails for any reason, you can restore the target instance from the backup.

5.  [Preserve any unpublished applications](../concept/data-preservation.md#) on the target instance.

6.  Navigate to **System Clone** &gt; **Request Clone**.

7.  Specify a predefined clone profile.

    A clone profile stores target and clone options. The clone profile automatically populates your clone request with your selected profile settings. See [clone profiles for clone requests](../reference/system-profile-clone.md).

8.  In the **Target instance** field, select the target instance that you want to receive the cloned data.

    Create a separate clone request for each target instance that you want to receive clone data.

9.  In the **Clone Scheduled Start Time** field, select the time that you want the cloning to start.

    You can schedule multiple clone requests for the same source instance. For example, create one clone request to copy data to non-production instance A and another clone request to copy data to non-production instance B. The scheduling engine determines whether multiple clone requests against the same source instance can occur simultaneously or whether they must occur sequentially.

    The system verifies the scheduled start time and either accepts the date-time value that you selected or suggests an available date-time value. The validation process prevents scheduling conflicts with other automations using the same target instance.

10. In the **Email upon completion** field, enter your email address so that you can receive alerts after the cloning finishes, is canceled, or has an error.

11. Click the **Options** arrowhead so that it turns downward and use the following table to make appropriate selections in the Options pane.

<table id="table_ajq_bss_gr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Exclude tables specified in Exclusion List

</td><td>

Prevents cloning records from tables on the source instance which are listed under  **System Clone** &gt; **Exclude Tables**. If a table is on the Exclusion List, clone will exclude the records on the table as well as records on the child tables. When excluding tables, their table schema and hierarchy will still be cloned to your target instance. As a result, your target instance will have empty but usable tables after the clone.

**Note:** ServiceNow out-of-the-box table exclusions will still be excluded and are not affected by this setting. These include tables containing auditing, license usage, logging, and notifications.

You can choose to disable this setting if you need the data from your excluded tables. This is called a Full Clone and is recommended for upgrade or deployment testing.

The legacy clone engine does not support this option.

The default setting is that tables specified in the Exclusion List are excluded from a clone.

</td></tr><tr><td>

Exclude audit and log data

</td><td>

Prevents the cloning of audit and log records from the source instance. This creates empty but usable audit and log tables on the target instance. **Note:** If you exclude audit and log data from your clone, the Activity Stream for records won't match the source instance. This is because the Activity Stream relies on the audit table to generate the history.

The default setting is that audit and log data are excluded from a clone.

</td></tr><tr><td>

Exclude attachment data

</td><td>

Prevents the cloning of certain files like -   Video files
-   Image files
-   Other large binary files
from the sys\_attachment table. **Note:** ServiceNow out-of-the-box attachments and other system-relevant files \(e.g. catalog item images, theme images, and icons\) are not affected by this setting.

The following ServiceNow out-of-the-box attachments and other system-relevant files are not affected by this setting and are not excluded from a clone:-   Table name values that start with ZZ\_.
-   Table names: sys\_certificate, sc\_cat\_item,sys\_upgrade\_manifest, ecc\_agent\_jar, ecc\_agent\_mib, sys\_store\_app, or invisible.sys\_store\_app.
The default setting is to exclude attachment data.

</td></tr><tr><td>

Preserve theme

</td><td>

Preserves the theme and CSS elements on the target instance. As a result, your target instance will keep its theme, its look and feel after a clone. The default setting is to preserve the theme on the target instance.

</td></tr><tr><td>

Lock settings for this clone request

</td><td>

If you use a clone profile, this option locks the settings and options at the time of the clone request. Any subsequent changes to the clone profile, regardless of when the clone runs, do not affect the clone request. This option is not selected by default.

</td></tr><tr><td>

Amount of data copied from specific tables

</td><td>

Limits the number of days of historical data for the task table and its child tables \(e.g. Incident, problem, and change tables\) to 90 days. To reduce clone time, consider excluding large tables altogether. When excluding tables, your target instance will have the same table schema and hierarchy \(i.e. empty usable tables\) as the source instance.

The default setting is to clone all data from the task table and its child tables to the target instance.

</td></tr><tr><td>

Preserve In Progress Update Sets

</td><td>

Preserves the last 90 days of in-progress update sets in the global application scope. This option allows you to keep in-progress, global update sets created within the last 90 days on your target instance.**Note:** This option does not preserve your in-progress scoped update sets. Update sets that are older than 90 days will not be saved. It is recommended to review and commit your update sets before cloning. The default is to not preserve update sets.

</td></tr><tr><td>

Clone frequency

</td><td>

This option allows you to schedule recurring clones from your source to your target instance. It allows you to define the clone frequency and the maximum number of occurrences. By default, the clone frequency is set to None. For more information about scheduling cloning, see [Schedule cloning](schedule-cloning.md).

</td></tr></tbody>
</table>12. Click **Submit**.

    If there are no issues with the clone request, the system displays the Authenticate Target modal.

    If your clone request preserves large tables, a warning message displays the large tables from your preserver list. You can cancel your clone request and remove the tables from your preserver list, or you can specify a reason and continue the clone request.

13. In the **Username** and **Password** fields, enter the username and password for an administrator account on the target instance and then click **Authenticate**.

14. Review the clone settings and click **OK**.

    An email is sent to the supplied address after the clone finishes, is canceled, or has an error.


## What to do next

You can:

-   [Schedule automatic clonings](schedule-cloning.md).
-   [Cancel your clone request](cancel-clone.md).
-   [View the cloning history](t_ViewCloneHistory.md) of completed clonings.


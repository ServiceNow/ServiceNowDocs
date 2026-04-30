---
title: Clone options
description: A reference topic that contains various configurations for your data when requesting a clone.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-08-25"
reading_time_minutes: 3
breadcrumb: [Reference, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Clone options

A reference topic that contains various configurations for your data when requesting a clone.

<table id="table_ajq_bss_gr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lock settings for this clone request

</td><td>

If you use a clone profile, this option locks the settings and options at the time of the clone request. Any subsequent changes to the clone profile, regardless of when the clone runs, don’t affect the clone request. This option isn’t selected by default.

</td></tr><tr><td>

Amount of data copied from the Task table

</td><td>

Limits the number of days of historical data for the task table and its child tables \(for example Incident, problem, and change tables\) to 90 days. To reduce clone time, consider excluding large tables altogether. When excluding tables, your target instance has the same table schema and hierarchy \(empty usable tables\) as the source instance.

The default setting is to clone all data from the task table and its child tables to the target instance.

</td></tr><tr><td>

Clone frequency

</td><td>

This option enables you to schedule recurring clones from your source to your target instance. It enables you to define the clone frequency and the maximum number of occurrences. By default, the clone frequency is set to None. -   None
-   Weekly
-   Every 2 weeks
-   Every 4 weeks

</td></tr><tr><td>

Backup options

</td><td>

Specifies which backup the clone request uses.-   Most recent: The clone uses the latest nightly backup, unless an upgrade or a major change to the instance occurred.
-   On-demand backup: The backup begins at your specified clone start time. Your clone will only begin after the backup completes, pushing back the time at which the cloning process can start.

</td></tr><tr><td>

Exclude tables specified in Exclusion List

</td><td>

Helps to prevent cloning records from tables on the source instance, which are listed under  **Instance clone** &gt; **Exclude Tables**. If a table is on the Exclusion List, the clone excludes the records on the table as well as records on the child tables. When excluding tables, their table schema and hierarchy are still cloned to your target instance. As a result, your target instance will have empty but usable tables after the clone.

**Note:** Default table exclusions are still excluded and aren't affected by this setting. Including tables containing auditing, license usage, logging, and notifications.

If you need the data from your excluded tables, you can choose to disable this setting.

The default setting is that tables specified in the Exclusion List are excluded from a clone.

</td></tr><tr><td>

Exclude audit and log data

</td><td>

Helps to prevent the cloning of audit and log records from the source instance. This exclusion creates empty but usable audit and log tables on the target instance. **Note:** If you exclude audit and log data from your clone, the activity stream for records doesn't match the source instance. The activity stream relies on the audit table to generate the history.

The default setting is that audit and log data are excluded from a clone.

</td></tr><tr><td>

Exclude attachment data

</td><td>

Helps to prevent the cloning of certain files from the sys\_attachment table, such as:-   Video files
-   Image files
-   Other large binary files

**Note:** Default attachments and other system-relevant files \(for example catalog item images, theme images, and icons\) aren’t affected by this setting.

The following default attachments and other system-relevant files aren’t affected by this setting and aren’t excluded from a clone:-   Table name values that start with ZZ\_.
-   Table names: sys\_certificate, sc\_cat\_item,sys\_upgrade\_manifest, ecc\_agent\_jar, ecc\_agent\_mib, sys\_store\_app, or invisible.sys\_store\_app.

The default setting is to exclude attachment data.

</td></tr><tr><td>

Preserve theme

</td><td>

Preserves the theme and CSS elements on the target instance. As a result, your target instance will keep its theme, its look and feel after a clone. The default setting is to preserve the theme on the target instance.

</td></tr><tr><td>

No. of days of In-progress Global Update Sets to be preserved

</td><td>

Preserves the last 90 days of in-progress update sets in the global application scope. This option enables you to keep in-progress, global update sets created within the last 90 days on your target instance.**Note:** This option doesn’t preserve your in-progress scoped update sets. Update sets that are older than 90 days aren't saved. Review and commit your update sets before cloning.

The default isn’t to preserve update sets.

</td></tr></tbody>
</table>**Parent Topic:**[Instance Clone reference](instance-clone-reference.md)


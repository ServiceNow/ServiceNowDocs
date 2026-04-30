---
title: Explore upgrade history log
description: Reduce processing time by extracting all upgrade related logs into a separate file named database-upgrade\_&lt;timestamp&gt;.log. You can also zip the file and attach it to upgrade history.
locale: en-US
release: yokohama
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reviewing upgrade history, Upgrade History tool in Upgrade Console, Upgrade Console tools, Using Upgrade Console, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Explore upgrade history log

Reduce processing time by extracting all upgrade related logs into a separate file named database-upgrade\_&lt;timestamp&gt;.log. You can also zip the file and attach it to upgrade history.

## Before you begin

Role required: admin.

## About this task

When the upgrade starts, the upgrade log messages are written to both the localhost\_log file and the database-upgrade\_&lt;timestamp&gt;.log file. When the upgrade is done, the database-upgrade\_&lt;timestamp&gt;.log file is uploaded to the upgrade history table.

## Procedure

1.  Navigate to **All** &gt; **System Logs** &gt; **Utilities**.

    **Note:** You can implement this step to view the extracted database-upgrade\_&lt;timestamp&gt;.log file only after the upgrade is done.

2.  Click **Node Log File Download**.

    The database-upgrade\_&lt;timestamp&gt;.log file appears in the list of log files.

    **Note:** The localhost\_log file consists of all the logs. The database-upgrade\_&lt;timestamp&gt;.log file consists of logs only related to the upgrade.

    The database-upgrade\_&lt;timestamp&gt;.log file appears only if the `glide.db.upgrade.log.save_to_db.enabled` property is set to True. By default, the `glide.db.upgrade.log.save_to_db.enabled` is set to True.

3.  Go to **Admin** &gt; **Upgrade Management Console** &gt; **Upgrade History**.

    A list of upgrades shows up.

4.  Click the required upgrade from the list.

    You can see database-upgrade\_&lt;timestamp&gt;.log file is automatically attached to the upgrade.

    **Note:** The database-upgrade\_&lt;timestamp&gt;.log file gets attached only if the `glide.db.upgrade.log.save_to_db.enabled` property is set to True. By default, the `glide.db.upgrade.log.save_to_db.enabled` is set to True.

5.  Download the zipped database-upgrade\_&lt;timestamp&gt;.log file.

    **Note:** The database-upgrade\_&lt;timestamp&gt;.log file has been zipped to reduce the download time.


**Parent Topic:**[Reviewing upgrade history](../concept/um-review-history.md)


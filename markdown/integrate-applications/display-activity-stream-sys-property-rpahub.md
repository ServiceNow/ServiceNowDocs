---
title: Display an activity stream for bot processes and robots in RPA Hub
description: Configure the system property to display an activity stream for bot processes and robots in RPA Hub.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, RPA Hub, Workflow Data Fabric]
---

# Display an activity stream for bot processes and robots in RPA Hub

Configure the system property to display an activity stream for bot processes and robots in RPA Hub.

## Before you begin

You must do this task in the classic environment.

Role required: admin

## Procedure

1.  In the **All menu** filter, enter `sys_properties.list`.

2.  In the **Name** column, search for the **glide.activity.rule.exclude.document\_tables** system property.

3.  In the **Value** field, add the table names `-cmdb_ci_rpa_process` and `-cmdb_ci_rpa_robot` separated by a comma.

    Adding prefix \(-\) to the table name includes the documents of the table in the activity stream.

    ![The glide.activity.rule.exclude.document_tables system property screen displaying the new values for the Value field.](../image/activity-stream-sys-property-rpahub.png)

4.  Select **Update**.



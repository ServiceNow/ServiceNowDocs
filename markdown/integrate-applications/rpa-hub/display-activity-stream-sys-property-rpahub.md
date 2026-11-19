---
title: Display an activity stream for bot processes and robots in RPA Hub
description: Configure the system property to display an activity stream for bot processes and robots in RPA Hub.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/integrate-applications/rpa-hub/display-activity-stream-sys-property-rpahub.html
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
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

    \[Omitted image "activity-stream-sys-property-rpahub.png"\] Alt text: The glide.activity.rule.exclude.document\_tables system property screen displaying the new values for the Value field.

4.  Select **Update**.


**Parent Topic:**[Managing RPA Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/integrate-applications/rpa-hub/managing-rpa-hub.md)


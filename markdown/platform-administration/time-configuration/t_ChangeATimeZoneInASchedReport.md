---
title: Change a time zone in a scheduled report
description: By default, scheduled reports use the time zone of the user who runs them \(the user in the Run As field\) to evaluate the query parameters. You are able to change this time zone.
locale: en-US
release: xanadu
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Change a time zone in a scheduled report

By default, scheduled reports use the time zone of the user who runs them \(the user in the **Run As** field\) to evaluate the query parameters. You are able to change this time zone.

## About this task

For example, a report on 'incidents open today' resolves 'today' based on the user's time zone. To manually specify the time zone used to resolve the parameters of the report:

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **Scheduled Reports**.

2.  Choose the report with the time zone you want to edit.

3.  Add Run as fields to the layout.

    1.  Configure the form layout to add the **Run as tz** field to the **Scheduled Report** form. See [Configuring the form layout](../../form-administration/concept/configure-form-layout.md#) for instructions.

        The Run as tz field lets you choose either a the time zone of the user who configured the schedule, or a specific time zone.

    2.  Configure the form layout to add the **Run as \[+\]** field to the **Scheduled Report** form. See [Configuring the form layout](../../form-administration/concept/configure-form-layout.md#) for instructions.

        The Run as \[+\] field lets you choose a specific user to run the report as.

4.  Select the time zone you would like to use.

5.  Select the user to run the report as.

6.  Click **Submit**.


**Parent Topic:**[Using time configuration](../using-time-configuration.md)


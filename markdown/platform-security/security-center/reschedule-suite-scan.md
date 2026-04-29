---
title: Reschedule a scan suite
description: Change the schedule of your scan suites to suit your needs.
locale: en-US
release: australia
product: Security Center
classification: security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Scan suites, Security scanner, Security configuration console, Security Center, Platform Security]
---

# Reschedule a scan suite

Change the schedule of your scan suites to suit your needs.

## Before you begin

Role required: admin, sn\_vsc.security\_center\_viewer

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Security Center**.

2.  In the **Tools** section, select **Security scanner**.

3.  Select **Suites** in the menu on the left edge of the screen.

4.  Open the suite you want to reschedule.

5.  Select the **Schedule** tab.

6.  Select an existing schedule, or select **New** to create a new schedule.

7.  In the **Scheduled Scan** form, fill in the fields as needed.

<table id="table_l15_tcs_4dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the scan schedule

</td></tr><tr><td>

Run

</td><td>

Select the how often your suite will run.**Note:** Additional fields will appear to help define your schedule. These fields vary depending on your selection.

</td></tr><tr><td>

Active

</td><td>

Whether the schedule is active. Inactive schedules are never executed.

</td></tr><tr><td>

Conditional

</td><td>

Select to enable the **Condition** field, where you can define a scripted condition for your schedule.

</td></tr><tr><td>

Condition

</td><td>

A scripted condition for your schedule. The suite will only run when the script evaluates to `true`.

</td></tr><tr><td>

Run as tz

</td><td>

Which timezone the schedule uses when determining when to run.

</td></tr></tbody>
</table>
**Parent Topic:**[Scan suites](../concept/sec-center-suites.md)


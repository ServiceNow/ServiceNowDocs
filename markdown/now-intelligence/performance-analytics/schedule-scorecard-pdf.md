---
title: Schedule the export and distribution of an indicator
description: Schedule an indicator to automate its distribution.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Schedule the export and distribution of an indicator

Schedule an indicator to automate its distribution.

## Before you begin

This feature requires the licensed version of [Performance Analytics](../concept/c_PremiumPerformanceAnalytics.md#).

Role required: pa\_power\_user, pa\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Scheduled Indicators** and create a new record.

<table id="table_nys_fdc_p1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Indicator

</td><td>

Select the indicator that you want to export.

</td></tr><tr><td>

Breakdown

</td><td>

Select a breakdown to filter the indicator scores.

</td></tr><tr><td>

Element

</td><td>

If you selected a breakdown, select a breakdown element to show only scores associated with that element.

</td></tr><tr><td>

Chart

</td><td>

Select this checkbox to include the scores visualization in the PDF. The visualization is the same as displayed on the indicator Analytics Hub.

</td></tr><tr><td>

Breakdowns

</td><td>

Select this checkbox to include the scores for each breakdown and breakdown element in a table at the bottom of the PDF. If you have selected a **Breakdown** and **Element**, the breakdowns displayed at the bottom of the PDF are 2nd-level breakdowns.

</td></tr><tr><td>

Users

</td><td>

Users who should receive the indicator.

 To receive indicators, users must have an Email address defined and have **Notifications** set to **Enable** in their user records.

</td></tr><tr><td>

Groups

</td><td>

Groups that should receive the indicator.

</td></tr><tr><td>

Email addresses

</td><td>

Email addresses of users who should receive the indicator but who are not in the system.

</td></tr><tr><td>

Active

</td><td>

Check box that enables \(selected\) or disables \(cleared\) scheduling for the indicator.

</td></tr><tr><td>

Run

</td><td>

Frequency for exporting the indicator.

</td></tr><tr><td>

Time

</td><td>

Time of day to export the indicator.

</td></tr><tr><td>

Conditional

</td><td>

Check box that displays \(selected\) or hides \(cleared\) the **Condition** field, which allows you to specify conditions under which the indicator is exported.

</td></tr><tr><td>

Condition

</td><td>

User-created script that checks for certain conditions to be true before exporting the indicator.

 This field is visible only when **Conditional** is selected.

</td></tr><tr><td>

Subject

</td><td>

Text that appears in the subject line of the distribution email.

</td></tr><tr><td>

Introductory message

</td><td>

Additional message that is delivered with the indicator.

</td></tr><tr><td>

Include with

</td><td>

Additional scheduled indicators to send.

</td></tr><tr><td>

Orientation

</td><td>

Select the page orientation, Landscape or Portrait.

</td></tr><tr><td>

Zip output

</td><td>

Select this check box to send the indicator as a zip file.

</td></tr></tbody>
</table>

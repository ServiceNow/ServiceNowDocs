---
title: Configure scheduled email reports in DPM Admin Center
description: Send periodic emails of KPI metrics to the DPM solution owners.
locale: en-US
release: yokohama
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: task
last_updated: "2025-04-17"
reading_time_minutes: 3
breadcrumb: [Use the Admin Center in Digital Portfolio Management, Configuring Digital Portfolio Management, Digital Portfolio Management, IT Service Management]
---

# Configure scheduled email reports in DPM Admin Center

Send periodic emails of KPI metrics to the DPM solution owners.

## Before you begin

Role required: sn\_dpm.dpm\_admin

## Procedure

1.  Navigate to **All** &gt; **Digital Portfolio Management** &gt; **DPM Admin Center** &gt; **Settings**.

2.  Select **Email properties**.

3.  Show or hide the email button on the Enterprise portfolio page.

    -   Turn on the toggle key to show the email button.
    -   Turn off the toggle key to hide the email button.
    If the toggle key is on, this **Send email** button displays on the Enterprise portfolio page in the DPM Workspace.

    ![Email button displayed on the Enterprise Portfolio page.](../image/dpm-email-button.png)

4.  Configure the scheduled metrics email.

    -   Turn on the toggle key to enable emails. This will periodically send emails of KPI metrics to DPM managers that own solutions. The default period is set to two weeks.
    -   Turn off the toggle key to disable emails.
5.  Define the maximum number of recipients per scheduled period.

6.  Your first email is automatically sent two weeks from the day you tun on the toggle key. If you'd like to change the frequency of emails, follow these steps:

7.  Select **Generate visualization attachments**.

8.  In the new window, fill in the fields.

<table id="table_b35_lqt_1fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run

</td><td>

How often the scheduled job runs:-   **Daily**: Runs daily, at a designated time.
-   **Weekly**: Runs on a weekly basis, at a designated time and day of the week.
-   **Monthly**: Runs on a monthly basis, at a designated time and day of the month.
-   **Periodically**: Runs on a designated repeating interval.
-   **Once**: Runs for a single occurrence only.
-   **On Demand**: Runs immediately, on demand.
-   **Business Calendar: Entry Start**: Runs on the starting entry dates for the business calendar that you select in the Business Calendar field. A scheduled job runs for the starting date of each of the business entries that you defined for the business calendar.

For example, if the business calendar represents a fiscal year, and the starting date of each entry is a fiscal month, the scheduled job runs on the first day of each month.

-   **Business Calendar: Entry End**: Runs for the ending date for the business calendar that you select in the **Business Calendar** field. This selection runs in the same manner as **Business Calendar: Entry Start**, but for the end dates of the associated business calendar entries.


</td></tr><tr><td>

Time zone

</td><td>

The time zone of the time you specify:-   **None**: Use your time zone.
-   **Use System Time Zone**: Use the default system time zone that is specified for your instance.
-   Choose an actual time zone. For example, **US/Pacific**.


</td></tr><tr><td>

Time

</td><td>

Time of day when the scheduled job runs, expressed in hours, minutes, and seconds on a 24-hour clock. The selection that you make in the Time zone field determines the time zone for this entry.

</td></tr><tr><td>

Day

</td><td>

Day that the scheduled job runs. This field appears only if you select **Monthly** or **Weekly** in the Run field.-   If **Run** is set to **Weekly**, select the day of the week. For example, select Wednesday.
-   If Run is set to **Monthly**, select the day of the month. For example, select 25 for the 25th day of the month.


</td></tr><tr><td>

Repeat interval

</td><td>

Duration of the repeat interval for each scheduled job execution. This field appears only if you select **Periodically** in the Run field. Enter the duration in the number of days, hours, or minutes. For example:-   To run the scheduled job every four days, enter `4` in the **Days** field.
-   To run it every 26 hours, enter `26` in the **Hours** field.
-   If it should repeat at an interval of 13:30:25, enter `13` in the Hours field, and then enter `30` and `25` in the two unlabeled fields after it.


</td></tr><tr><td>

Starting

</td><td>

Date and time of the first scheduled job. This field appears only if you select **Periodically** in the Run field.

</td></tr></tbody>
</table>9.  Select **Execute Now**.

10. Select **Email performance metrics for DPM managers**.

    **Note:** You must schedule the visualization attachments to run at least two hours prior to **Email performance metrics to DPM managers**.

11. In the new window, fill in the fields.

12. Select **Execute Now**.


**Parent Topic:**[Use the Admin Center in Digital Portfolio Management](../concept/dpm-admin-center.md)


---
title: Configure scheduled jobs for Self-Service Analytics
description: Schedule when to run the deflection configuration to generate the activities that match an activity pattern within an activity window.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Self-Service Analytics, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure scheduled jobs for Self-Service Analytics

Schedule when to run the deflection configuration to generate the activities that match an activity pattern within an activity window.

## Before you begin

[Set up the deflection configuration for Self-Service Analytics](configure-deflection-ssa.md).

Role required: admin

## About this task

You configure the duration of processing the deflection configuration for a user entity. This configuration is optional for consumers and customer contacts. The scheduled job captures data for Self-Service Analytics and stores the generated data in the Deflection Metric \[ssa\_deflection\_metric\] table.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Configure the scheduled script processed for a user entity in a scheduled job.

    -   For consumers, select **Deflection Analytics for Consumers**.
    -   For customer contacts, select **Deflection Analytics for Contacts**.
    -   For user entities other than consumers and customer contacts, click **New** and select **Automatically run a script of your choosing** to create another scheduled job or modify an existing schedule job.
3.  On the Scheduled Script Execution form, verify the default field values for consumers and customer contacts or fill in the values for a custom configuration.

<table id="table_e3d_ccq_jlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the scheduled script execution.

</td></tr><tr><td>

Active

</td><td>

Option to activate the script at the scheduled date and time. By default the job is inactive.

</td></tr><tr><td>

Run

</td><td>

Type of schedule to execute the script on. Choices are:-   Daily
-   Weekly
-   Monthly
-   Periodically
-   Once


</td></tr><tr><td>

Day

</td><td>

-   If you select **Weekly** as the **Run** value, the day of the week.
-   If you select **Monthly** as the **Run** value, the day of the month.


</td></tr><tr><td>

Repeat Interval

</td><td>

If you select **Periodically** as the **Run** value, the duration between each script execution.**Note:** This setting does not account for Daylight Savings Time changes. For example, if you select a period of one day, this adds 24 hours to the starting time of the job. If the start time was configured during a period with Daylight Savings Time, the job executes with a one hour offset on days when that time zone is not in Daylight Savings Time.

</td></tr><tr><td>

Time

</td><td>

If you select **Daily**, **Weekly**, or **Monthly** as the **Run** value, the time of day, based on a 24-hour clock.

</td></tr><tr><td>

Starting

</td><td>

Date and time of the first scheduled script execution.

</td></tr><tr><td>

Application

</td><td>

Application that contains the script.

</td></tr><tr><td>

Conditional

</td><td>

Option to run a scheduled job if certain conditions are met in the associated script.

</td></tr><tr><td>

Condition

</td><td>

Conditional script that determines whether a scheduled job must run. The last expression of the script should evaluate to a Boolean \(true or false\) value. This field appears only when the **Condition** check box is selected.

</td></tr><tr><td>

Run this script

</td><td>

Script to run at the scheduled date and time.For a new scheduled script, copy the script from the existing script \(Deflection Analytics for Consumers or Deflection Analytics for Contacts\) and modify the `deflectionAnalyticsService.captureDeflectionAnalytics('*sys\_ID*')` field value to include the sys\_id of your deflection configuration record. For information about identifying the sys\_id, see [The unique record identifier \(sys\_id\)](https://www.servicenow.com/docs/access?context=c_UniqueRecordIdentifier&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Click **Update** for consumers and customer contacts or **Submit** to save a custom configuration.


**Parent Topic:**[Configure Self-Service Analytics](config-ssa.md)


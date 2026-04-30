---
title: Configure signal schedules in Proactive Prompts
description: Schedule that determines when to run the signal configuration to generate prompts that notify the user to act on.
locale: en-US
release: xanadu
product: Proactive Prompts
classification: proactive-prompts
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Proactive Prompts, Proactive Prompts, HR Service Delivery, Employee Service Management]
---

# Configure signal schedules in Proactive Prompts

Schedule that determines when to run the signal configuration to generate prompts that notify the user to act on.

## Before you begin

The signal schedule is the triggering action in the prompt's workflow that evaluates the configuration and generates prompts that are then delivered to users.

Role required: sn\_pp.admin

## Procedure

1.  Navigate to **All** &gt; **Proactive Prompts** &gt; **Signal Schedules**.

2.  Select **New**.

3.  On the form, fill in the fields:

<table id="table_ehb_kyp_nvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the signal schedule job.

</td></tr><tr><td>

Active

</td><td>

Option to activate the signal schedule job.

</td></tr><tr><td>

Conditional

</td><td>

Option to run the scheduled job based on certain conditions in the associated script.

</td></tr><tr><td>

Condition

</td><td>

Conditional script that determines whether a scheduled job must run. The last expression of the script should evaluate to a Boolean \(true or false\) value.**Note:** This field is displayed only when the **Conditional** option is selected.

</td></tr><tr><td>

Run

</td><td>

Type of schedule to execute the job on. The available options are:-   Daily
-   Weekly
-   Monthly
-   Periodically
-   Once
-   On demand
-   Business Calendar: Entry Start
-   Business Calendar: Entry End


</td></tr><tr><td>

Time zone

</td><td>

Time zone of the signal schedule job.The Use System Time Zone option causes the job to run in the time zone of the instance running the job. If no time zone is selected, the job runs in the time zone of the user who entered the time.

</td></tr><tr><td>

Time

</td><td>

The time when the schedule must be executed in 24-hour clock format.**Note:** This field is available only when the **Run** field value is Daily, Weekly, or Monthly.

</td></tr></tbody>
</table>4.  Select **Submit**.



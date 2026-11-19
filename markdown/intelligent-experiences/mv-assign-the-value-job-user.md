---
title: Assign the value job user
description: Assign an active user to run value jobs so that Control Tower can calculate value. When the assigned user is inactive, value calculation stops.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mv-assign-the-value-job-user.html
release: brazil
topic_type: task
last_updated: "2026-11-19"
reading_time_minutes: 1
breadcrumb: [Value, Configure, Measure AI systems, Measure AI systems, Super Intelligence Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Assign the value job user

Assign an active user to run value jobs so that Control Tower can calculate value. When the assigned user is inactive, value calculation stops.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

A value job requires an active user to operate. Make sure to assign an active user to run value jobs.

If the user becomes inactive, the value job will not run, and the calculation of values will cease. You will see a message indicating that the value calculation has stopped because the user required to run the value job is inactive. The message will also prompt you to assign an active user to resume the value calculation.

## Procedure

1.  Navigate to **All** &gt; **Control Tower** &gt; **Home**.

2.  Navigate to **Settings** &gt; **Rules and templates** &gt; **Templates** &gt; **Value controls**.

    \[Omitted image "mv-assign-the-value-job-user.png"\] Alt text: Value controls tab with the value.job.user panel open, showing its description and a Value field for selecting the user who runs value calculation jobs.

3.  Select **value.job.user**.

4.  From the **Value** list, select a user.

    You can select any active user, because Control Tower uses the user to run the job rather than to check privileges.

5.  Select **Update**.

    **Note:** If you see a message indicating that the value calculation has stopped because the user required to run the value job is inactive, select **Assign User** from the message. From the **Value** list, select a user, and then select **Update**.


## Result

Value jobs run based on the schedule.


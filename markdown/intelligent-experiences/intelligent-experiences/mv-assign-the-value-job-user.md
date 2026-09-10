---
title: Assign the value job user
description: Assign an active user to run value jobs so that the AI Control Tower can calculate value. When the assigned user is inactive, value calculation stops.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
---

# Assign the value job user

Assign an active user to run value jobs so that the AI Control Tower can calculate value. When the assigned user is inactive, value calculation stops.

## Before you begin

Role required: sn\_ai\_governance\_ai\_steward

## About this task

A value job requires an active user to operate. Make sure to assign an active user to run value jobs.

If the user becomes inactive, the value job will not run, and the calculation of values will cease. You will see a message indicating that the value calculation has stopped because the user required to run the value job is inactive. The message will also prompt you to assign an active user to resume the value calculation.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home**.

2.  Navigate to **Settings** &gt; **Rules and templates** &gt; **Templates** &gt; **Value controls**.

3.  Select **value.job.user**.

4.  From the **Value** list, select a user.

    You can select any active user, because the AI Control Tower uses the user to run the job rather than to check privileges.

5.  Select **Update**.

    **Note:** If you see a message indicating that the value calculation has stopped because the user required to run the value job is inactive, select **Assign User** from the message. From the **Value** list, select a user, and then select **Update**.


## Result

Value jobs run based on the schedule.


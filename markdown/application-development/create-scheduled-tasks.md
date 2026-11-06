---
title: Create and manage scheduled tasks in Arc
description: Schedule Arc to run an instruction once or on a repeating schedule, and run, edit, copy, pause, or delete any schedule from one list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/create-scheduled-tasks.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 3
keywords: [scheduled tasks, schedules, blueprints, reminders, Custom Reminder]
breadcrumb: [Use, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Create and manage scheduled tasks in Arc

Schedule Arc to run an instruction once or on a repeating schedule, and run, edit, copy, pause, or delete any schedule from one list.

## Before you begin

Role required: sn\_app\_arc.user

## About this task

Schedules allow you to create and manage repetitive tasks.

All schedules run in your device's local time.

You can have up to 50 schedules. If Arc is closed at a scheduled time, that run is marked missed and the schedule moves on to its next time instead of running late.

## Procedure

1.  In Arc, select **Schedules** in the sidebar.

    The **Schedules** window lists your schedules. If you don't have any yet, it shows **No Schedules Yet**.

2.  Select **Add New Schedule**.

3.  Select a blueprint, or select **Custom Reminder** to write your own instruction.

    Blueprints are ready made routines, grouped under **Rituals &amp; Planning**, such as **Morning Briefing** and **Weekly Review**, and **Comms &amp; Follow-ups**, such as **Standup Digest** and **Inbox Sweep**. A blueprint fills in the details for you.

    Other blueprints are grouped under **Tickets &amp; Incidents**, such as **Incident Watch** and **Change Request Watch**, and **Dev**, which has **PR Review Digest**. **Custom Reminder** is listed first, under **Start Fresh**.

4.  In the **Name** field, enter a name for the schedule, and in the **Message** field, enter the instruction for Arc to run.

5.  Under **What time?**, select how often the schedule runs, and then set the date and time.

    Choose **Once**, **Every day**, **Weekdays \(Mon–Fri\)**, **Weekly**, **Monthly**, or **Every N minutes**. Times use 24 hour local time.

6.  To get a notification instead of having Arc run the instruction, select **Reminder only**.

    **Reminder only** appears only for **Custom Reminder**, because blueprints run as a task. Use it when you want to be reminded of something, such as calling a colleague. Leave it off when you want Arc to do the work, such as fetching your unread email every morning.

7.  Select **Schedule it**.

    The schedule appears as a card in the **Schedules** list.

8.  Manage a schedule from its card.

    -   To run a schedule right away, select **Run now**. The schedule keeps its regular time.
    -   To change a schedule, select **Edit**.
    -   To create a similar schedule, select **Duplicate**. The new schedule starts with the same details.
    -   To pause or resume a schedule, turn its toggle off or on.
    -   To remove a schedule, select **Delete**.
    To find a schedule, enter part of its name in **Search schedules**. To update the list, select the refresh icon.


-   **[Create a schedule from a chat in Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/create-schedule-from-chat.md)**  
Ask Arc in a chat to run a task or remind you at a set time, without opening the scheduling window.
-   **[Edit a schedule in Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)**  
Change a schedule's name, instruction, or timing without creating it again from scratch.
-   **[Duplicate a schedule in Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/duplicate-schedule.md)**  
Copy an existing schedule as a starting point for a new one, so you don't enter the same details again.
-   **[Pause or resume a schedule in Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/pause-schedule.md)**  
Stop a schedule from running for a while without deleting it, and turn it back on when you need it again.
-   **[Run a schedule now in Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/run-schedule-now.md)**  
Run a schedule right away, outside its regular time, for example to test a new schedule or get a result early.
-   **[Delete a schedule in Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/delete-schedule.md)**  
Remove a schedule you no longer need so that it stops running.

**Parent Topic:**[Using ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-using.md)


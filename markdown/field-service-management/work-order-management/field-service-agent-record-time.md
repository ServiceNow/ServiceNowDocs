---
title: Record time worked for a task or activity manually
description: Agents can record time worked on a work order task as well as time spent on other activities.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Recording time worked, Updating task status, Completing work orders on the web interface, Use, Field Service Management]
---

# Record time worked for a task or activity manually

Agents can record time worked on a work order task as well as time spent on other activities.

## Before you begin

Role required: wm\_agent

## About this task

An agent can record time worked directly from a work order task by selecting **Record Time** from the Work Order Task form. An agent can record time regardless of the work order task state. An agent can also record time spent on other activities from the **Time Worked** list by creating a time worked record, recording the time, and selecting a category.

**Note:** If multiple rate cards are enabled, agents can also select rate types when creating time worked entries.

A time card is created for each category type and work order task. The total hours recorded on each time card are then recorded on the current time sheet in the **Time Cards** related list.

## Procedure

1.  To record time worked for a task or an activity:

    -   Navigate to a work order task and select **Record Time**. Selecting **Record Time** opens a **Time Worked** form with the **Task** and **User** field already populated.
    -   Navigate to **Time Sheets** &gt; **My Time Worked** and select **New**. This opens a **Time Worked** form with the **User** field already populated.
    ![record time form](../image/record-time.png)

2.  If necessary, select the work order task in the **Task** field.

3.  If necessary, select the **Work Date**.

    This field defaults to the current date.

4.  Select a **Category** for the time being recorded.

5.  Select a **Rate type** for the time being recorded.

    When multiple rate types are enabled for Field Service Management, agents can specify multiple rate types for time worked against a task.

6.  Fill in the **Time worked**.

7.  Provide any additional information in the **Comments** field and select **Submit.**

    The **Time Worked** form is saved and added to the **Time Worked** list. If your entry is the first time worked entry for the selected category, a time card is created for that category and the time worked record is added to the card. If a time card for the category exists, the time worked record is added to that card.



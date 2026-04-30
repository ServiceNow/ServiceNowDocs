---
title: Schedule the generation of a daily report
description: Generate and distribute a daily scheduled report that summarizes the agent's work performance via email.
locale: en-US
release: yokohama
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Channels in Workforce Optimization for ITSM, Channels in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Schedule the generation of a daily report

Generate and distribute a daily scheduled report that summarizes the agent's work performance via email.

## Before you begin

Role required: sn\_channel\_mgmt.admin

## About this task

|When|Then|
|----|----|
|​The **Send Daily Agents Report**schedule job is run|The**sn\_channel\_mgmt.agents\_report** event is executed|
|The**sn\_channel\_mgmt.agents\_report** event is executed|The **Daily Agents Report** notification is triggered|
|The **Daily Agents Report** notification is triggered|The **daily\_agents\_reports** email script is executed|
|The **daily\_agents\_reports** email script is executed|An email is sent to all managers|

**Note:** ​To change the existing report, modify the **daily\_agents\_reports** email script.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search and select **Send Daily Agents Report**.

    The scheduled script form appears.

3.  Click the link **here** to edit the record.

4.  Select the **Active** check box.

5.  In the **Run** field, ensure that the option **Daily** is selected.

    The script, by default, sends the agents' work summary report daily to the managers.

6.  Select the **Time zone**.

7.  Do any of the following:

    -   To update the scheduled job, select **Update**.
    -   To execute the scheduled script, select **Execute Now**.

## Result

All managers and additional managers of the teams receive an email notification that summarizes their agents' performance.

**Parent Topic:**[Setting up Channels in Workforce Optimization for ITSM](../concept/setup-channels-configurable-workforce-optimization-itsm.md)


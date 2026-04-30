---
title: Activate a scheduled job to generate data to view portfolio financials
description: Activate and define Data generation for financials in SPW/PPW scheduled job to migrate budget from old data model to new data model and view portfolio financials.
locale: en-US
release: xanadu
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2025-01-10"
reading_time_minutes: 1
breadcrumb: [Configure portfolio financials in Portfolio Planning, Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Activate a scheduled job to generate data to view portfolio financials

Activate and define **Data generation for financials in SPW/PPW** scheduled job to migrate budget from old data model to new data model and view portfolio financials.

## About this task

It is a one-time activity to define and run this scheduled job to view portfolio financials.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Filter the name field to locate and open **Data generation for financials in SPW/PPW**.

3.  Select Active option to activate and schedule the job.

4.  Edit the fields on the Scheduled Script Execution form to customize the job and meet your requirements.

    For more information about the field description and scripts, see [Automatically run a script of your choosing](https://www.servicenow.com/docs/access?context=t_ScheduleAScriptExecution&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US#t_ScheduleScriptExecution).

5.  Select **Execute Now** to execute the scheduled job.


## Result

All the required mappings to view the portfolio financials for Epics, Demands, and Projects are mapped.

To validate if the data generation job is successful, navigate to **All** &gt; **System Definition** &gt; **Tables** and check the mappings for **Investment** record in the **Project** \[sn\_align\_core\_project\] table.


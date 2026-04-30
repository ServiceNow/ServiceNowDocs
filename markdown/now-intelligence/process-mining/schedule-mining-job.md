---
title: Schedule a Process Mining job
description: Schedule a Process Mining job to mine one or more projects later.
locale: en-US
release: yokohama
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a project using Classic view, Using Process Mining, Process Mining, Platform Analytics]
---

# Schedule a Process Mining job

Schedule a Process Mining job to mine one or more projects later.

## Before you begin

Role required: sn\_process\_optimization\_power\_user or sn\_process\_optimization\_admin

**Note:** You can create only one scheduled job for each project. You can, however, associate multiple projects to a job. If there are several projects scheduled for mining within a job, the projects execute sequentially. For example, a job which has Projects 1 and 2 scheduled within it will mine Project 1 first. Then, it begins mining Project 2 after mining of Project 1 completes.

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Scheduled Jobs** &gt; **Create New**.

2.  On the Scheduled Process Mining Job form, populate the applicable fields for the job you want to create, then select **Submit**.

    See [descriptions of fields on a scheduled job record](https://www.servicenow.com/docs/access?context=t_ScheduleTheGenerationOfAnEntity&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

3.  In the Project Definitions section, select **Edit**.

4.  From the **Edit Members** form, select the projects in the **Collection** column that you want to mine and move them to the **Project Definitions List** column.

5.  Select **Save**.

    The scheduled job runs on the frequency that you've configured.


## What to do next

-   View a successfully generated project from the Analyst Workbench.
-   Navigate to **All** &gt; **Process Mining** &gt; **Scheduled Jobs** &gt; **All Jobs** to view scheduled process mining jobs.

**Parent Topic:**[Create a project using Classic view](../task/create-proj.md)


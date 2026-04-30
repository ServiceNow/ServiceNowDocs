---
title: Upgrade existing projects on activating multicurrency plugin
description: Execute the PM upgrade project currency for active projects and PM upgrade project currency for inactive projects scheduled jobs to upgrade your active and inactive projects, respectively, after you activate the multicurrency plugin. Select the scheduled jobs and run them on demand to upgrade your projects in project currency only when necessary.
locale: en-US
release: zurich
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Upgrade existing projects on activating multicurrency plugin

Execute the **PM upgrade project currency for active projects** and **PM upgrade project currency for inactive projects** scheduled jobs to upgrade your active and inactive projects, respectively, after you activate the multicurrency plugin. Select the scheduled jobs and run them on demand to upgrade your projects in project currency only when necessary.

## Before you begin

Role required: admin or it\_project\_manager

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Click the **PM upgrade project currency for active projects**.

3.  Click **Execute Now** to upgrade all your existing active projects to project currency.

    On execution of the job, all amounts in the cost-related fields of the Project, Project Task, Baseline, Cost Plan, Cost Plan Breakdown, Benefit Plan, Benefit Plan Breakdown forms are copied from functional currency to project currency fields. Once the values of functional currency fields are copied to the project currency fields project currency cannot be edited since the financial costs already exist.

4.  To upgrade your inactive projects, click **PM upgrade project currency for inactive projects**.

5.  Click **Execute Now**.

    On executing the scheduled job, the project currency value for all existing projects is set to the functional currency. The project currency in the Project Tasks, Baselines, Cost Plans, Cost Plan Breakdowns, Benefit Plans, Benefit Plan Breakdowns, Expense Lines forms is set to functional currency.

    **Note:** The jobs may have performance impact depending on the number of projects and cost plans, hence run the jobs only when necessary.



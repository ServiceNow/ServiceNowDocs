---
title: Run the entity onboarding job for Workday reports
description: Run the specified scheduled job to get new entities that may have been added in Workday. Running this job ensures that the entity mapping table is updated.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management with Workday, Integrating ESG Management with other applications, Environmental, Social, and Governance Management]
---

# Run the entity onboarding job for Workday reports

Run the specified scheduled job to get new entities that may have been added in Workday. Running this job ensures that the entity mapping table is updated.

## Before you begin

At least one [Workday report](activate-the-workday-reports.md) must be activated.

Role required: admin

## About this task

When you run the **Workday entity onboarding** scheduled job, the job uses the first activated report in the system to invoke Workday. Workday then sends the entity ID in the CSV file along with the activated report value.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  In the **Search** field, enter `Workday`.

3.  From the filtered search results, select and open the **Workday entity onboarding** scheduled job.

4.  Select **Execute Now**.



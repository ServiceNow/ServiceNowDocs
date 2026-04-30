---
title: Map industry titles to role levels
description: Create a connection between common job titles in your industry with the role levels in your organization to provide relevant skill recommendations at the role groups level.
locale: en-US
release: zurich
product: Talent Development Core
classification: talent-development-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Skills Foundation, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Map industry titles to role levels

Create a connection between common job titles in your industry with the role levels in your organization to provide relevant skill recommendations at the role groups level.

## About this task

Role levels for employees must have either been imported into the Role level \[sn\_skills\_int\_role\_level\] table or added manually. For more information on the import process, see [Load job architecture data into your ServiceNow instance](load-data-skills-tables.md).

## Before you begin

Role required: sn\_skills\_int.job\_arch\_admin, sn\_skills\_int.admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for and select the **Train Title classification** scheduled job.

3.  Select **Execute now** to run the job.

4.  Make the Job architecture title classification solution active.

    1.  Navigate to **All** and enter `ml_solution.list` in the filter navigator.

    2.  In the drop-down list of the **Search**

5.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

6.  Search for and select the **Predict Title classification** scheduled job.

7.  Select **Execute now**.


## Result

The mapping is created in the Role Level M2M Industry Title \[sn\_skills\_int\_role\_level\_m2m\_ind\_title\] table. A maximum of one industry title is fetched for each role level.


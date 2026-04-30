---
title: Resume a lifecycle event case
description: Resume a lifecycle event case after a workflow error or workflow timeout.
locale: en-US
release: xanadu
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create an HR case for a lifecycle event, Lifecycle Events, HR Service Delivery, Employee Service Management]
---

# Resume a lifecycle event case

Resume a lifecycle event case after a workflow error or workflow timeout.

## Before you begin

Role required: sn\_hr\_le.case\_writer

## Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Lifecycle Events Cases**, and open the lifecycle event case that errored.

    ![Lifecycle event case where the second activity set errored out.](../image/resume-lifecycle-event-case.png)

2.  Identify and fix the error.

    **Tip:** Navigate to the **Comments and Work Notes** section in the case to view the work note on why the workflow failed.

3.  Click **Resume** to resume the case.

    The lifecycle event case resumes from where it was errored out.

    **Important:** You cannot resume the case if it was in **Closed Complete**, **Closed Incomplete**, or **Cancelled** state.



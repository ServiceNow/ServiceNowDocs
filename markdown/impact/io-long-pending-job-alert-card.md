---
title: Analyze job details for long pending jobs
description: Stay ahead of job delays by identifying and acting on jobs that breach predefined lateness thresholds. The Long Pending Jobs alert card tracks pending jobs by lateness duration, so you can act on the pending jobs before they affect the downstream workflows and miss the SLAs.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Performance, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Analyze job details for long pending jobs

Stay ahead of job delays by identifying and acting on jobs that breach predefined lateness thresholds. The Long Pending Jobs alert card tracks pending jobs by lateness duration, so you can act on the pending jobs before they affect the downstream workflows and miss the SLAs.

## Before you begin

Role required: admin

The job details capability is available to all users regardless of their tier level.

## About this task

Instance Observer's job monitoring capability has expanded with a new telemetry to help you analyze job behavior more deeply. Existing IO job performance capability already supports in-depth analysis into job execution, anomalies, and top resource-intensive jobs — top 2000 by execution time.

The new telemetry addresses pending jobs that have been scheduled but are stuck in a ready or queuing state, and have not transitioned into an executing phase.

Jobs get stuck because of:

-   Insufficient resources to pick up new jobs
-   Something is blocking execution
-   New jobs are unable to start

What you need:

-   Visibility into how long the pending jobs have been overdue.
-   An alert so you can act on them — either reschedule or terminate the stuck jobs to keep the instance healthy.

The long pending jobs alert provides minute-level telemetry on the pending jobs, showing at the instance level how many jobs are pending and by how many minutes they are overdue on average.

Beyond pending jobs, this telemetry not only helps you to know how long a job takes to run, but also which jobs aren't running at all, and how long they're being delayed.

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Monitor** &gt; **Instance Observer**.

2.  In the **Performance** menu, select the **Job Details** option.

3.  Select the instance from the **Instance** field.

4.  Select the metrics **Job Overdue \(Pending\)** and **Top 2K Pending Jobs** options in the **Metrics** field to get specific reports on the overdue pending jobs and those at the top 2000 level.

5.  Select the **Date Range**, and **Get Snapshot**.

    ![Job details highlighting overdue pending and top 2K jobs.](../image/io-job-overdue-pending.png)

6.  Select a point in the chart of the **Job Overdue \(Pending\)** section to get a continuous, minute-level view of how long pending jobs have been overdue across your instance.

    At any point in time, you can identify the jobs that are delayed or overdue from the scheduled time. This analysis helps you spot outliers before they impact your workflows.

7.  Scroll down to the **Top 2K Pending Jobs** table to view the listing of specific jobs that are most overdue from their scheduled time, along with their priority, job ID, and approximate overdue duration.

8.  To set filter conditions on the job name, job ID, or priority, select ![menu icon.](../../../common/image/icon_menu3lines.png)

    For example, you can enter **discovery** to filter all jobs that have **discovery** in their name.

    ![Sorting and filtering pending jobs.](../image/io-job-overdue-priority.png)

9.  To sort the jobs by their priority level, select ![sort icon.](../../../reuse/icons/product-icons/sort-descending-outline-24.svg)

    For instances running thousands of jobs, analyzing job by job isn't practical. You can switch to **Priority** view, grouping jobs by their assigned priority level. This sorting helps you to categorize and act on jobs in bulk. For example, address all mid-server discovery jobs \(priority 110\) or test jobs \(priority 100\) in bulk, rather than managing them individually.

10. To download the data, select **Download as CSV**.


## What to do next

You can also set alert card for pending jobs. For more information, see [Configure long pending jobs alert by job priority](io-long-pending-jobs.md).

**Parent Topic:**[Performance](../concept/instance-observer-performance.md)


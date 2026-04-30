---
title: Understand your Scheduled Jobs dashboard
description: Visit scheduler dashboard to learn about key health metrics and insights of scheduled jobs.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Monitor System Events and Scheduled Jobs dashboards, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Understand your Scheduled Jobs dashboard

Visit scheduler dashboard to learn about key health metrics and insights of scheduled jobs.

Navigate to **All** &gt; **System Diagnostics** &gt; **Scheduled Jobs Dashboard**.

![Scheduled jobs dashboard.](../image/scheduled-jobs-dashboard.png)

The following cards show up on the dashboard

<table id="table_wwg_yvf_nxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Stuck Jobs

</td><td>

The scheduled jobs that are pinned to a non-existent node show up here. If a scheduled job is assigned to run on a non-existent node and is a parent job that doesn't have Startup as the **Trigger Type**, it is classified under **Stuck Jobs**. The System ID column states the node that the job was assigned to run. One of the reasons of a job being classified as **Stuck Jobs** is if an instance was cloned from another instance and now there are jobs pinned to run on the old instance's nodes. You can take the following actions on the stuck jobs:

-   You can delete it to remove the job from sys\_trigger permanently.
-   You can recover these jobs which clears the**System ID** column data and allows it to run again based on its **Next Action** time.

</td></tr><tr><td>

Permanent Error Jobs

</td><td>

The scheduled jobs which have a **State** of **Permanent Error** show up here. If you have upgraded from a pre-Utah version to a more recent version, a fix script is executed and it sets the scheduled jobs to **Permanent Error** state if the job was a parent job or a standalone job and picked up to run on a specific node that no longer exists. You can also set the job state to **Permanent Error** manually. You can take the following actions on the permanent error jobs:

-   You can delete it to remove the job from sys\_trigger permanently.
-   You can recover these jobs which set the state back to **Ready**. It can again run based on its **Next Action** time.

</td></tr><tr><td>

Pending Jobs

</td><td>

Jobs that are to be executed soon.

</td></tr><tr><td>

Running Jobs

</td><td>

Jobs that are actively running.

</td></tr><tr><td>

Jobs Classification \(optional\)

</td><td>

Optional way to group certain jobs based on filter conditions to collect job completion history by the defined group/classification. You can set up these classifications in the Job Classification Rules table. The default classification is TriggerType.JobName.

</td></tr><tr><td>

Total Execution Count

</td><td>

Graphical representation of the total number of scheduled job executions on your instance over a period of time. The default time period is last 24 hours. You can view the data only from last 7 days. The data originate from the sys\_scheduler\_job\_history table.

**Note:** When you click on an execution count in the graph, the Scheduled Job History list shows up. The list of jobs have been grouped using Jobs Classification concept with Trigger Type as either Run Once or Recurring.

</td></tr><tr><td>

Average Lateness

</td><td>

Graphical representation of the average lateness in milliseconds of all scheduled jobs on your instance over a period of time. The default time period is last 24 hours. You can view the data only from last 7 days. The data originates from the sys\_scheduler\_job\_history table.**Note:** When you click on a lateness average data in the graph, the Scheduled Job History list shows up. The list of jobs have been grouped using Jobs Classification concept with Trigger Type as either Run Once or Recurring.

</td></tr><tr><td>

Scheduled Job Trends

</td><td>

List of completed jobs grouped by Job Classification concept. The default time period is last 24 hours. You can view the data only from last 7 days. The data originate from the sys\_scheduler\_job\_history table.

</td></tr></tbody>
</table>**Note:** For both **Stuck Jobs** and **Permanent Error Jobs** tiles, the data and columns originate from the sys\_trigger table. Both the tiles are used to cleanup jobs and keep the scheduled jobs in a positive state. Select the required tile to see the list view of the jobs. The **Lateness** column on both the lists refers to how late the job is based on the time it was supposed to run. If **Next Action** is in the past, the lateness is calculated as the current time minus the next action time. For example, if the job was scheduled to run two minutes ago, then lateness is two minutes. If the job is scheduled to run in the future, then the lateness is 0.

## Scheduled Job Trends

This table provides details on the history of completed jobs by classifications. Default view provides the data for last 24 hours.

<table id="table_rdk_cfq_hyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Job Classification

</td><td>

Provides a way of grouping similar type of jobs based on job name, trigger type \(recurring, run once, etc.\).

</td></tr><tr><td>

Priority

</td><td>

Priority at which the jobs are processed.

**Note:** The lower the number, the higher is the priority. For example, priority of 10 is higher than 100.

</td></tr><tr><td>

Execution Count

</td><td>

Number of times the job has been executed within a timeframe.

</td></tr><tr><td>

Average Processing Time\(s\)

</td><td>

Average time needed to process the jobs.

</td></tr><tr><td>

Total Processing Time\(s\)

</td><td>

Total time needed to process the jobs.

</td></tr></tbody>
</table>
---
title: Run historical data collection for a Platform Analytics Solution
description: After you activate an Platform Analytics Solution, run a historical data collection job. This job gives you immediate insight from your existing data.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Collect data for Platform Analytics Solutions, Analytics solutions, Platform Analytics]
---

# Run historical data collection for a Platform Analytics Solution

After you activate an Platform Analytics Solution, run a historical data collection job. This job gives you immediate insight from your existing data.

## Before you begin

Role required: pa\_admin, admin

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Data Collector** &gt; **Jobs**.

2.  Filter the list of jobs for those containing the word 'Historic'.

3.  Locate and open the historic job that corresponds to your new Platform Analytics Solution.

4.  Go to the Collection Parameters section, and set the **Relative start** and **Relative start interval** fields to collect data from as far back as you want.

    The Data Collector runs a number of times equal to the number of days \(or other collection periods\) specified in the form. For example, the default configuration of 60 days causes the Data Collector to run 60 times in succession. The Data Collector starts at T-60 days and examines all records as if the date were 60 days ago. After processing those records, the Data Collector runs again at T-59 days. The Data Collector repeats the process until it gets to the current date.

    Each day's collection may take a minute or two to complete depending on the size of your tables. A historic data collection over multiple months may take some time to complete.

    If the product or application for which you installed the Platform Analytics Solution is new, you might not have much historical data. In this case, you can shorten the relative start interval. If you have not yet used the product or application, you can skip collecting historical data altogether.

5.  Ensure that the user specified in the **Run as** field exists.

    If you are using domain separation, you collect only records from domains which the **Run as** user can view. However, the ACL permissions of the **Run as** user do not affect data collection.

6.  Verify that the **Run As tz** time zone is appropriate for your company.

    Database queries based on this indicator source use this time zone. This time zone affects the timestamps for the data collection job. This time zone also defines what day is "Today" for conditions like \[\[Created\]\[on\]\[Today\]\].

7.  Click **Execute Now** to run the job.

8.  Navigate to **Data Collector** &gt; **Job Logs**.

9.  Look at the **State** of the job you are running.

    Refresh the view periodically until the job completes. If the job is successful, the **State** changes to `Collected`.


## Collecting historical data for newly installed Platform Analytics Solution

You have just installed a set of Platform Analytics Solutions. You want to run the initial historical data collection job on them, so you navigate to **Performance Analytics** &gt; **Data Collector** &gt; **Jobs**. To find the historic jobs for Platform Analytics Solutions, you filter the list on \[\[Name\]\[contains\]\[Historic\]\].

**Tip:** When you start to create your own historical data collector jobs, include the word 'Historic' in their names.

![List of historic jobs showing Knowledge historical job](../image/nowintel-solution-jobs.png)

You decide to run the job for the Knowledge Management solution first. To ensure that nobody has run the knowledge management historical job yet, you navigate to **Data Collector** &gt; **Job Logs** and filter the list on \[\[Job\]\[contains\]\[knowledge\]\].![Job logs showing no knowledge management jobs run since last zBoot](../image/nowintel-solution-no-knowledge.png)

In this case, you see that the job has not been run since the last zBoot. So you navigate back to the **Jobs** list and open **\[PA Knowledge\] Historic Data Collection**.![Record for a historical data collection job](../image/nowintel-solution-histjob.png)

In the form, you verify the following details:

1.  The **Relative start** field is set for the default 60 days, which is fine for you.
2.  The **Run as** user exists on your instance. Otherwise, you would have to choose a different user.

    ![System Administrator user on instance](../image/nowintel-solution-sysadmin.png)

3.  The time zone is appropriate for your company.

You are satisfied with the settings for the historical job, so you click **Execute Now**. After a few minutes, the job is shown as `Collected` in the job logs.![Job log showing collected Knowledge Management historical job](../image/nowintel-solution-complete-hist-job.png)

**Parent Topic:**[Collect data for Platform Analytics Solutions](../concept/collect-data-nowintel-solutions.md)

**Previous topic:**[Collect data for Platform Analytics Solutions](../concept/collect-data-nowintel-solutions.md)

**Next topic:**[Schedule data collection for a Platform Analytics Solution](schedule-job-nowintel-solution.md)

**Related topics**  


[Collect historical data](t_RunHistoricalDataCollection.md)


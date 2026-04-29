---
title: Run multiple scheduled jobs for alert grouping
description: Run multiple scheduled jobs in parallel to group alerts. This helps prevent overwhelming the system during surges \(alert storms\).
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Scheduled jobs and parameters for alert grouping, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Run multiple scheduled jobs for alert grouping

Run multiple scheduled jobs in parallel to group alerts. This helps prevent overwhelming the system during surges \(alert storms\).

## Before you begin

Role required: admin

## About this task

The current scheduled job operates with a single thread. During alert surges \(alert storms\), processing takes significantly longer. To address this impact, now multiple jobs can process alerts within the scheduled job. This enhances scalability and improves overall performance during high-volume periods.

The number of jobs to be running in the alerts processing is defined in a new property **sa\_analytics.agg.alert\_grouping.num\_of\_jobs**. The job number is sent as a parameter to the relevant method.

**Note:** In this scenario, the procedure for increasing the scale-out from no scale-out \(single job\) to 2 jobs is shown.

You can efficiently manage and run multiple scheduled jobs in parallel to group alerts using specific properties. These properties allow you to tailor the grouping criteria to meet your needs, ensuring that alerts are processed based on assignment groups, domain separation, or group-by fields. The available properties are:

-   **sa\_analytics.agg.group\_alert\_with\_same\_assignment\_group\_only**: Groups alerts that share the same assignment group. By default, the value is set to false. If you want to set this property to true, create a property with the same name and set the value to true.
-   **sa\_analytics.agg.group\_alert\_with\_same\_domain\_only**: Groups alerts that belong to the same domain. By default, the value is set to true.
-   **sa\_analytics.agg.group\_alert\_with\_same\_group\_by\_fields**: “Group by” property, with comma-separated list of field names that need to have matching values across alerts to allow alerts to be grouped together. The property can contain alert field names \(such as assignment\_group\), CI field names \(such as alert\_cmdb\_ci.location\), alert additional info field names \(such as additional\_info.state\) or alert tags \(such as t\_data\_center\). When the specified field values match each other between alerts, those alerts can be grouped together.

**Note:** To ensure efficient scale-out, at least one of these properties must be defined to establish some form of separation or grouping logic. This is necessary to ensure that all alerts belonging to the same group are processed correctly by specific jobs, creating a logical division of alerts.

Without setting at least one of these properties to true, the alerts will not be properly segregated. For instance, if you do not define any grouping logic \(set any property to true\) and both the assignment group and domain separation are set to false, the scale-out will not work, and all alerts will be processed by a single scheduled job.

## Procedure

1.  Navigate to **All** &gt; **System definition** &gt; **Scheduled jobs**.

2.  Locate the scheduled job: Service Analytics group alerts using RCA/Alert Aggregation.

3.  For all existing scheduled jobs Service Analytics group alerts using RCA/Alert Aggregation, set the value in the **Active** column to **false**.

    ![Deactivate scheduled job](../../service-operations-workspace-itom/image/deactivate-scheduled-job.png "Deactivate scheduled job")

4.  Create a new property **sa\_analytics.agg.alert\_grouping.num\_of\_jobs**, or if it already exists, update the property to the desired number of multiple scheduled jobs for alert grouping such as 2 or 4.

5.  Clone the scheduled job definition from the Scheduled jobs \[sys\_auto\] table to the desired number of multiple scheduled jobs for alert grouping.

6.  In the new jobs, in the Run this script section, call the new JS function queryS0 \(instead of old query\(\) function\) and transfer to it the job number as input parameter.

    **Note:** Job numbers must start at 0 and follow consecutively: 0, 1, 2, 3, 4...

7.  Fix hashes in the \[sa\_analytics\_status\] and \[sa\_hash\] table by selecting the earliest hash with the same prefix, cloning it, and adding the hash name suffix, for example, “\_groupingX”, where X is the job number.

    In the case of scaling out from no scale-out \(single job\) to 2 jobs, and for the hash name `last_alert_process_time`, clone it to maintain the same value as in `last_alert_process_time`:

    -   `last_alert_process_time_grouping0`
    -   `last_alert_process_time_grouping1`
    In the case of scaling out from no scale-out \(single job\) to 4 jobs, and for the hash name `last_alert_process_time`, clone it to maintain the same value as in `last_alert_process_time`:

    -   `last_alert_process_time_grouping0`
    -   `last_alert_process_time_grouping1`
    -   `last_alert_process_time_grouping2`
    -   `last_alert_process_time_grouping3`
    |Hash name|Table|
    |---------|-----|
    |query\_job\_last\_run|sa\_hash|
    |last\_alert\_process\_time|sa\_analytics\_status|
    |last\_staging\_table\_update\_time|sa\_analytics\_status|
    |last\_staging\_table\_truncate\_time|sa\_analytics\_status|
    |analytics\_trigger\_g1|sa\_hash|

8.  Activate the new jobs by selecting the **Active** check box for each job.

    ![Activate scheduled job](../../service-operations-workspace-itom/image/active-scheduled-job.png "Activate scheduled job")


## Result

The scheduled job Service Analytics group alerts using RCA/Alert Aggregation is set up to run multiple jobs simultaneously for alert grouping.


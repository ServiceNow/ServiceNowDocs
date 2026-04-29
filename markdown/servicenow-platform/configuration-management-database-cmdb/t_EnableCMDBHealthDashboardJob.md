---
title: Enable and configure a CMDB Health Dashboard job
description: Enable and configure the CMDB Health Dashboard jobs that process CMDB Health tests, to start calculating CMDB Health scores for the completeness, compliance, correctness KPIs, associated metrics, and relationships.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Enable and configure a CMDB Health Dashboard job

Enable and configure the CMDB Health Dashboard jobs that process CMDB Health tests, to start calculating CMDB Health scores for the **completeness**, **compliance**, **correctness** KPIs, associated metrics, and relationships.

## Before you begin

Role required: sn\_cmdb\_admin or admin

## About this task

In the base system, CMDB Health Dashboard jobs are disabled by default. Enable and configure the respective job for the CMDB health KPI that you want data collected and aggregated for. You can schedule a job to run on a recurring schedule, or run it once at any time.

For more information about how CMDB Health Dashboard jobs work, see the [Understanding the CMDB HealthDashboard Numbers](https://community.servicenow.com/community?id=community_article&sys_id=d27bbd60db64cd50770be6be139619c8) blog post in the ServiceNow Community.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Health Preference**.

2.  Select **Scheduled Jobs** on the left-side bar and then select the job that you want to enable or configure.

    |CMDB Health Dashboard job|Description|
    |-------------------------|-----------|
    |CMDB Health Dashboard - Completeness Score Calculation|Script for calculating the completeness KPI of CMDB health.|
    |CMDB Health Dashboard - Compliance Score Calculation|Script for calculating the compliance KPI of CMDB health.|
    |CMDB Health Dashboard - Correctness Score Calculation|Script for calculating the correctness KPI of CMDB health.|
    |CMDB Health Dashboard - Relationship Score Calculation|Script for calculating the CI relationships KPI of CMDB health.|
    |CMDB Health Dashboard - Relationship Compliance Processor|Script for calculating compliance of relationships with suggested relationships, and with hosting and containment rules.|

3.  Review the default configuration, and update as necessary.

<table id="table_z2n_s3k_p5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Job name. Leave this field with the pre-populated name.

</td></tr><tr><td>

Active

</td><td>

Select to activate the job.

</td></tr><tr><td>

Conditional

</td><td>

If selected, the scripted condition must evaluate to true before the job can run.

</td></tr><tr><td>

Run

</td><td>

Configure the schedule for job execution, or select **On Demand** to run the job manually when needed.

 If **Active** is selected, then additional fields appear according to your choice. For example, **Repeat Interval** \(when **Run** is set to **Periodically**\), and **Time** for various settings of **Run**. Fill in the details to set precise running times.

</td></tr><tr><td>

Time zone

</td><td>

Local time zone.

</td></tr><tr><td>

Run this script

</td><td>

The job's script. **Note:** Changes to the script might result in unexpected behavior.

</td></tr></tbody>
</table>4.  Select **Execute Now** to immediately run the job once.


## Result

After you enable a CMDB Health Dashboard job, the results for the KPI are aggregated and appear in the CMDB Health dashboard and CI Health widget on CI forms, at the CMDB, class, and CI levels.


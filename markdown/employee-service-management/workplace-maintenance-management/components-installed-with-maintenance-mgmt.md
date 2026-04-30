---
title: Components installed with Workplace Maintenance Management
description: Different roles and components or tables are available with the installation of Workplace Maintenance Management.
locale: en-US
release: zurich
product: Workplace Maintenance Management
classification: workplace-maintenance-management
topic_type: reference
last_updated: "2025-09-07"
reading_time_minutes: 6
breadcrumb: [Reference, Workplace Maintenance Management, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Maintenance Management

Different roles and components or tables are available with the installation of Workplace Maintenance Management.

## Roles installed with Workplace Maintenance Management

Navigate to **All** &gt; **System Definition** &gt; **Roles** &gt; **.**

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|sn\_wsd\_wc.manager|Provides read access to all data including Occupancy Dashboard and other dashboards.|sn\_wsd\_wc.user|
|sn\_wsd\_wc.admin|Provides admin access to configure and set up the Workplace Connectors application|sn\_wsd\_wc.manager|
|sn\_wsd\_wc.user|Provides read access to only a few columns and fields. The read access is set up by administrators.|None|

## Tables installed with Workplace Maintenance Management

Navigate to **All** &gt; **System Definition** &gt; **Tables.**

<table id="table_t5k_1kj_qpb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workplace Maintenance Plan\[sn\_wsd\_maintenance\_plan\]

</td><td>

Stores preventive maintenance plans.

</td></tr><tr><td>

Workplace Maintenance Plan Items\[sn\_wsd\_maintenance\_m2m\_plan\_maint\_item\]

</td><td>

Stores all the items \(locations or assets\) that are part of a maintenance plan.

</td></tr><tr><td>

Workplace Maintenance Schedule

\[sn\_wsd\_maintenance\_schedule\]

</td><td>

Stores all the schedules \(daily, weekly, monthly and so on\) created for a Maintenance plan.

</td></tr><tr><td>

Create a maintenance case

 \[sn\_wsd\_maintenance\_case\]

</td><td>

Stores information about maintenance cases.

</td></tr><tr><td>

Maintenance Plan Record\[sm\_m2m\_maint\_plan\_to\_record\]

</td><td>

Stores the plan records \(a record for every schedule and maintenance item combined\).

</td></tr><tr><td>

Workplace Maintenance Service Configuration \(sn\_wsd\_maintenance\_service\_config\)

</td><td>

Associates workplace services and sets scheduling conditions for a plan record. The schedule job fetches plan records that have a maintenance schedule template for a workplace service to create maintenance cases. For more information, see [Create plan service configuration](../task/create-maint-service-config.md) and [Workplace planned maintenance scheduled job](../concept/sch-job-planned-nightly.md).

</td></tr></tbody>
</table>## Workplace Maintenance Management Scheduled Jobs

Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs.**

<table id="table_ylk_m4d_gzb"><thead><tr><th>

Scheduled Job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workplace Planned Maintenance Nightly Run

</td><td>

A scheduled job runs every 48 hours \(2 days\) to fetch plan records and create maintenance cases. For more information, see [Workplace planned maintenance scheduled job](../concept/sch-job-planned-nightly.md).

</td></tr><tr><td>

Workplace Maintenance Case Daily Data Collection

</td><td>

This scheduled job collects data and populates it in the Workplace Maintenance Management Dashboard.Collects data as specified in the Relative start and Relative end fields. The collection time is time zone specific.

</td></tr><tr><td>

Workplace Maintenance Case Historical Data Collection

</td><td>

This scheduled job collects historical data and populates it in the Workplace Maintenance Management Dashboard.Collects data as specified in the Relative start and Relative end fields. The collection time is time zone specific.

</td></tr></tbody>
</table>## Properties installed with Workplace Maintenance Management

Navigate to the **All** context menu in your instance and enter **sys\_properties.list** in the search Filter option. Search for Workplace Maintenance Management properties in the Application context menu.

<table id="table_q45_cpq_kgc"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_wsd\_maintenance.optimise\_plans

</td><td>

Property to optimize plans by the Optimise Cleaning Activities Agentic AI workflow. For more information, see [Optimize cleaning activities agentic workflow](../../now-assist-wsd/concept/optimize-cleaning-activities-agent.md).**Note:** Workplace Maintenance managers should enter the sys ID of the maintenance plan record in the Value field. For multiple plans that you want to optimize, enter comma separate mainteance plan ID values. For example- "**a23321432, 3243245dsf**". Copy the Sys ID of a maintenance plan from your ServiceNow® instance URL link. https://&lt;instance\_name&gt;.service-now.com/now/workplace-management/maintenance-plan/3243245dsf. Here, the maintenance plan sys ID is 3243245dsf.

</td></tr><tr><td>

sn\_wsd\_maintenance.optmise\_cleaning\_min\_utilisation\_threshold

</td><td>

Property to analyze the minimum space utilization threshold. Default value is **40**. If the utilization for a workplace maintenance plan is below this range, it is deactivated if it meets all the deactivation criteria set forth by the Optimise Cleaning Activities Agentic AI workflow. For more information, see [Optimize cleaning activities agentic workflow](../../now-assist-wsd/concept/optimize-cleaning-activities-agent.md).

</td></tr><tr><td>

sn\_wsd\_maintenance.optmise\_cleaning\_max\_utilisation\_threshold

</td><td>

Property to analyze the maximum utilization threshold. Default value is **80**. If the utilization for a workplace maintenance plan case goes beyond this range, a new maintenance case is added by the Optimize Cleaning Activities Agentic AI workflow. For more information, see [Optimize cleaning activities agentic workflow](../../now-assist-wsd/concept/optimize-cleaning-activities-agent.md).

</td></tr></tbody>
</table>## Scheduled Job installed with Maintenance Management

Navigate **All** &gt; **System Definition** &gt; **Scheduled Jobs** or enter `sys_properties.list` in the Filter search box or context menu of an instance. Search for Workplace Maintenance Management scheduled jobs.

<table id="table_xvw_wgs_kgc"><thead><tr><th>

Scheduled Job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Optimise cleaning activities

</td><td>

Optimise cleaning Activities Agentic Workflow is triggered when this scheduled job is run. This scheduled job runs in the UTC time zone. For more information, see [Optimize cleaning activities agentic workflow](../../now-assist-wsd/concept/optimize-cleaning-activities-agent.md)

</td></tr><tr><td>

Workplace Maintenance Case Historical Data Collection

</td><td>

Schedule job to gather data from existing records for the first time or when a new case is added. This allows to analyze trends and performance metrics over time by collecting snapshots of data using scheduled jobs, which can be configured for various frequencies, such as daily, monthly, or yearly.

</td></tr><tr><td>

Workplace Planned Maint Nightly Run

</td><td>

Schedule job to automatically create maintenance cases for planned workplace maintenance based on active maintenance plan records in your instance. It runs nightly, checks maintenance plans for upcoming required work, and if a plan has an associated maintenance template, it generates a maintenance case and updates the plan's next run time. It fetches all active maintenance plan records that have a "Next run time" indicating maintenance is due soon. If the plan has a template defined, the scheduled job creates a new maintenance case for that plan and updates the plan's "Next run time" for the subsequent maintenance cycle. If no maintenance template is associated with a plan, the job moves to the next plan record in the queue.When this scheduled job is executed, Maintenance cases are generated in Preventative Maintenance.

</td></tr><tr><td>

Workplace Maintenance Case Daily Data Collection

</td><td>

Schedule job to automatically create planned maintenance cases based on existing planned maintenance records with associated templates and schedules. This job runs nightly to populate the Maintenance Management dashboard with data, enabling facilities teams to manage and execute routine maintenance tasks effectively. The job is scheduled to run daily, typically at night. It collects data from the Workplace Maintenance service configuration and Maintenance Schedule records. For planned maintenance records with an associated template and schedule, the job creates new, open maintenance cases. The collected data then populates the Maintenance Management dashboard, providing a clear overview of planned maintenance activities. It automates the process of creating maintenance cases, reducing manual effort and improving efficiency.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Maintenance Management references](../concept/workplace-maintenance-mgmt-references.md)

**Previous topic:**[Maintenance plan schedule examples](../concept/maintenance-plan-examples.md)

**Next topic:**[Workplace Lease Administration](../../workplace-lease-administration/concept/workplace-lease-admin-feat.md)


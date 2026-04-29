---
title: Talent Acquisition Dashboard
description: The Talent Acquisition Dashboard helps get an overview of the workload and performance details of the hiring efforts in your organization.
locale: en-US
release: australia
product: Recruiter Workspace
classification: recruiter-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Recruitment Workspace, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Talent Acquisition Dashboard

The Talent Acquisition Dashboard helps get an overview of the workload and performance details of the hiring efforts in your organization.

The users of the Talent Acquisition Dashboard require the following role.

|User|Description|Required role|
|----|-----------|-------------|
|admin \(sn\_ta\_hiring\_core.admin\)|This user can edit the data display in the dashboard.|itil|
|Recruiter \(sn\_ta\_hiring\_core.recruiter\)|This user can view the data on the dashboard.|itil|

The Talent Acquisition Dashboard has the **Workload** tab and the **Performance** tab. Each tab has several card views to display data.

The data visualization on the **Workload** tab is as follows:

## Dashboard data view

![Data visualization displayed in the workload tab of the Talent Acquisition dashboard.](../images/ta-dashboard-workload.png "Workload tab view")

|Card|Data type|Description|
|----|---------|-----------|
|Active Job Requisitions|Number|Number of active job requisitions.|
|Job Requisition by Recruiter|Stacked bar|Data on the requisitions by their owning recruiters and their States.|
|Job Requisition by State|Bar chart|Data visualization of the job requisitions by their States.|
|Job Requisition On Hold|Number|Number of job requisitions on hold.|
|Job Requisition On Hold by Reason|Pie chart|Percentages of requisitions put on hold are segregated by reasons.|
|Job Requisitions opened per month|Line graph|Monthly trend of opening job requisitions.|
|Active Job Applications|Number|Number of active job applications.|
|Job Requisitions older than 7 days|Number|Number of job requisitions that are created more than 7 days back.|
|Job Requisitions older than 30 days|Number|Number of job requisitions that are created more than a month back.|
|Job Requisition older than 90 days|Number|Number of job requisitions that are created more than 3 months back.|

Apart from the data cards, you can use the following filters to skim through the data on the tab.

-   Job Requisition State
-   Hiring Manager
-   Department
-   Cost Center
-   Primary Location
-   Employment Type
-   Created Date

![Data visualization displayed in the performance tab of the Talent Acquisition dashboard.](../images/ta-hdasboard-performance.png "Performance tab view")

|Card|Data type|Description|
|----|---------|-----------|
|Job Requisitions filled over time|Line graph|Trend of positions filled over the time.|
|Average time spent per Job Requisition state|Bar chart|Time that is spent on a job requisition segregated by their states.|
|Job Requisitions filled in the last 30 days|Number|Number of job requisitions created more than a month back.|
|Average time from New to Ready|Number|Aggregated time that is spent to move a requisition from **New** to **Ready** State.|
|Average time from Ready to Closed|Number|Aggregated time that is spent to move a requisition from **Ready** through the **Closed** State.|
|Average time from New to Open|Number|Aggregated time that is spent to move a requisition from **New** to **Open** State.|
|Average time from application submission to hired|Number|Aggregated time that is spent from the submission of an application to hire.|
|Application Time per State|Graph|Aggregated time an application remains in one state.|

**Parent Topic:**[Recruitment Workspace reference](recruitment-workspace-reference.md)


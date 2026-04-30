---
title: Create a criteria for a matching rule in Work scheduler
description: Add a criteria for a matching rule to enable assignment of work items to team members based on the rule.
locale: en-US
release: zurich
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Assigning work, Work scheduler, Workforce Optimization for ITSM, IT Service Management]
---

# Create a criteria for a matching rule in Work scheduler

Add a criteria for a matching rule to enable assignment of work items to team members based on the rule.

## Before you begin

Role required: admin

## About this task

The following matching rules, which are available by default, are based on the selection criteria matching type:

|Rule name|Work configuration name|Table|UX app route|
|---------|-----------------------|-----|------------|
|Incident Matching rule|Incidents|Incident \[incident\]|Incident|
|Problem Matching rule|Problems|Problem \[problem\]|Problem|
|Requested item Matching rule|Requested items|Requested Item \[sc\_req\_item\]|Requested item|
|Request Matching rule|Requests|Request \[sc\_request\]|Request|
|Catalog Task Matching rule|Catalog Task|Catalog Task \[sc\_task\]|Catalog task|
|Change Request Matching rule|Change Request|Change Request \[change\_request\]|Change requests|
|Change Task Matching rule|Change Task|Change Task \[change\_task\]|Change task|

For information on how matching criteria works, see [Matching criteria for work items in Work scheduler](../concept/work-items-assignment-matching-criteria-wfo-itsm.md).

The following four criteria are available by default:

-   WFO-Mandatory skills
-   WFO-Availability
-   WFO-Optional skills
-   WFO-Timezone overlap

## Procedure

1.  Navigate to **All** &gt; **Work scheduler** &gt; **Matching Rules**.

2.  In the Matching Rules list, select a matching rule; for example, the **Incident matching rule**.

3.  In the Select Criteria related list, select **New.**

4.  Fill in the fields on the form.

    For information on creating a new matching criteria, see [Create assignment workbench matching criteria](https://www.servicenow.com/docs/access?context=create-assignment-wkbench-criteria&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

5.  Select **Submit**.


-   **[Matching criteria for work items in Work scheduler](../concept/work-items-assignment-matching-criteria-wfo-itsm.md)**  
The assignment workbench uses configurable matching criteria, such as skills and availability, to evaluate the agents in a selected group and provide an overall ranking.

**Parent Topic:**[Assigning work using Work Scheduler in Workforce Optimization for ITSM](../concept/work-scheduler-wfo-itsm.md)


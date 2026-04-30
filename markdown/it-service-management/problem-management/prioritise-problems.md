---
title: Data lookup for prioritizing problems
description: To follow ITIL guidelines, problem records are prioritized by the impact and urgency of the problem.
locale: en-US
release: zurich
product: Problem Management
classification: problem-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Problem Management, IT Service Management]
---

# Data lookup for prioritizing problems

To follow ITIL guidelines, problem records are prioritized by the impact and urgency of the problem.

Problem prioritization is available on new instances.

On the problem form, users select values from the **Impact** and **Urgency** fields that determine which priority value is generated for the problem.

|Field|Definition|
|-----|----------|
|Impact|Impact is a measure of the effect of an incident, problem, or change on business processes.|
|Urgency|Urgency is a measure of how long the resolution can be delayed until an incident, problem, or change has a significant business impact.|
|Priority|Priority is based on impact and urgency, and it identifies how quickly the service desk should address the task.|

Priority is calculated according to the following data lookup rules:

|Impact|Urgency|Priority|
|------|-------|--------|
|1 - High|1 - High|1 - Critical|
|1 - High|2 - Medium|2 - High|
|1 - High|3 - Low|3 - Moderate|
|2 - Medium|1 - High|2 - High|
|2 - Medium|2 - Medium|3 - Moderate|
|2 - Medium|3 - Low|4 - Low|
|3 - Low|1 - High|3 - Moderate|
|3 - Low|2 - Medium|4 - Low|
|3 - Low|3 - Low|5 - Planning|

By default, the **Priority** field is read-only and must be set by selecting the **Impact** and **Urgency** values. To change how the priority is calculated, you can either alter the priority lookup rules or disable the **Priority is managed by Data Lookup - set as read-only** UI policy and create their own business logic.

In the Problem Priority Data Lookup \[dl\_problem\_priority\] table, you can modify the data lookup rules for the task priority.

## Work notes for problem priorities

When you initially create and save a problem, the **Work notes** field is not mandatory. If you change the priority of the problem by selecting different **Impact** or **Urgency** values on a problem form that was saved, the **Work notes** field becomes mandatory.

**Note:** This feature is available only in new instances starting with Jakarta or a later release. The Problem Management Best Practice – Jakarta plugin \(com.snc.best\_practice.problem.jakarta\) plugin must be activated.

**Parent Topic:**[Reference section for Problem Management](reference-section-for-problem-management.md)


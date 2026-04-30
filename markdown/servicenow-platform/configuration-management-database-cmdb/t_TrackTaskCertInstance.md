---
title: Track a task with a certification instance
description: The Certification Tasks related list on the certification instance record provides information about associated tasks.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data certification performance, Data Certification on Core UI, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Track a task with a certification instance

The Certification Tasks related list on the certification instance record provides information about associated tasks.

## Before you begin

Role required: admin

## About this task

The State field on the certification instance record is read-only and is based on the cumulative states of the certification tasks associated with the instance. The Percent complete column allows users with the certification\_admin role to track task progress quickly. For more information, see [Track Certification Tasks](t_TrackACertificationTask.md).

To track a certification instance:

## Procedure

1.  Navigate to **All** &gt; **Data Certification** &gt; **Schedules** &gt; **Instances**.

2.  Click a certification instance Number.

3.  View and edit the following fields as necessary.

    |Field|Description|
    |-----|-----------|
    |Number|\[Read-only\] Automatically generated identification number for the instance.|
    |Certification Schedule|The [certification schedule](../concept/c_PlanningDataCertification.md) used to create the certification instance.|
    |State|\[Read-only\] Current state of the certification instance: Work in Progress, Complete, Closed Incomplete, or Cancelled. For more information, see [Track Certification Tasks](t_TrackACertificationTask.md).|
    |Created|\[Read-only\] Date and time the certification instance was created. Date is filled in automatically when the Execute Now button clicks the associated certification schedule.|
    |Complete by|\[Required\] Date and time when the certification instance must be completed. The system updates this field when it executes the schedule, using the deadline specified on the instance. All certification tasks associated with the certification instance must be marked Complete, Closed Incomplete, or Cancelled before the instance is complete.|
    |Percent complete|Percentage of the instance that has reached the Closed Complete state. This field is automatically filled in based on the Percent Complete fields on the associated certification tasks.|
    |Task Description|Information about the certification instance. This field automatically displays the text from the Task description field of the associated certification schedule.|
    |Instructions|Field for providing instructions to the user or group performing the certification. This field is automatically filled in with information from the Instructions field on the associated certification schedule.|



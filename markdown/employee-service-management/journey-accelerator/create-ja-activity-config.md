---
title: Create an Employee Center activity configuration
description: Create or modify an activity configuration to define how the Employee Center handles application links in My active items.
locale: en-US
release: australia
product: Journey Accelerator
classification: journey-accelerator
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Add a Journey Accelerator action plan link to My Active Items list, Configure action plan access in the Employee Center, Configure, Journey Accelerator, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Create an Employee Center activity configuration

Create or modify an activity configuration to define how the Employee Center handles application links in My active items.

## Before you begin

Use the application picker to set the appropriate scope. Employee Center. See, Application picker

The name of the activity to configure. Use the name of the activity created in the [Add a Journey Accelerator action plan link to My Active Items list](add-ja-action-plan-myitems-list.md) task example `Action plan items`.

Role required: admin

## About this task

Activity configurations enable administrators to control the actions of links associated with applications and features. For more information about activity configuration:

-   [Activity Configuration form](../../employee-center/reference/ec-activity-configuration-form.md)
-   [Activity Configuration Detail form](../../employee-center/reference/activity-configuration-detail-form.md)

The scope of an activity configuration is associated with an application. Availability of fields in an activity form depends on the selected application. This task starts in the Employee Center application and creates conditional filters applied to the Journey Accelerator application.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Activity Configuration**, and click the activity you want to configure.

    **Note:** Set the Activity picker to Employee Center to start this task.

2.  Click **New** on the **Activity Configuration Details** tab.

3.  To change the scope, set the Activity picker to **Journey Accelerator** \[sn\_ja\_plan\].

4.  Create filter conditions and or clauses that determine a user's visibility of action plans listed in the Journey Accelerator Plan \[sn\_ja\_plan\] table.

    These conditions control what each user can access from Employee Center action plan links.

    |Conditions|Boolean Operator|
    |----------|----------------|
    |Active|is|true|AND/OR|
    |Manager|is \(dynamic\)|Me|AND/OR|
    |Mentors can edit|is \(dynamic\)|Me|or|
    |Mentors can view|is \(dynamic\)|Me|or|

    |Conditions|Boolean Operator|
    |----------|----------------|
    |Active|is|true|AND/OR|
    |Employee|is \(dynamic\)|Me|AND/OR|
    |State|is not|Draft|AND/OR|

5.  Click **Submit**



---
title: Configure a lifecycle event
description: Build a lifecycle event and its associated activity sets and activities with the lifecycle event builder.
locale: en-US
release: zurich
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Building a lifecycle event, Use, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Configure a lifecycle event

Build a lifecycle event and its associated activity sets and activities with the lifecycle event builder.

## Before you begin

Role required: sn\_hr\_le.admin or sn\_hr\_le.activity\_set\_manager

Begin by defining the event type, such as new hire onboarding. Each lifecycle event has one or more activity sets, which represent different stages in the lifecycle event process. And each activity set has one or more activities, which can be requests for approvals, tasks for employees, activities for fulfillers, or the sending of notifications.

## Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Administration** &gt; **Manage Lifecycle Events**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form.

<table id="table_ich_2rq_42b"><thead><tr><th>

Field

</th><th colspan="2">

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td colspan="2">

Name of the lifecycle event.

</td></tr><tr><td>

Active

</td><td colspan="2">

Option to activate the lifecycle event for use.

</td></tr><tr><td>

Description

</td><td colspan="2">

Description of the lifecycle event.

</td></tr><tr><td>

Display activity sets to subject person

</td><td colspan="2">

\(Employee Center only\) Option to show the activity sets timeline on the HR ticket page to the subject person of the lifecycle event case. This is a two-part process. In addition to selecting the box here, you must also select **Show case to subject person** for the HR service that the lifecycle event is associated with. To select the latter, see [Configure an HR service](configure-hr-service.md).**Note:**

-   If **Show case to subject person** for the corresponding HR service is not selected, then the activity sets timeline will not display for the subject person.
-   The progress bar for each activity set does not appear for the subject person. It only appears for the opened for person.
-   The HR ticket page is where users can view the details of an HR case in the Employee Service Center. See  for more information.


</td></tr><tr><td>

In the employee view, sort activities by

</td><td colspan="2">

You can choose how your employees view activities in the lifecycle event.-   Due date: Show activities in chronological order with tasks that are due earlier at the top and other activities in by creation date.
-   Display order: Show activities in the order they appear in an activity set.
 **Note:** What you select in this field is also reflected on the Employee Center for a user's to-dos.

</td></tr><tr><td rowspan="5">

Event type

</td><td colspan="2">

Event type of the lifecycle event. Select one of the following:

</td></tr><tr><td>

Onboarding

</td><td>

Lifecycle event to use with mobile onboarding.**Note:** You must also make sure that the **Display activity sets to subject person** option on the lifecycle event form and the **Show case to subject person** option on the corresponding HR service form are selected. See [Select a Lifecycle Event for Now Mobile](select-lifecycle-event-for-mobile-onboarding.md) for more information.

</td></tr><tr><td>

Offboarding

</td><td>

 

</td></tr><tr><td>

Transitions

</td><td>

 

</td></tr><tr><td>

HR Services

</td><td>

 

</td></tr></tbody>
</table>4.  Click the **Activity Sets** tab or **Next** to configure the activity sets and activities for the lifecycle event.

    You can create new or modify existing activity sets and activities. For further details on the form fields, see:

    -   [Configure a lifecycle event activity set](configure-hr-lifecycle-event-activity-set.md)
    -   [Configure a lifecycle event activity](configure-hr-lifecycle-event-activity.md#)
5.  Click **Submit** or **Update**.


-   **[Configure a lifecycle event activity set](configure-hr-lifecycle-event-activity-set.md)**  
Create or modify a lifecycle event activity set to define a container for a group of activities.
-   **[Lifecycle Events evaluation interval](../concept/le-evaluation-interval1.md)**  
There is a mechanism available to ensure timers within a workflow trigger automatically rather than wait for the evaluation interval to trigger.
-   **[Configure a lifecycle event activity](configure-hr-lifecycle-event-activity.md#)**  
Create or modify a lifecycle event activity. Lifecycle Events activities can be approvals, employee tasks, fulfiller activities, notifications, flows, content, or activity containers.
-   **[Configure the rescind process for a lifecycle event](configure-rescind-for-a-lifecycle-event.md)**  
Cancel and revert work done in a lifecycle event case with the rescind process. Rescind activities can be defined to notify employees and departments when a case is rescinded, trigger automated flows, and revert work already completed, such as the provisioning of equipment or the setting up of a workplace.

**Parent Topic:**[Building a lifecycle event](../concept/hr-lifecycle-event-configuration.md)

**Previous topic:**[Configure a schedule content template for a lifecycle event activity](configure-schedule-content-template-for-lifecycle-event.md)

**Next topic:**[Configure a lifecycle event activity set](configure-hr-lifecycle-event-activity-set.md)


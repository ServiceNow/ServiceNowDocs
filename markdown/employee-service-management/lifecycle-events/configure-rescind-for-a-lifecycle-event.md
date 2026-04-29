---
title: Configure the rescind process for a lifecycle event
description: Cancel and revert work done in a lifecycle event case with the rescind process. Rescind activities can be defined to notify employees and departments when a case is rescinded, trigger automated flows, and revert work already completed, such as the provisioning of equipment or the setting up of a workplace.
locale: en-US
release: australia
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure a lifecycle event, Building a lifecycle event, Using Lifecycle Events, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Configure the rescind process for a lifecycle event

Cancel and revert work done in a lifecycle event case with the rescind process. Rescind activities can be defined to notify employees and departments when a case is rescinded, trigger automated flows, and revert work already completed, such as the provisioning of equipment or the setting up of a workplace.

## Before you begin

Role required: sn\_hr\_le.admin or sn\_hr\_le.activity\_set\_manager

## About this task

The rescind process enables you to cancel and revert work done in a lifecycle event case. For example, if a new hire decides not to join the company or a job offer is revoked, you can revert work done in the onboarding case.

## Procedure

1.  Enable the rescind activity set.

    1.  Navigate to **Lifecycle Events** &gt; **Administration** &gt; **Manage Lifecycle Events**, and open a lifecycle event record.

    2.  Click the **Activity Sets** tab.

    3.  Click **Enable Rescind**.

        The rescind activity set displays on the right-hand side of the lifecycle event builder.

        **Note:** You cannot set an audience for activity sets that have a trigger type of **Rescind**.

2.  Add one or more rescind activities.

    1.  Click **Add** to add a rescind activity to the rescind activity set.

    2.  Fill in the fields on the form.

<table id="table_tk3_mn2_jlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the rescind activity.

</td></tr><tr><td>

Description

</td><td>

Description of the rescind activity.

</td></tr><tr><td>

Activity to rescind

</td><td>

Name of the activity to rescind. You can select any activity that is associated with the same lifecycle event type, with the exception of activity containers \(you can select member activities\) and other rescind activities.

</td></tr><tr><td>

Activity type

</td><td>

Activity type of the rescind activity. Select one of the following activity types:-   [Approval](configure-hr-lifecycle-event-activity.md#)
-   [Employee activity](configure-hr-lifecycle-event-activity.md#)
-   [Fulfiller activity](configure-hr-lifecycle-event-activity.md#)
-   [Notification](configure-hr-lifecycle-event-activity.md#)
-   [Flow](configure-hr-lifecycle-event-activity.md#)
-   [Content](configure-hr-lifecycle-event-activity.md#)
-   [Activity container](configure-hr-lifecycle-event-activity.md#)

**Note:** For this activity type, there is no **Activity to rescind** field at the container level. When configuring the rescind member activities, you can select the corresponding activity to rescind at the member activity level.

</td></tr><tr><td>

Active

</td><td>

Option to activate the rescind activity for use.

</td></tr><tr><td>

Owning group

</td><td>

Owning group that the rescind activity is associated with.

</td></tr><tr><td>

Audience

</td><td>

Defines whether the activity should trigger for the lifecycle event case. You can apply one or more audience records. The subject person of the lifecycle event case must meet the conditions or criteria of all audience records for the activity to trigger in the case. If no audience record is selected, then the activity will always trigger for the case.**Important:** The rescind activity automatically inherits the audience of the underlying activity to rescind. If you clear or update the activity to rescind, the audience is also automatically cleared or updated.

</td></tr></tbody>
</table>    3.  Repeat the process as needed.


**Parent Topic:**[Configure a lifecycle event](configure-hr-lifecycle-event-type.md)


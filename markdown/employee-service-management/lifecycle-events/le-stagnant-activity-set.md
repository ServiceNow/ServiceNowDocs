---
title: Lifecycle Events activity set progress optimization
description: Ensure that the activity sets you have defined for Lifecycle Events progress seamlessly through completion when they meet the conditions to be triggered for a Lifecycle Events case.
locale: en-US
release: zurich
product: Lifecycle Events
classification: lifecycle-events
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure a Lifecycle Events trigger for activity sets, Lifecycle Events evaluation interval, Configure a lifecycle event, Building a lifecycle event, Use, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Lifecycle Events activity set progress optimization

Ensure that the activity sets you have defined for Lifecycle Events progress seamlessly through completion when they meet the conditions to be triggered for a Lifecycle Events case.

Activity sets are created or modified to define a group of activities. Activity sets represent different stages in the life cycle event process and have conditions under which they’re triggered. The trigger conditions for an activity set depend on the values defined in the **Trigger type** and **Audience** fields in the Activity Set record. When an activity set is created, the **State** field in the corresponding Activity Set Context record is set to **Awaiting Trigger**. Once an activity set meets the trigger conditions that are defined for it, the value in the **State** field is changed to **Running Activities**.

Occasionally, issues that impede progress for activity sets may surface although the corresponding trigger conditions have been met. To optimize progression for the activity sets you have defined and that are active, it’s important to understand the conditions under which an activity set becomes stagnant. Use the following table to acquire information about the issues attributed to the stagnation of an activity set's progress and the corresponding solutions for the issues reflected:

<table id="table_r4z_gp3_n2c"><thead><tr><th>

Issue

</th><th>

Description

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

Configuration changes

</td><td>

Activity set configuration changes performed while you have existing Lifecycle Events cases that are dependent on a previous activity set configuration.

</td><td>

You must use caution when changing the configuration of an activity set that is defined and active, specifically the following components:-   Changing the **Audience** field value in the Activity Set record.
-   Changing the **Trigger type** field value in the Activity Set record.
-   Adding new activities to an activity set.
-   Moving activities between activity sets.

Existing Lifecycle Events cases don't use the configuration changes you made to an activity set when any of the following conditions are true:

-   The activity set has triggered for the Lifecycle Events case.
-   Activities have already generated for the Lifecycle Events case.
-   Activities have already completed for the Lifecycle Events case.

These configuration changes should be performed in a non-production instance to validate whether the changes produce any adverse effects.

**Tip:** If an activity set becomes stagnant due to a configuration change, you can perform the following steps to resume progress:

1.  Change the **State** field in the Activity Set Context record to **Error**.
2.  Resume the corresponding Lifecycle Events case.

This solution is a workaround and doesn't exemplify the use for which the resume case functionality is intended. To use this workaround, the following conditions must be true:

-   The activities associated with the activity set must not have been completed.
-   The tasks associated with the Lifecycle Events case must not have been created.

This workaround should be performed in a non-production instance to validate whether the changes produce the desired effects.

</td></tr><tr><td>

Misconfiguration

</td><td>

An erroneous activity set configuration that causes unintended behavior and adversely affects the progression of activities within an activity set.

</td><td>

Review the activity sets you have defined to confirm whether they’re correctly configured. For example, you defined a new activity set, activity set 2 \(AS2\), and set the **Trigger type** field to **Other Activity Sets** so that AS2 is triggered after the completion of activity set 1 \(AS1\). However, if AS1 is deactivated, your configuration for AS2 becomes invalid. Since AS1 is deactivated,the configuration for AS2 must be changed to remove its dependency from AS1.

</td></tr><tr><td>

Customization

</td><td>

Issues associated with custom Lifecycle Events workflows or their related script includes that are used to manage and run activities.

</td><td>

Confirm whether there are any restricted caller access \(RCA\) records that have become invalidated from modifying a script include. If there are invalid RCA records related to a modified script include, review each record and allow access accordingly.Also, confirm whether there are any RCA records with an error regarding the inability to call or access a script include, like hr\_ActivitySet.

</td></tr><tr><td>

Evaluation interval

</td><td>

Reducing the interval of time that must transpire between each cycle of the activity set evaluation process. The activity set evaluation process determines whether activity sets with the **State** field set to **Awaiting Trigger** in the corresponding Activity Set Context record meet the trigger conditions that are defined for them.

</td><td>

Use caution if you decide to reduce the time interval between each cycle of the activity set evaluation process to less than the default value \(four hours\).Reducing the wait time between each cycle of the activity set evaluation process increases the frequency at which the activity set evaluation process runs. Consequently, this modification increases the number of workflow activities that run simultaneously. If the number of activities running reaches the capacity of activities that can be processed by the workflow, the workflow is canceled during its next attempt to run.

Review the Workflow contexts table to confirm whether there are any records associated with a Lifecycle Events workflow that have been canceled. The **State** field in the corresponding Workflow context record is set to **Canceled** for workflows that have been canceled.

**Tip:** Use the [Condition with Event BR \(Demo\) activity set](le-evaluation-interval1.md#section_gd5_1wz_nsb) in lieu of modifying the evaluation interval. See [Lifecycle Events evaluation interval](le-evaluation-interval1.md) for more information about the evaluation interval and the Condition with Event BR \(Demo\) activity set.

</td></tr><tr><td>

Audience criteria

</td><td>

The subject person doesn't meet the audience criteria defined for an activity that is intended for a target audience. The corresponding activity set is skipped during the evaluation process.

</td><td>

Review the Activity Set Contexts table to confirm whether there are any records that have been skipped. The **State** field in the corresponding Activity Set Context record is set to **Skipped** for activity sets that have been skipped.

</td></tr></tbody>
</table>**Parent Topic:**[Configure a Lifecycle Events trigger for activity sets](../task/le-config-event-trigger.md)


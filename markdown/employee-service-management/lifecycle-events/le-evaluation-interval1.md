---
title: Lifecycle Events evaluation interval
description: There is a mechanism available to ensure timers within a workflow trigger automatically rather than wait for the evaluation interval to trigger.
locale: en-US
release: xanadu
product: Lifecycle Events
classification: lifecycle-events
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configure a lifecycle event, Building a lifecycle event, Lifecycle Events, HR Service Delivery, Employee Service Management]
---

# Lifecycle Events evaluation interval

There is a mechanism available to ensure timers within a workflow trigger automatically rather than wait for the evaluation interval to trigger.

Activity sets can be triggered using different methods based on how you configure it:

-   Immediately
-   By a date
-   Trigger script \(advanced\)
-   Conditions \(fields from a table\)
-   Combination or different trigger types
-   \*Other activity sets

    **Note:** For more information on activity set triggering, see [Configure a lifecycle event activity set](../task/configure-hr-lifecycle-event-activity-set.md) and [Lifecycle Events workflows](LEWorkflow.md).


\*When an activity set is triggered by other activity sets it must wait for all dependencies to resolve before triggering.

## HR Activity launcher flow

When a lifecycle event case is changed to the Ready state, all activity sets run through the HR Activity Launcher flow. The activities in each activity set are not triggered at this time. When an activity set is not dependent on other activity sets to trigger activities, the trigger conditions are analyzed.

If the trigger condition has not been met, it waits for the Wait to reevaluate Trigger Script timer to run \(default is every four hours\).

If the trigger condition is met, but after the evaluation interval runs, it has to wait another four hours before the activities set is re-evaluated. This can cause delays in an activity set to trigger.

The Wait to reevaluate Trigger Script timer uses the **sn\_hr\_le.All activity set closure timer** field under Lifecycle Event Properties to determine when to evaluate the activity set. The default value is four hours.

You can reduce the value in the **sn\_hr\_le.All activity set closure timer** field in order to launch the activity set sooner.

**Note:** Use caution if you decide to change the default value. Frequent updates trigger more events and can cause your lifecycle event activity sets to cancel before it can complete. For more information, see [Lifecycle event properties](../task/lifecycle-event-properties-page.md).

![HR Activity Launcher](../image/activity_launcher.png)

## Condition with Event BR \(Demo\) activity set

An alternative to using the **Evaluation interval** field is to use the **Condition with Event BR \(Demo\)** activity set that is included with demo data as an example of what you can use. This is an optional solution, but you can create and use server-side code \(business rule, event script, scheduled job, etc.\) that triggers the check\_activity\_set\_trigger event into the HR Activity Set Trigger Check workflow. Any activity set can be triggered using the check\_activity\_set\_trigger event from the server side with the exception of activity sets that are triggered immediately or only by other activity sets.

**Note:** To access the **Condition with Event BR \(Demo\)** activity set, activate the Human Resources Scoped App: Lifecycle Events for Enterprise \(com.sn\_hr\_lifecycle\_ent\) plugin. This is an optional method that can be used instead of the values in the **Evaluation interval** field.

-   The trigger type for the activity set must be set to **Condition**.
-   The **Condition with Event BR \(Demo\)** activity set triggers when the state of primary lifecycle event case moves to **Work in progress**.
-   The **Email - Condition with Event BR \(Demo\)** activity is included with the **Condition with Event BR \(Demo\)** activity set.
-   The **Condition with Event BR \(Demo\)** activity set contains the **HR Activity Launcher** workflow. It also contains the **Condition with Event BR \(Demo\)** business rule.
    -   The **Condition with Event BR \(Demo\)** business rule runs after the state of an LE case changes to **Work in Progress**.
    -   It then looks for the workflows that are running for the LE case until it finds the HR Activity Set Trigger Check workflow and broadcasts the check\_activity\_set\_trigger event to that workflow.
-   You can modify the **Condition with Event BR \(Demo\)** activity set, **Email - Condition with Event BR \(Demo\)** activity, and **Condition with Event BR \(Demo\)** business rule to fit your requirements.

    **Note:** For more information, see [Lifecycle Events workflows](LEWorkflow.md) and [Business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).


## HR Activity Set Trigger Check workflow

The HR Activity Set Trigger Check workflow \(see below\) was added to the HR Activity Launcher workflow so that any server-side script can notify the workflow to see if the activity set is ready to trigger.

**Note:** It does not trigger the activity, it evaluates the condition of the activity set.

![HR Activity Launcher with HR Activity Set Trigger Check](../image/activity_launcher_sd.png) ![HR Activity Set Trigger Check workflow](../image/HR_activity_set_trigger_set.png)

-   The HR Activity Set Trigger Check workflow is called when an activity set is not dependent on other activity sets.
-   It periodically checks if the trigger condition for an activity set has been met.
-   If the trigger conditions have not been met, it still waits for the evaluation interval to run.
-   If the check\_activity\_set\_trigger event fires, the Activity set trigger conditions are checked immediately.

-   **[View and use the Condition with Event BR \(Demo\) activity set](../task/le-evaluation-interval-process.md)**  
You can trigger activity sets using an event that is included in the Condition with Event BR \(Demo\) activity set or you can create and use server-side code \(business rule, event script, scheduled job, etc.\) that triggers the check\_activity\_set\_trigger event into the HR Activity Set Trigger Check workflow.
-   **[View and use the Condition with Event BR \(Demo\) business rule](../task/le-eval-interval-business-rule.md)**  
You can view and use the Condition with Event BR \(Demo\) business rule to trigger an evaluation of your activity set faster.
-   **[Change the evaluation interval default wait time](../task/le-activity-set-evaluation-interval.md)**  
As an administrator, you can change the default time that an activity set waits before the activity set is evaluated.
-   **[Configure a Lifecycle Events trigger for activity sets](../task/le-config-event-trigger.md)**  
Create triggers for activity sets in Lifecycle Events.
-   **[Lifecycle Events triggers and workflow reference](../reference/le-eval-interval-trigger-workflow-info.md)**  
Information about Lifecycle Events triggers and workflow.

**Parent Topic:**[Configure a lifecycle event](../task/configure-hr-lifecycle-event-type.md)


---
title: Lifecycle Events triggers and workflow reference
description: Information about Lifecycle Events triggers and workflow.
locale: en-US
release: zurich
product: Lifecycle Events
classification: lifecycle-events
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Lifecycle Events evaluation interval, Configure a lifecycle event, Building a lifecycle event, Use, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Lifecycle Events triggers and workflow reference

Information about Lifecycle Events triggers and workflow.

## HR Activity launcher flow

When a lifecycle event case is changed to the Ready state, all activity sets run through the HR Activity Launcher flow. The activities in each activity set aren’t triggered. When an activity set isn’t dependent on other activity sets to trigger activities, the trigger conditions are analyzed.

If the trigger condition hasn’t been met, it waits for the Wait to reevaluate the Trigger Script timer to run \(default is every four hours\).

If the trigger condition is met, but after the evaluation interval runs, it has to wait another four hours before the activities set is reevaluated. Waiting for reevaluation can cause delays in an activity set to trigger.

The Wait to reevaluate Trigger Script timer uses the **evaluation\_interval** in the **sn\_hr\_le\_activity\_set** table. The default value is four hours. You can reduce the value in the **evaluation\_interval** field to launch the activity set sooner, see [Change the evaluation interval default wait time](../task/le-activity-set-evaluation-interval.md).

**Note:** Use caution if you decide to change the default value. Frequent updates trigger more events and can cause your lifecycle event activity sets to cancel before it can complete. For more information, see [Lifecycle event properties](../task/lifecycle-event-properties-page.md).

## Condition with Event BR \(Demo\) activity set

An alternative to using the **Evaluation interval** field to trigger an activity set is to use the **Condition with Event BR \(Demo\)** activity set that is included with the demo data as an example of what you can use. Using the **Condition with Event BR \(Demo\)** is an optional solution, but you can create and use server-side code \(business rule, event script, scheduled job, and the like\) that triggers the check\_activity\_set\_trigger event into the HR Activity Set Trigger Check workflow. Any activity set can be triggered using the check\_activity\_set\_trigger event from the server side except for activity sets that are triggered immediately or only by other activity sets.

**Note:** To access the **Condition with Event BR \(Demo\)** activity set, activate the Human Resources Scoped App: Lifecycle Events for Enterprise \(com.sn\_hr\_lifecycle\_ent\) plugin. This is an optional method that can be used instead of the values in the **Evaluation interval** field.

-   The trigger type for the activity set must be set to **Condition**.
-   The **Condition with Event BR \(Demo\)** activity set triggers when the state of primary lifecycle event case moves to **Work in progress**.
-   The **Email - Condition with Event BR \(Demo\)** activity is included with the **Condition with Event BR \(Demo\)** activity set.
-   The **Condition with Event BR \(Demo\)** activity set includes the **HR Activity Launcher** workflow. It also includes the **Condition with Event BR \(Demo\)** business rule.
    -   The **Condition with Event BR \(Demo\)** business rule runs after the state of an LE case changes to **Work in Progress**.
    -   It then looks for the workflows that are running for the LE case until it finds the HR Activity Set Trigger Check workflow and broadcasts the check\_activity\_set\_trigger event to that workflow.
-   You can change the **Condition with Event BR \(Demo\)** activity set, **Email - Condition with Event BR \(Demo\)** activity, and **Condition with Event BR \(Demo\)** business rule to fit your requirements.

    **Note:** For more information, see [Lifecycle Events workflows](../concept/LEWorkflow.md) and [Business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).


## HR Activity Set Trigger Check workflow

The HR Activity Set Trigger Check workflow was added to the HR Activity Launcher workflow so that any server-side script can notify the workflow to see if the activity set is ready to trigger. The HR Activity Set Trigger Check workflow evaluates conditions. It doesn’t directly trigger any workflows.

-   The HR Activity Set Trigger Check workflow is called when an activity set isn’t dependent on other activity sets.
-   It regularly checks if the trigger condition for an activity set has been met.
-   If the trigger conditions haven’t been met, it still waits for the evaluation interval to run.
-   If the check\_activity\_set\_trigger event fires, the Activity set trigger conditions are checked immediately.

## Check activity set trigger workflow event

Use the **check\_activity\_set\_trigger** workflow event in a server-side script \(business rule, event script, scheduled job, and the like\) to shortcut the Wait to reevaluate the Trigger Script timer and evaluate an activity set's trigger just-in-time. If you’re considering using a more frequent Evaluation interval to avoid a long timer wait, use this option instead.

**Note:** The **check\_activity\_set\_trigger** event doesn’t work with activity sets that are triggered immediately or triggered only by other activity sets.

When preparing to use the **check\_activity\_set\_trigger** workflow event, first determine when the activity set's trigger criteria could be checked. For example, if using a "Condition" trigger type, a business rule with the same condition may be a good place to check if the condition is true. If using an "Advanced" trigger, determine what server-side business logic caused the Advanced script to return true. For example:

-   script include
-   scheduled job
-   import script

.

After you've determined the server-side location to check the trigger criteria, add the following script to it:

```
(function executeRule(current, previous /*null when async*/) {
	var wf = new global.Workflow().getRunningFlows(current);
	while (wf.next()) {
		if (wf.getValue('name') !== 'HR Activity Set Trigger Check')
			continue;
		new global.Workflow().broadcastEvent(wf.sys_id, 'check_activity_set_trigger');
	}
})(current, previous);
```

**Parent Topic:**[Lifecycle Events evaluation interval](../concept/le-evaluation-interval1.md)


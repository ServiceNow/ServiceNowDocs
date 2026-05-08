---
title: Configure a lifecycle event activity set
description: Create or modify a lifecycle event activity set to define a container for a group of activities.
locale: en-US
release: australia
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Configure a lifecycle event, Building a lifecycle event, Using Lifecycle Events, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Configure a lifecycle event activity set

Create or modify a lifecycle event activity set to define a container for a group of activities.

## Before you begin

Role required: sn\_hr\_le.admin or sn\_hr\_le.activity\_set\_manager

Activity sets represent different stages in the lifecycle event process, and you must define when the activity set is triggered, such as immediately upon creation of the lifecycle event case or after the completion of another activity set. Each activity set is associated with a single lifecycle event.

## Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Administration** &gt; **Manage Lifecycle Events**, and open a record.

2.  Click the **Activity Sets** tab to access the lifecycle event builder.

3.  Create a new or modify an existing activity set.

    -   To create a new activity set, click **New Activity Set**.
    -   To modify an existing activity set, hover over the activity set and click **Edit Activity Set**.
4.  Fill in the fields on the form.

<table id="table_qlb_yrq_42b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the lifecycle event activity set.

</td></tr><tr><td>

Display title

</td><td>

Display title of the activity set. The display title is employee-facing only, and appears on the activity sets timeline on the HR ticket page in both portal and mobile. For example, an employee-facing title for the preboarding activity set could be "Get ready for day one." If no display title is provided, the default activity set name will be used instead.

</td></tr><tr><td>

Description

</td><td>

Description of the lifecycle event activity set.

</td></tr><tr><td>

Active

</td><td>

Option to activate the lifecycle event activity set for use.

</td></tr><tr><td>

Display order

</td><td>

Order number for when the activity set appears in the lifecycle event builder and in the activity sets timeline on the HR ticket page.**Note:**

-   The order number has no relation to when the activity set is triggered.
-   If no order number is provided, then the activity set will appear after all of the numbered activity sets.
-   The HR ticket page is where users can view the details of an HR case in the Employee Service Center. See  for more information.


</td></tr><tr><td>

Display to opened for

</td><td>

Option to show or hide the activity set to the opened for person of the lifecycle event case. If selected, the activity set will appear in the activity sets timeline on the HR ticket page in both portal and mobile.**Note:** If not selected, the activity set will not appear in the activity sets timeline. Any associated to-dos assigned to the opened for and subject person will still appear on the HR ticket page. However, to-dos that are assigned to anyone else will be hidden.

</td></tr><tr><td>

Display to subject person

</td><td>

Option to show or hide the activity set to the subject person of the lifecycle event case. If selected, the activity set will appear in the activity sets timeline on the HR ticket page in both portal and mobile. This is a three-part process. In addition to selecting the check box here, you must also:-   Select **Display activity sets to the subject person** for the lifecycle event type. See [Configure a lifecycle event](configure-hr-lifecycle-event-type.md) for more information.
-   Select **Show case to subject person** for the HR service that the lifecycle event is associated with. See [Configure an HR service](configure-hr-service.md) for more information.
 **Note:** If not selected, the activity set will not appear in the activity sets timeline. Any associated to-dos assigned to the subject person will still appear on the HR ticket page. However, to-dos that are not assigned to the subject person will be hidden.

</td></tr><tr><td>

Audience

</td><td>

The specific audience the activity set targets. Setting an audience for an activity set allows you to create activities within an activity set for a specific group of people. If the audience field is empty, the activity set applies to all employees.You can also use audience as a filter when using the Test Activity Sets tool. For more information, see [Using the Test Activity Sets tool for a lifecycle event activity set](../concept/hr-lifecycle-event-test-tool.md).

 **Note:** You can also define an audience at the activity level. The audience criteria for an activity set overrides the audience criteria for an activity.

</td></tr></tbody>
</table>5.  In the **Activity Set Trigger Condition** section, set the trigger condition for the activity set.

<table id="table_pzv_wnd_cgb"><thead><tr><th>

Trigger condition

</th><th colspan="2">

Description

</th></tr></thead><tbody><tr><td>

Immediate

</td><td colspan="2">

Activity set triggers upon creation of the lifecycle event case.

</td></tr><tr><td rowspan="7">

Date

</td><td colspan="2">

Activity set triggers before, on, or after the specified date.**Note:** If the date for the activity set is updated, then the change will apply only to open HR cases with active activity sets that have not yet triggered.

</td></tr><tr><td>

Trigger table

</td><td>

Select an HR case or profile table.

</td></tr><tr><td>

Trigger field

</td><td>

Select a date field.

</td></tr><tr><td>

Ignore empty date

</td><td>

Option to not trigger the activity set when the date field is empty. If selected, the activity set will not trigger when the date field does not have a value.

</td></tr><tr><td>

Date offset type

</td><td>

Select the date offset type:-   None
-   Before
-   After


</td></tr><tr><td>

Date offset quantity

</td><td>

Provide an offset quantity. This field is available when **Before** or **After** is selected from **Date offset type**.

</td></tr><tr><td>

Date offset units

</td><td>

Provide a unit of measure of days, weeks, or months. This field is available when **Before** or **After** is selected from **Date offset type**.

</td></tr><tr><td rowspan="2">

Other Activity Sets

</td><td colspan="2">

Activity set triggers after the completion of one or more activity sets.

</td></tr><tr><td>

Activity set dependencies

</td><td>

Select one or more activity sets that must complete before the activity set triggers.

</td></tr><tr><td rowspan="2">

Advanced

</td><td colspan="2">

Activity set triggers per the provided script.

</td></tr><tr><td>

Trigger script

</td><td>

Provide a custom script to determine when the activity set triggers.There are two variables in the scripts:

 -   parentCase: Reference to parent lifecycle event case.
-   hrTriggerUtil: Allows checking of other activity sets or dates from other types of triggers.
 The Activity Set Launcher workflow runs every four hours to verify these conditions. See [Lifecycle Events workflows](../concept/LEWorkflow.md).

</td></tr><tr><td rowspan="3">

Condition

</td><td colspan="2">

Activity set triggers per the specified conditions.**Note:** When defining conditions like case sensitivity or null values, see API GlideFilter - Scoped, Global.

</td></tr><tr><td>

Condition table

</td><td>

Select an HR case or HR profile table.

</td></tr><tr><td>

Condition

</td><td>

Use the condition builder to define the conditions that must be met for the activity set to trigger.

</td></tr><tr><td rowspan="5">

Combination

</td><td colspan="2">

Activity set triggers based on a combination of a specified date, other activity sets, and/or conditions.

</td></tr><tr><td>

Combination type

</td><td>

Select when the activity set triggers:-   And: Activity set triggers only when all of the specified triggers are met.
-   Or: Activity set triggers when any of the specified triggers are met.


</td></tr><tr><td>

Date

</td><td>

You can specify a date as part of the combination trigger type.

</td></tr><tr><td>

Other Activity Sets

</td><td>

You can select one or more activity sets that must complete as part of the combination trigger type.

</td></tr><tr><td>

Condition

</td><td>

You can use the condition builder to define the conditions that must be met as part of the combination trigger type.

</td></tr></tbody>
</table>6.  Click **Submit** or **Update**.


## Advanced trigger script

-   Trigger type = advanced.
-   The new hire \(Subject Person\) has an assigned manager.
-   The start date for the new hire has been reached \(cannot be empty\).
-   Two specific activity sets have completed.

```
(function shouldActivitySetTrigger(parentCase /* GlideRecord for parent case */,
							  hrTriggerUtil /* hr_TriggerUtil script include instance */) {

	//Check that employee has a manager
	var employeelocationType = parentCase.subject_person.manager;
	if (gs.nil(employeeLocationType))
		return false;

	//Check that the employees start date is populated and on or before today
	var employeeStartDate = parentCase.subject_person_hr_profile.employment_start_date;
	if (gs.nil(employeeStartDate) || !hrTriggerUtil.checkForElapsedDate(employeeStartDate.getDisplayValue()))
		return false;

	//Check Previous Sets have finished
	var prerequisiteActivitySetIds = ['20f71984ecb61300964fb378c827556f', '58123661dbf2930085ea54c0cf9619ba'];
	if (!hrTriggerUtil.checkActivitySetsCompleted(prerequisiteActivitySetIds))
		return false;

	return true;   

})(parentCase, hrTriggerUtil);
```

Replace the sys\_ids in the example with your activity set sys\_ids. From your activity set, click the **Form Context Menu** icon and select **Copy sys\_id**.

**Parent Topic:**[Configure a lifecycle event](configure-hr-lifecycle-event-type.md)


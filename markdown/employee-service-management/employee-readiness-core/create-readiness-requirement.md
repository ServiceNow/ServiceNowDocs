---
title: Create a health and safety requirement
description: Create requirements to track when employees are ready to return to the workplace or visit a site. You can also create requirements that visitors must complete before entering the workplace.
locale: en-US
release: xanadu
product: Employee Readiness Core
classification: employee-readiness-core
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Employee Health and Safety Status, Employee Readiness Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Create a health and safety requirement

Create requirements to track when employees are ready to return to the workplaceor visit a site. You can also create requirements that visitors must complete before entering the workplace.

## Before you begin

Role required: sn\_imt\_core.admin

## About this task

Use health and safety requirements to define the requirements that employees must fulfill before they can return to the workplace, or that visitors must fulfill before entering the workplace. Create separate requirements for employees and visitors. A requirement must apply to either employees or visitors, not both. Employee Readiness Core provides some [pre-built requirements](../reference/included-health-safety-requirements.md). However, you can create additional requirements using data from any of the Safe Workplace suite or Emergency Response Management apps.

Health and safety requirements are built with [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US). Before creating a requirement, make sure that you're familiar with the basics of ServiceNow® Workflow Studio.

The following steps show how to create a requirement using the pre-built Employee Health Verification Requirement as an example.

## Procedure

1.  In Workflow Studio, create an action to check the requirement status for an employeeor visitor.

    1.  Create an action.

    2.  Save the action in the Employee Readiness Core application.

    3.  In the Inputs section of the Action Outline, create an input for the type of record that you will use to check if the employeeor visitor has fulfilled the requirement.

        For example, to fulfill the Employee Health Verification Requirement, employees must have a health verification record in the Employee Health Verification table \[sn\_imt\_monitoring\_health\_verification\].

        |Label|Name|Type|Mandatory|
        |-----|----|----|---------|
        |Employee Health Verification|health\_verification|Reference.Employee Health Verification \[sn\_imt\_monitoring\_health\_verification\]|Yes|

    4.  Add a **Script Step** to the Action Outline.

    5.  In the **Required Runtime** field, select **Instance**.

    6.  Create an input variable using the input that you created for the action as the value.

        This enables you to use the input for the action in a script.

        |Name|Value|
        |----|-----|
        |health\_verification|**Employee Health Verification** input that you created in the Inputs section.|

    7.  In the **Script** field, add a script to define the conditions when an employee'sor visitor's requirement status is `cleared` or `not_cleared`.

        For the Employee Health Verification Requirement, the requirement is `cleared` for an employee if their health verification response is `yes`, and `not_cleared` for any other response.

        ```
        (function execute(inputs, outputs) {
        	outputs.requirement_status = inputs.health_verification.response == 'yes'
            	? 'cleared'
            	: 'not_cleared';
        })(inputs, outputs);
        ```

    8.  Create an output variable for the requirement status.

        This defines the *requirement\_status* variable that you used in the script.

        |Label|Name|Type|Mandatory|Choice \(Advanced options\)|
        |-----|----|----|---------|---------------------------|
        |requirement\_status|requirement\_status|Choice|Yes|Dropdown with --None--|

    9.  In the Outputs section of the Action Outline, create an output for the requirement status.

        Creating this output enables you to use the *requirement\_status* output variable from the script as an output returned by the action.

        |Label|Name|Type|Mandatory|Choice \(Advanced options\)|
        |-----|----|----|---------|---------------------------|
        |Requirement status|requirement\_status|Choice|No|Dropdown with --None--|

    10. Assign the *requirement\_status* value to the output.

        |Label|Value|
        |-----|-----|
        |Requirement Status|*requirement\_status* output variable from the script step.|

        The action returns the value of the *requirement\_status* for the employeeor visitor \(`cleared` or `not_cleared`\) as an output.

    11. Click **Publish**.

2.  Create a health and safety requirement.

    1.  Navigate to **Employee Health and Safety Status** &gt; **Health and Safety Requirements**.

    2.  Click **New**.

    3.  On the form, fill in the fields.

        The Include previous applicable records section defines a set of records that have already been created but should still trigger the requirement flow. Including previous records ensures that employees or visitorswho complete the requirement before it is activated have their requirement status set to **Cleared**.

<table id="table_wxk_x2n_2mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the requirement. For example, `Employee Health Verification Requirement`.

</td></tr><tr><td>

Requirement for

</td><td>

Who the requirement applies to. The options are **Employee** and **Visitor**. A requirement must apply to either employees or visitors, not both.For example, the Employee Health Verification requirement only applies to employees.

</td></tr><tr><td>

Requirement flow

</td><td>

Leave this field empty. You will return to the requirement record and fill in this field after you create the flow.

</td></tr><tr><td>

Active

</td><td>

This field is read-only. Once you update all fields for the requirement, you can use the **Activate** button to activate the requirement.

</td></tr><tr><td>

Default status

</td><td>

The default status is assigned to health and safety users who don't have any activity towards completing the requirement. The options are **Cleared** and **Not Cleared**.For example, employees who don't have a health verification record are assigned a default status of **Not Cleared** for the Employee Health Verification Requirement.

</td></tr><tr><td>

Use duration

</td><td>

Option to set a time limit that the requirement status is valid for.

</td></tr><tr><td>

Valid for

</td><td>

Time limit that the requirement status is valid for. For example, the Employee Health Verification Requirement status is valid for seven days. Employees must resubmit their health verification weekly to continue fulfilling the requirement.

 This field appears only when the **Use duration** field is selected.

</td></tr><tr><td>

Actionable

</td><td>

Option to add a link for employees to complete the requirement on the Health and Safety Status page.

</td></tr><tr><td>

Action name

</td><td>

The name of the action for the employee to complete the requirement. For example, **Submit self-report**. This name is shown on the Health and Safety Status page.This field appears only when the **Actionable** field is selected.

</td></tr><tr><td>

Action URL

</td><td>

The URL of the Service Catalog item that employees use to complete the requirement. For example, the Employee Health Verification Requirement is completed by submitting the Health Verification form, which has the URL `?id=sc_cat_item&sys_id=9c578864ed111010fa9b395e35885545`.

 This field appears only when the **Actionable** field is selected.

</td></tr><tr><td>

Action visibility

</td><td>

Sets when the link to complete the requirement is displayed on the Health and Safety Status page. Select **Visible when false** to only show the link when the employee hasn't completed the requirement, or select **Always visible** to always show the link.This field appears only when the **Actionable** field is selected.

</td></tr><tr><td>

Exclude

</td><td>

When selected, excludes all users in the **Audience** field from the requirement.

</td></tr><tr><td>

Audience

</td><td>

Select the audience to refine the number of users the requirement applies to. For example, you might want to target all users in an audience that happens to be located in California or target an audience you created specifically for a location, regardless of whether they are users who are traveling, visiting, or working in the location.

 No audience is selected by default and the requirement applies to users based on the rest of the form.

 **Note:** If **Exclude** is checked, the requirement targets all users except those in the audience.

</td></tr><tr><td colspan="2">

Include previous applicable records

</td></tr><tr><td>

Table

</td><td>

Table to look for previously created records that will trigger the requirement flow.For example, the Employee Health Verification Requirement uses the Employee Health Verification table \[sn\_imt\_monitoring\_health\_verification\].

</td></tr><tr><td>

Condition

</td><td>

Add conditions to filter the records from the table that will trigger the flow.

</td></tr></tbody>
</table>    4.  Click **Submit**.

3.  In Workflow Studio, create a flow to update the requirement status for an employeeor visitor.

    1.  Create a new flow.

    2.  Save the flow in the Employee Readiness Core application.

    3.  Add a trigger so that the flow runs whenever the type of record that you're using to check the requirement status is created or updated.

        For example, for the Employee Health Verification Requirement, the flow runs whenever a health verification record is created or updated.

        |Trigger|Table|Condition|Run Trigger|
        |-------|-----|---------|-----------|
        |Created or Updated|Employee Health Verification \[sn\_imt\_monitoring\_health\_verification\]|None.|For each unique change|

    4.  Add the action that you created to the flow.

    5.  Add the record from the trigger as the input.

        For example, for the Employee Health Verification input, add the Employee Health Verification record that was created or updated in the trigger event.

    6.  Add the Update User Requirement action provided in Employee Readiness Core to the flow.

        |User \[User\]|Health and safety requirement \[Health and Safety Requirement\]|Requirement status|Trigger datetime|
        |-------------|---------------------------------------------------------------|------------------|----------------|
        |**Employee** or **User** field from the trigger record. For example, the **Employee** field from the Employee Health Verification record.|Health and safety requirement you created.|`requirement_status` returned by the action that you created.|**Created** field from the trigger record. Only use this input if you set a value for the **Valid for** field on the requirement.|

    7.  Click **Activate**.

4.  Complete the health and safety requirement.

    1.  Navigate to **Employee Health and Safety Status** &gt; **Health and Safety Requirements**.

    2.  Click the requirement that you created earlier.

    3.  In the **Requirement flow** field, add the flow that you created to update the requirement status for employeesor visitors.

    4.  Click **Update**.


## What to do next

When you create the requirement, it's not active by default. You must activate the requirement before you can track whether employeesor visitors have fulfilled the requirement. For instructions, see [Activate a health and safety requirement](activate-readiness-requirement.md).

**Parent Topic:**[Employee Health and Safety Status](../concept/employee-health-safety-status.md)


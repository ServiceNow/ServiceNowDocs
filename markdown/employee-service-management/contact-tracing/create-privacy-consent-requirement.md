---
title: Create a requirement for employees to acknowledge the privacy consent request
description: Create a requirement for your employees to respond to the privacy consent request before entering the workplace to facilitate the use of their data for contact tracing.
locale: en-US
release: xanadu
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Create a requirement for employees to acknowledge the privacy consent request

Create a requirement for your employees to respond to the privacy consent request before entering the workplace to facilitate the use of their data for contact tracing.

## Before you begin

-   Requirements are available in the ServiceNow® Employee Readiness Core application, which must be installed.
-   Privacy Consent requirement is built with ServiceNow® Workflow Studio, so make sure you're familiar with the [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) basics.

Role required: sn\_imt\_core.admin

## About this task

Define the privacy consent requirement for employees to return to work. Employees who agree to the use of their data for contact tracing fulfill the privacy consent requirement and are eligible to return to the workplace. Employees who disagree do not fulfill the privacy consent requirement and are not eligible to return to the workplace. For more information, see [Respond to a request for privacy consent in Contact Tracing](submit-privacy-consent.md#).

**Note:** This procedure describes how to create a requirement using the base system Privacy Consent Requirement as an example.

## Procedure

1.  In Workflow Studio, create an action to add or update the requirement status for an employee who responds to the privacy consent request.

    1.  Create an action and save it in the Employee Readiness Core application.

    2.  In the Inputs section of the Action Outline, create an input for the type of record to use to check whether the employee meets the requirement.

        |Label|Name|Type|Mandatory|
        |-----|----|----|---------|
        |preference|preference|String|Yes|

    3.  Add a **Script Step** to the Action Outline.

    4.  In the **Required Runtime** field, select **Instance**.

    5.  Create an input variable using the input that you created for the action as the value.

        This variable enables you to use the input for the action in a script.

        |Name|Value|
        |----|-----|
        |preference|**preference** input that you created in the Inputs section.|

    6.  In the **Script** field, add a script to define the conditions when an employee's requirement status is `cleared` or `not_cleared`.

        For the Privacy Consent Requirement, the requirement is `not_cleared` for an employee if the employee disagrees to the privacy consent request, and `cleared` if the employee agrees.

        ```
        (function execute(inputs, outputs) {
            if (inputs.preferences == "agree") {
                outputs.requirement_status = "cleared";
            } else if (inputs.preferences == "withdraw_consent") {
                outputs.requirement_status = "not_cleared";
            }
        
        })(inputs, outputs);
        
        ```

    7.  Create an output variable for the requirement status.

        This output variable defines the *requirement\_status* variable that you used in the script.

        |Label|Name|Type|Mandatory|Choice \(Advanced options\)|
        |-----|----|----|---------|---------------------------|
        |requirement\_status|requirement\_status|Choice|Yes|Dropdown with --None--|

    8.  In the Outputs section of the Action Outline, create an output for the requirement status.

        Creating this output enables you to use the *requirement\_status* output variable from the script as an output returned by the action.

        |Label|Name|Type|Mandatory|Choice \(Advanced options\)|
        |-----|----|----|---------|---------------------------|
        |Requirement status|requirement\_status|Choice|No|Dropdown with --None--|

    9.  Assign the *requirement\_status* value to the output.

        |Label|Value|
        |-----|-----|
        |Requirement Status|*requirement\_status* output variable from the script step.|

        The action returns the value of the *requirement\_status* for the employee \(`cleared` or `not_cleared`\) as an output.

    10. Click **Publish**.

2.  Create a privacy consent requirement.

    1.  Navigate to **Employee Health and Safety Status** &gt; **Health and Safety Requirements**.

    2.  Click **New**.

    3.  On the form, fill in the fields.

        The Include previous applicable records section defines a set of records that have already been created but should still trigger the requirement flow. Including previous records ensures that employees who complete the requirement before it is activated have their requirement status set to Cleared.

<table id="table_wxk_x2n_2mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the requirement.

</td></tr><tr><td>

Requirement flow

</td><td>

Flow to update the requirement status for an employee. Leave this field empty. You will return to the requirement record and fill in this field after you create the flow.

</td></tr><tr><td>

Active

</td><td>

This field is read-only. Once you update all fields for the requirement, you can use the **Activate** button to activate the requirement.

</td></tr><tr><td>

Default status

</td><td>

The default status assigned to employees who don't have any activity towards completing the requirement. The options are Cleared and Not Cleared.For example, employees who don't have a record in the User Privacy Notice and Consents \[sn\_imt\_tracing\_user\_privacy\_consent\] table are assigned a default status of Not Cleared for the Privacy Consent Requirement.

</td></tr><tr><td>

Use duration

</td><td>

Option for setting a time limit for the validity of the requirement status.Do not select this field because the employee's status is automatically updated when the employee responds to the privacy consent request.

</td></tr><tr><td colspan="2">

Include previous applicable records

</td></tr><tr><td>

Table

</td><td>

Table to consult for previously created records that will trigger the requirement flow.For example, the Privacy Consent Requirement uses the User Privacy Notice and Consents table.

</td></tr><tr><td>

Condition

</td><td>

Conditions to filter the records from the table that will trigger the flow.

</td></tr></tbody>
</table>    4.  Click **Submit**.

3.  In Workflow Studio, create a flow to update the requirement status for an employee.

    1.  Create a flow and save it in the Employee Readiness Core application.

    2.  Add a trigger so that the flow runs whenever the type of record that you're using to check that the requirement status is created or updated.

        For example, for the Privacy Consent Requirement, the flow runs whenever a user privacy notice and consent record is created or updated.

        |Trigger|Table|Condition|Run Trigger|
        |-------|-----|---------|-----------|
        |Created or Updated|User Privacy Notice and Consents \[sn\_imt\_tracing\_user\_privacy\_consent\]|\[Preferences\] \[changes to\] \[I Agree\] OR \[Preferences\] \[changes to\] \[Withdraw Consent\]|Only if not currently running|

    3.  Add the action that you created to the flow, with the record from the trigger as the input.

        For example, for the preference input, add the User Privacy Notice and Consent record that was created or updated in the trigger event.

    4.  Add the Update User Requirement action provided in Employee Readiness Core to the flow.

        |User \[User\]|Health and safety requirement \[Health and Safety Requirement\]|Requirement status|Trigger datetime|
        |-------------|---------------------------------------------------------------|------------------|----------------|
        |**User** field from the trigger record. For example, the **User** field from the User Privacy Notice and Consent record.|Health and safety requirement you created for the privacy consent.|`requirement_status` returned by the action you created.|Leave the field blank.|

    5.  Click **Activate**.

4.  Complete the health and safety requirement.

    1.  Navigate to **Employee Health and Safety Status** &gt; **Health and Safety Requirements**.

    2.  Open the Privacy Consent Requirement record.

    3.  In the **Requirement flow** field, add the flow that you created to update the requirement status for employees.

    4.  Click **Update**.


## What to do next

You must activate the requirement before you can track whether employees have fulfilled it. For instructions, see [Activate a health and safety requirement](../../employee-readiness-core/task/activate-readiness-requirement.md).

**Parent Topic:**[Setting up Contact Tracing](../concept/set-up-contact-tracing.md)


---
title: Create a requirement for potentially exposed contacts to return to work
description: Create a requirement for potentially exposed employees to meet to verify that they are eligible to return to work.
locale: en-US
release: xanadu
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Create a requirement for potentially exposed contacts to return to work

Create a requirement for potentially exposed employees to meet to verify that they are eligible to return to work.

## Before you begin

-   Health and safety requirements are available in the ServiceNow® Employee Readiness Core application, which must be installed.
-   Health and safety requirements are built with ServiceNow® Workflow Studio, so make sure you're familiar with the [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) basics.

Role required: sn\_imt\_core.admin

## About this task

Define health and safety requirements for employees to return to work. Employees should not be in any potentially exposed contacts investigation of a case. If they are part of an active case investigation, they should meet the requirement of a clear status to be eligible to return to workplace. For more information, see [Follow up with potentially exposed contacts](contact-exposed-contacts.md).

**Note:**

This procedure describes how to create a requirement using the base system Exposed Contacts Requirement as an example.

## Procedure

1.  In Workflow Studio, create an action to add or update the requirement status for an employee added to the potentially exposed contacts list of a case.

    1.  Create an action and save it in the Employee Readiness Core application.

    2.  In the Inputs section of the Action Outline, create an input for the type of record to use to check whether the employee meets the requirement.

        For example, to meet the Exposed Contacts Requirement, employees must have a record in the Exposed Contacts table \[sn\_imt\_tracing\_exposed\_contact\].

        |Label|Name|Type|Mandatory|
        |-----|----|----|---------|
        |Exposed Contact|exposed\_contact|Reference.Exposed Contacts \[sn\_imt\_tracing\_exposed\_contact\]|Yes|

    3.  Add a **Script Step** to the Action Outline.

    4.  In the **Required Runtime** field, select **Instance**.

    5.  Create an input variable using the input that you created for the action as the value.

        This variable enables you to use the input for the action in a script.

        |Name|Value|
        |----|-----|
        |exposed\_contact|**Exposed Contact** input that you created in the Inputs section.|

    6.  In the **Script** field, add a script to define the conditions when an employee's requirement status is `cleared` or `not_cleared`.

        For the Exposed Contacts Requirement, the requirement is `not cleared` for an employee if the health status in any exposed contact records for the employee is `under_investigation` or `infected`, and `cleared` for any other response.

        ```
        (function execute(inputs, outputs) {
          
          outputs.requirement_status = 'cleared'; 
          if (!inputs.exposed_contact.is_primary_exposed_contact) {
            var now_GR = new GlideRecord('sn_imt_tracing_exposed_contact');
            now_GR.addQuery('exposure_case.active',true);
            now_GR.addQuery('is_primary_exposed_contact',true);
            now_GR.addQuery('user',inputs.exposed_contact.user);
            now_GR.setLimit(1);
            now_GR.query();
            if (now_GR.next()) {
            	if(now_GR.status == 'under_investigation' || now_GR.status == 'infected'){    
            		outputs.requirement_status = 'not_cleared';  
          		}else{  	
            		outputs.requirement_status = 'cleared';  
          		}
            }else{
              var gr2 = new GlideRecord('sn_imt_tracing_exposed_contact');
              gr2.addQuery('exposure_case.active',true);
              gr2.addQuery('user',inputs.exposed_contact.user);
              gr2.query(); 
              while(gr2.next()){
                if(gr2.status == 'under_investigation' || gr2.status == 'infected'){    
            		outputs.requirement_status = 'not_cleared';
                    break;
                }
              } 
            }
          }else{
          	if(inputs.exposed_contact.status == 'under_investigation' || inputs.exposed_contact.status == 'infected'){    
            	outputs.requirement_status = 'not_cleared';  
          	}else{  	
            	outputs.requirement_status = 'cleared';  
          	}
          }
        })(inputs, outputs);
        
        ```

    7.  Create an output variable for the requirement status.

        This defines the *requirement\_status* variable that you used in the script.

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

2.  Create an exposed contacts requirement.

    1.  Navigate to **Employee Health and Safety Status** &gt; **Health and Safety Requirements**.

    2.  Click **New**.

    3.  On the form, fill in the fields.

        The Include previous applicable records section defines a set of records that have already been created but should still trigger the requirement flow. Including previous records ensures that employees who complete the requirement before it is activated have their requirement status set to Not Cleared.

<table id="table_wxk_x2n_2mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the requirement. For example, `Exposed Contacts Requirement`.

</td></tr><tr><td>

Requirement flow

</td><td>

Flow to update the requirement status for a potentially exposed employee. Leave this field empty. You will return to the requirement record and fill in this field after you create the flow.

</td></tr><tr><td>

Active

</td><td>

This field is read-only. Once you update all fields for the requirement, you can use the **Activate** button to activate the requirement.

</td></tr><tr><td>

Default status

</td><td>

The default status assigned to employees who are not in the potentially exposed contacts list to meet the health and safety requirement. The options are Cleared and Not Cleared.For example, employees who don't have an exposed contact record are assigned a default status of Not Cleared for the Exposed Contacts Requirement.

</td></tr><tr><td>

Use duration

</td><td>

Option for setting a time limit for the validity of the requirement status.Do not select this field because the employee's status is automatically updated when the status of the exposed contact task for the employee is updated.

</td></tr><tr><td colspan="2">

Include previous applicable records

</td></tr><tr><td>

Table

</td><td>

Table to consult for previously created records that will trigger the requirement flow.For example, the Exposed Contacts Requirement uses the Exposed Contacts table \[sn\_imt\_tracing\_exposed\_contact\].

</td></tr><tr><td>

Condition

</td><td>

Conditions to filter the records from the table that will trigger the flow.

</td></tr></tbody>
</table>    4.  Click **Submit**.

3.  In Workflow Studio, create a flow to update the requirement status for an employee.

    1.  Create a flow and save it in the Employee Readiness Core application.

    2.  Add a trigger so that the flow runs whenever the type of record that you're using to check the requirement status is created or updated.

        For example, for the Exposed Contacts Requirement, the flow runs whenever an exposed contacts record in a case is created or updated.

        |Trigger|Table|Condition|Run Trigger|
        |-------|-----|---------|-----------|
        |Created or Updated|Exposed Contacts \[sn\_imt\_tracing\_exposed\_contact\]|None.|Once|

    3.  Add the action that you created to the flow, with the record from the trigger as the input.

        For example, for the Exposed Contacts input, add the Exposed Contacts record that was created or updated in the trigger event.

    4.  Add the Update User Requirement action provided in Employee Readiness Core to the flow.

        |User \[User\]|Health and safety requirement \[Health and Safety Requirement\]|Requirement status|Trigger datetime|
        |-------------|---------------------------------------------------------------|------------------|----------------|
        |**Employee** or **User** field from the trigger record. For example, the **User** field from the Exposed Contacts record.|Health and safety requirement you created for the potentially exposed contacts.|`requirement_status` returned by the action you created.|Select **Date/Time**.|

    5.  Click **Activate**.

4.  Complete the health and safety requirement.

    1.  Navigate to **Employee Health and Safety Status** &gt; **Health and Safety Requirements**.

    2.  Click the requirement.

    3.  In the **Requirement flow** field, add the flow that you created to update the requirement status for employees.

    4.  Click **Update**.


## What to do next

You must activate the requirement before you can track whether employees have fulfilled it. For instructions, see [Activate a health and safety requirement](../../employee-readiness-core/task/activate-readiness-requirement.md).

**Parent Topic:**[Setting up Contact Tracing](../concept/set-up-contact-tracing.md)


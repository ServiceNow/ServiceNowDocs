---
title: Response scripts
description: Use response scripts to automatically take actions based on user responses to survey questions. Response scripts can be used to create or update records across any of the Emergency Response Management and Safe Workplace suite apps.Emergency Outreach provides the pre-built Request PPE response script.Create a response script to automatically create or update records based on user responses to survey questions.
locale: en-US
release: zurich
product: Emergency Outreach
classification: emergency-outreach
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Emergency Outreach, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Response scripts

Use response scripts to automatically take actions based on user responses to survey questions. Response scripts can be used to create or update records across any of the Emergency Response Management and Safe Workplace suite apps.

Each response script is associated with a survey. The response script runs if a user completes the associated survey and their answers match the response criteria.

**Note:** The [Employee Readiness Surveys](employee-readiness-surveys.md) app must be installed to use response scripts.

**Parent Topic:**[Emergency Outreach](emergency-outreach.md)

## Included response scripts

Emergency Outreach provides the pre-built Request PPE response script.

The Request PPE response script requires the [Workplace PPE Inventory Management](../../ppe-inventory-management/concept/ppe-inventory-management.md) app. This response script creates a PPE request for employees who complete the Employee workplace readiness survey and meet the response criteria for the health status, travel, and ready to return to the workplace questions.

The Request PPE response script is not active by default and must be manually activated. It is ready to activate without any modifications, but you can choose to edit the script to meet your company's needs. To activate the Request PPE response script, navigate to **Emergency Outreach** &gt; **Response Scripts** and click the Request PPE record. Select the **Active** check box, then click **Update**.

If you need to perform additional actions based on survey responses, you can create additional response scripts. Use the included Request PPE response script as an example to help create your own response scripts.

## Create a response script

Create a response script to automatically create or update records based on user responses to survey questions.

### Before you begin

Role required: sn\_imt\_checkin.checkin\_admin

### About this task

Response scripts can be used to create or update records across any of the Emergency Response Management and Safe Workplace suite apps. For example, you could create a response script to reserve a workspace for a user who is ready to return to the workplace.

### Procedure

1.  Navigate to **All** &gt; **Emergency Outreach** &gt; **Response Scripts** and click **New**.

2.  On the form, fill in the fields.

<table id="table_w5l_152_nmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Selected.

</td></tr><tr><td>

Name

</td><td>

Name of the script.

</td></tr><tr><td>

Survey

</td><td>

Survey that causes the script to run.When a survey instance is completed by a user, the script runs if the user's responses to the survey questions match the response criteria.

</td></tr><tr><td>

Script

</td><td>

Script to insert or update a record. The script should perform the following steps.

-   Get the sys\_id for the user who submitted the survey.

    ```
var userSysId = userGr.getUniqueValue();
    ```

**Note:** The `userGr` variable is defined in the Run Response Scripts action. This action is used by the Response Script Actions flow, which runs the response scripts when a user completes a survey and fulfills the response criteria. The `userGr` variable is a user GlideRecord, so you can use it to get additional fields from the user as needed. For example, `userGr.getValue(‘location’)` gets the user's location.

-   If the plugin that installs the table you want to write to is active, insert or update a record for the user.

**Note:** The following code is provided as an example only. You must provide the correct plugin, table, and field names in your script, and make any additional modifications that you require.

    ```
//example code to insert a record
if (GlidePluginManager.isActive('plugin_name')) {
    var now_GR = new GlideRecord('table_name');
    now_GR.initialize();
    now_GR.user_field = userSysId;
    now_GR.field = 'value'; 
    //update additional fields here as needed
    now_GR.insert();
}
    ```

    ```
//example code to update an existing record associated with the user
if (GlidePluginManager.isActive('plugin_name')) {
    var now_GR = new GlideRecord('table_name');
    now_GR.get('user_field', userSysId);
    now_GR.field_to_update = 'value'; 
    //update additional fields here as needed
    now_GR.update();
}
    ```

    ```
//example code to update multiple existing records associated with the user 
if (GlidePluginManager.isActive('plugin_name')) {
    var now_GR = new GlideRecord('table_name');
    now_GR.addQuery('user_field', userSysId);
    now_GR.setValue('field_to_update', 'value');
    //update additional fields here as needed
    now_GR.updateMultiple();
}
    ```

</td></tr></tbody>
</table>3.  Save the response script record using the form context menu.

    The Response Criteria related list is automatically populated with all questions from the associated survey.

4.  Edit the response criteria to define the answers a user must provide for the response script to run.

    1.  Define the required answer in the response criteria for relevant questions.

    2.  Delete the response criteria for any questions that don't require a specific answer.

5.  Click **Update**.



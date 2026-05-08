---
title: Define ServiceNow AI Lens behavior with Lens actions
description: As a Lens admin, you can create Lens actions in ServiceNow AI Lens to customize Lens behavior by providing default instructions, configuring context, and more.Create a Lens action to define custom context, trigger options, and default instructions for the ServiceNow AI Lens execution.Enable customers to scan documents related to car accident on their desktop to auto-fill the Insurance Request form on the ServiceNow instance.Enable compliance analysts to digitize and review several vendor agreements. Instead of manually entering details, they can launch ServiceNow AI Lens directly from the desktop, scan agreements, and adjust extracted values in the preview window before saving.Enable service agents to create user records by extracting specific information from identity documents using ServiceNow AI Lens, directly from the ServiceNow instance.Use ServiceNow AI Lens to map the column headers of an Excel sheet that you specify with ServiceNow table columns and then insert the Excel sheet data into the table.
locale: en-US
release: australia
product: ServiceNow Lens
classification: servicenow-lens
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 22
breadcrumb: [Configure, ServiceNow AI Lens, Enable AI experiences]
---

# Define ServiceNow AI Lens behavior with Lens actions

As a Lens admin, you can create Lens actions in ServiceNow AI Lens to customize Lens behavior by providing default instructions, configuring context, and more.

Use Lens actions to define default instructions, trigger options, custom context, and post processing instructions for the Lens response. With Lens actions, you can achieve the following goals:

-   Trigger ServiceNow AI Lens from a desktop, ServiceNow instance, or Virtual Agent \(from a mobile device or a portal\)
-   Auto-fill a form on the ServiceNow instance
-   View the gathered insights in an editable preview
-   Trigger flows, subflows, or actions after Lens execution
-   Invoke AI agents
-   Run ServiceNow AI Lens as a back-end service
-   Auto-map the column headers of an Excel sheet with the columns of a ServiceNow table, and then insert the Excel sheet data into the ServiceNow table.

Whenever ServiceNow AI Lens is launched from an instance, it checks if any active Lens action is available for the table. If available, it uses the logic defined in Lens action during execution. The Lens action can only be used by the users or groups or roles that are assigned to the Lens Actions record.

Refer to the following examples to understand the different use cases of setting up the Lens actions.

-   [Example: Scan documents to auto-fill the Insurance Request form](servicenow-lens-actions.md#)
-   [Example: Extract structured data from vendor agreements](servicenow-lens-actions.md#)
-   [Example: Auto-fill user records on a user table](servicenow-lens-actions.md#)
-   [Auto-map Excel sheet column headers with ServiceNow table columns](servicenow-lens-actions.md#)

## Customize ServiceNow AI Lens behavior by creating a Lens action

Create a Lens action to define custom context, trigger options, and default instructions for the ServiceNow AI Lens execution.

### Before you begin

Role required: lens\_admin

### About this task

Learn about the various Lens trigger options for ServiceNow AI Lens.

<table id="table_ilf_l3c_yfc"><thead><tr><th>

Goal

</th><th>

Trigger From

</th><th>

Trigger For

</th></tr></thead><tbody><tr><td>

Auto-fill a form with a custom context and default instructions when triggered from the instance.When ServiceNow AI Lens is triggered from the instance in the context of the Lens action, the default instructions are always applied and specific form fields are extracted.

To view the procedure to define default instructions, see [Define default instructions for ServiceNow AI Lens](../task/default-prompt-system-property-lens.md).

</td><td>

Instance

</td><td>

Form

</td></tr><tr><td>

Auto-fill a form with a custom context and default instructions when triggered from the ServiceNow AI Lens desktop app.You can trigger ServiceNow AI Lens from the desktop app directly in context of the Lens action instead of launching Lens from the instance. The default instructions are always applied and specific form fields are extracted.

</td><td>

Desktop

</td><td>

Form

</td></tr><tr><td>

Auto-map the column headers of an Excel sheet with the columns of a specified table, and then insert the Excel sheet data into the table.To view the procedure to auto-map the column headers of an Excel sheet with the columns of a table, and insert Excel data into the table, see [Auto-map Excel sheet column headers with table columns.](servicenow-lens-actions.md#)

</td><td>

Desktop

</td><td>

Excel Mapping

</td></tr><tr><td>

With the help of a client script or server script, run ServiceNow AI Lens as a back-end service.

</td><td>

Instance

</td><td>

Service

</td></tr><tr><td>

View the gathered insights in the preview window of ServiceNow AI Lens by providing custom context and perform post processing steps.

</td><td>

Desktop

</td><td>

Others

</td></tr></tbody>
</table>When ServiceNow AI Lens is triggered from the instance or desktop to auto-fill a form, it uses an active Lens action associated with the target table.

For example, if a user selects **Create with Lens** from Incident table list, ServiceNow AI Lens checks for an active Lens action record for the Incident table where **Trigger From** is set to Instance and **Trigger For** is set to Form. If a matching action record exists, Lens executes in the context of that action.

### Procedure

1.  Navigate to **All** &gt; **ServiceNow AI Lens** &gt; **Lens Actions**.

2.  Select **New**.

3.  Enter a name and description for the Lens action in the Name and Description fields respectively.

4.  In the **Trigger From** field, select one of the following options.

    |Option|Description|
    |------|-----------|
    |**Desktop**|Option to specify that this action must be used when ServiceNow AI Lens is triggered from the ServiceNow AI Lens desktop app.|
    |**Instance**|Option to specify that this action must be used when ServiceNow AI Lens is triggered from a ServiceNow instance.|

5.  To save the changes, right-click the form header and select **Save**.

6.  Set up the Lens action by filling the fields in the Lens Actions form, under the Customize heading.

<table id="table_vjg_bbk_pfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger For

</td><td>

-   **Form** - Lens action is used when ServiceNow AI Lens is triggered to auto-fill a form. Apply a transformation logic to the Lens response before the form is auto-filled by using the [servicenow-lens-actions.md\#transform-response](servicenow-lens-actions.md#transform-response) option.

This option is available when you select **Desktop** or **Instance** from the Trigger From list.

-   **Service** - Lens action is used when ServiceNow AI Lens is used as a service. Select this option to trigger Lens from an instance to auto-populate a **Workspace form**, or to trigger it using Virtual Agent or Script Include.

This option is available when you select **Instance** from the Trigger From list.

-   **Others** - Lens action is used when ServiceNow AI Lens is triggered to display a preview of extracted data and perform post processing steps, if applicable.

This option is available when you select **Desktop** from the Trigger From list.

-   **Excel Mapping** -

Option to specify that you can use this Lens action to attach an Excel sheet and let ServiceNow AI Lens auto-map its column headers with the columns of a table. After the auto-mapping is done, you can view and change the mapping, and insert the Excel sheet data to the table.

This option is available when you select **Desktop** from the Trigger From list.

</td></tr><tr><td>

Order

</td><td>

Execution priority of the Lens action for a given table:-   **1**: Highest priority
-   **999999**: Least priority
The default value is set to 100.

For example, if any user is assigned to two Lens action records for the same table, the Lens action with the least number is used during Lens execution.

</td></tr><tr><td>

Table

</td><td>

Table to which this Lens action applies. Selected table provides context during Lens execution when specific fields are selected or script is provided.For example, Incident table.

</td></tr><tr><td>

Request Context

</td><td>

Option to provide enhanced context during Lens execution by selecting specific fields or providing custom schema via script.-   **Supported Fields** - Selected fields for providing enhanced context for Lens execution.
-   **Advanced** - Script to generate a custom schema object for providing enhanced context for Lens execution.


</td></tr><tr><td>

Fields

</td><td>

Table fields that you can select to provide enhanced context for Lens execution. Select fields to help Lens determine what information to extract from images. Only fields supported by Lens are available for selection. For more information, see [Field types supported](../reference/field-types-supported.md).This field appears only when **Supported Fields** is selected from the **Request Context** choice field.

</td></tr><tr><td>

Pre Processing Script

</td><td>

Script to generate a custom schema object to provide enhanced context for Lens execution. Custom schema help Lens determine what information to extract from images.This field appears only when **Advanced** is selected from the **Request Context** choice field.

Example sample script:

```
function preProcessRequest(lensActionRecord, inputJSON) {
    // Initialize the schema object
    var schemaObj = {};
    /*
    This is a utility method to generate schema object, 
    users can pass tableName and formFields as an array of fields for the given table to generate custom schema that is passed to the LLM.
    
    //Return schemaObj adhering to the structure defined in example
    // tableName = 'incident'
    tableName = inputJSON.tableName; 

    //formFields - array of fields for the given table.
    //formFields = ['short_description', 'comments', 'impact'];
    
    fieldsToProcess = inputJSON.formFields;
    schemaObj = new global.AILensSchemaUtil().generateSchema(tableName, fieldsToProcess);

    */
    return schemaObj;
}
var schemaObj = preProcessRequest(lensActionRecord, inputJSON);
```

Parameters accepted by the `preProcessRequest` method:

-   **lensActionRecord** \(Input\) - GlideRecord of the Lens action that is executed.
-   **inputJSON** \(Input\) - Optional JSON object that users can pass through service APIs.
-   **schemaObj** \(Output\) - Returned JSON object of custom schema.
Example of the returned schemaObj object:

```
schemaObj =  {
  "schemaPayload": {
    "type": "json_schema",
    "json_schema": {
      "name": "schema_extraction",
      "schema": {
        "type": "object",
        "properties": {
          "short_description": {
            "type": "string",
            "label": "Short description"
          },
          "comments": {
            "type": "string",
            "label": "Additional comments"
          },
          "impact": {
            "type": "choice",
            "label": "Impact",
            "choiceValues": ["1", "2", "3"],
            "choiceLabels": {
              "1 - High": "1",
              "2 - Medium": "2",
              "3 - Low": "3"
            }
          }
        },
        "required": [
          "short_description",
          "comments",
          "impact"
        ],
        "additionalProperties": false
      }
    }
  },
  "fieldLabels": ["short_description", "comments", "impact"]  //Optional key
}
```

</td></tr><tr><td>

Default Additional Directions

</td><td>

Default instructions that are supplied to Now Assist in addition to the user-provided instructions.For example, `Summarize this paper by extracting the title, author name, publication date in the dd-mm-yyyy format, abstract, and keywords`

</td></tr><tr><td id="transform-response">

Transform Response

</td><td>

Option to specify the transformation script for transforming the Lens response before auto-filling the form.This field appears only when **Form** is selected from the **Trigger For** choice field.

</td></tr><tr><td>

Transformation Script

</td><td>

Script that transforms the Lens response before populating the form.This field appears only when the **Transform Response** option is selected.

Sample script:

```
function transformResponseScript(lensActionRecord, lensResponse) {
   // Initialize the schema object
    var transformResponse = {};
    
    //Add your code here
    
    //Return schemaObj adhering to the structure defined in example
    return transformResponse;
}
var transformResponse = transformResponseScript(lensActionRecord, lensResponse);
```

Parameters accepted by the `transformResponseScript` method:

-   **lensActionRecord** \(Input\) - GlideRecord of the Lens action that is executed.
-   **lensResponse** \(Input\) - JSON object of the Lens response provided after Lens execution.
-   **transformResponse** \(Output\) - Returned JSON object of transformed schema.
Example of the returned transformResponse object:

```
transformResponse = {
  "short_description": "Service Degradation Error in Order Processing System",
  "description": "The Order Processing API v2.1 encountered a service degradation issue in the Production environment",
  "urgency": "1"
}
```

</td></tr><tr><td>

Enable Post Processing

</td><td>

Option to specify advanced processing instructions after Lens execution is complete.This field appears only when **Others** or **Service** is selected from the **Trigger For** field.

</td></tr><tr><td>

Post Processing Script

</td><td>

Script that is run asynchronously after Lens execution to further process the Lens response, such as triggering a flow, subflow, actions, or AI Agent.This field appears only when the **Enable Post Processing** option is selected.

```
function postProcessResponse(lensActionRecord, lensResponse, lensExecutionRecord) {
    
    //Add your code here

}
postProcessResponse(lensActionRecord, lensResponse, lensExecutionRecord);
```

Parameters accepted by the `postProcessResponse` method:

-   **lensActionRecord** \(Input\) - GlideRecord of the Lens action that is executed.
-   **lensResponse** \(Input\) - JSON object of the Lens response provided after Lens execution.
-   **lensExecutionRecord** \(Input\) - GlideRecord of the Lens execution record.


</td></tr><tr><td>

Wait for processed response

</td><td>

Option to wait for ServiceNow AI Lens to display the output of post-processing on the Preview window. If enabled, it waits for the post processing output. Else, it doesn't wait for post processing output but post processing continues in the background.

</td></tr><tr><td>

Max wait time \(seconds\)

</td><td>

The maximum time ServiceNow AI Lens waits to display the output of post-processing. If the output doesn't appear within this duration, the session times out while the post-processing continues in the background until completion.

</td></tr><tr><td>

Attach Captured Images To Record

</td><td>

Option to attach the captured images to the record that is auto-filled using ServiceNow AI Lens.This option is enabled by default.

</td></tr></tbody>
</table>7.  To assign users or groups or rolesto the Lens action, under the Assigned Users and Groups or Roles heading, select **New**, and then use any one of the following methods.

<table id="choicetable_hnt_fq4_13c"><thead><tr><th align="left" id="d40824e951">

Method

</th><th align="left" id="d40824e954">

Steps

</th></tr></thead><tbody><tr><td id="assign-roles-to-lens-action">

**Assign one or more roles to the Lens action**

</td><td>

Select **Enable Roles** and perform the following steps.1.  Select the Unlock Roles \(![Roles Unlock icon.](../image/lens-lock-icon.png)\) icon.
2.  Select the Look up icon \(![Lookup Roles icon.](../image/lens-magnify-icon.png)\) and then select a role.

Repeat the step to add more roles.

3.  Select the Lock Roles icon \(![Lock Roles icon.](../image/lens-lock-roles-icon.png)\).


</td></tr><tr><td id="assign-users-to-lens-action">

**Assign one or more users to the Lens action**

</td><td>

1.  To assign yourself, select the Add Me icon \(![Add Me icon.](../image/lens-add-me-icon.png)\).
2.  To assign one or more users, select the Unlock Users \(![Roles Lock icon.](../image/lens-lock-icon.png)\) icon.
3.  Select the Look up icon \(![Lookup Roles icon.](../image/lens-magnify-icon.png)\) and then select a user.
4.  Repeat the step to add more users.

5.  Select the Lock Users icon \(![Lock Roles icon.](../image/lens-lock-roles-icon.png)\).


</td></tr><tr><td id="assign-groups-to-lens-action">

**Assign one or more groups to the Lens action**

</td><td>

1.  Select the Unlock Groups \(![Groups Unlock icon.](../image/lens-lock-icon.png)\) icon.
2.  Select the Look up icon \(![Lookup Groups icon.](../image/lens-magnify-icon.png)\) and then select a group.

Repeat the step to add more groups.

3.  Select the Lock Groups icon \(![Lock Roles icon.](../image/lens-lock-roles-icon.png)\).


</td></tr></tbody>
</table>    You can assign any one of the following combinations to the Lens action:

    -   Assign roles to the Lens action.
    -   Assign yourself and one or more groups to the Lens action.
    -   Assign one or more users and groups to the Lens action
8.  Select **Submit**.

    The users or groups, or roles are assigned to the Lens action.

    ![Users, groups, or roles assigned to Lens action](../image/lens-action-form.png "Users, groups, or roles assigned to Lens action")

9.  Select **Update**.

10. Update the assignment of users or groups or roles to the Lens action.

<table id="choicetable_ugv_m32_33c"><thead><tr><th align="left" id="d40824e1164">

Assignment type

</th><th align="left" id="d40824e1167">

Steps

</th></tr></thead><tbody><tr><td id="d40824e1173">

**Roles**

</td><td>

1.  Under the heading **Assigned Users and Groups or Roles**, select the role.
2.  To remove a role, select a role and then select \(![Remove role icon.](../image/lens-file-attch-remove.png)\)
3.  Assign one or more new roles. For more information, see [servicenow-lens-actions.md\#assign-roles-to-lens-action](servicenow-lens-actions.md#assign-roles-to-lens-action)


</td></tr><tr><td id="d40824e1207">

**Users**

</td><td>

1.  Under the heading Assigned Users and Groups or Roles, select the user.
2.  To remove a user, select a user and then select \(![Remove role icon.](../image/lens-file-attch-remove.png)\)
3.  Assign one or more new users. For more information, see [servicenow-lens-actions.md\#assign-users-to-lens-action](servicenow-lens-actions.md#assign-users-to-lens-action)


</td></tr><tr><td id="d40824e1236">

**Groups**

</td><td>

1.  Under the heading Assigned Users and Groups or Roles, select the group.
2.  To remove a group, select a group and then select \(![Remove role icon.](../image/lens-file-attch-remove.png)\)
3.  Assign one or more new groups. For more information, see [servicenow-lens-actions.md\#assign-groups-to-lens-action](servicenow-lens-actions.md#assign-groups-to-lens-action)


</td></tr></tbody>
</table>11. Select **Activate** for activating the Lens action.

    The Lens action will be available on the ServiceNow AI Lens desktop application landing page.


## Example: Scan documents to auto-fill the Insurance Request form

Enable customers to scan documents related to car accident on their desktop to auto-fill the Insurance Request form on the ServiceNow instance.

### Before you begin

Role required: lens\_admin

### About this task

You can define in the Lens action that ServiceNow AI Lens must be triggered from the desktop to auto-fill the Insurance Request form. Lens action includes the fields that must be updated with the extracted data.

![Example Lens action record for auto-filling Insurance request form.](../image/lens-action-insurance-example.png)

### Procedure

1.  Navigate to **All** &gt; **ServiceNow Lens** &gt; **Lens Actions**.

2.  In the **Name** field, enter `Auto-fill Insurance Request from desktop`.

3.  In the **Description** field, enter `Lens action for Boxeo Insurance to auto-fill the Insurance Request form when Lens is triggered from Desktop`.

4.  From the **Trigger From** option, select Desktop.

5.  In the form header, right-click and select **Save**.

6.  From the **Trigger For** option, select Form.

7.  In the **Table** field, select the Insurance Request table.

8.  In the **Request Context** field, select Supported Fields to provide context.

9.  From the **Fields** field, move fields to the Selected list.

    `policy_number, location_of_incident, policy_holder_name, vehicle_number, policy_state, policy_checks_failed, policy_checks_passed, incident_date_time, damage_description, claim_type, claim_evaluation_percentage`

10. In the **Default Additional Directions** field, enter the following directions for the Now Assist.

    ```
    1. Incident Date : If available, extract the date from pictures uploaded.
    2. Personal Information:
    	○ Names: Generate name from images or documents attached. If not present do not hallucinate.
    3. Location:
    	○ If a vehicle number is visible, extract the corresponding city or state from images. If not found in images based on the vehicle number extract U.S city/state and use it as the location.
    	○ If no vehicle number is visible, leave the field blank.
    4. Vehicle Number:
    	○ If present, use the visible vehicle number.
    	○ If not present, extract vehicle number from images like driving license. If not present, leave the field empty.
    5. Policy Checks:
    	○ Refer to the policy checks document for validation.  
    	○ List only passed checks in policyChecksPassed as an HTML table with columns: Check Name, Status, Remarks.
    	○ List only failed checks in policyChecksFailed as an HTML table with columns: Check Name, Status, Remarks. If a document/image is not found for a check then add it to the policyChecksFailed.
    	○ No validation should be skipped. Consider all rules under each policy section and add them into policyChecksPassed or policyChecksFailed based on they status whether they are passed or failed.
    6. Claim Evaluation:
    	○ Calculate the claimEvaluationPercentage using the formula:
    (Number of Passed Checks / Total Number of Checks) * 100
    7. Policy State:
    	○ "Valid" – if Claim Evaluation is 100,
    	○ "Needs More Information" – if Claim Evaluation is greater than 50 and less than 100,
    	○ "Failed" – if Claim Evaluation is less than or equal to 50.
    8. Ensure the final output with all the above fields accurately filled.
    ```

11. Add users or groups who can use this Lens action.

    1.  In the Assigned Users and Groups related list, select **New**.

    2.  Select the required users or group of users that have the lens\_user role.

        Only the assigned users or group of users can leverage the Lens action during Lens execution.

    3.  Select **Submit**.

12. Select **Update**.

13. Select **Activate** for activating the Lens action.


## Example: Extract structured data from vendor agreements

Enable compliance analysts to digitize and review several vendor agreements. Instead of manually entering details, they can launch ServiceNow AI Lens directly from the desktop, scan agreements, and adjust extracted values in the preview window before saving.

### Before you begin

Role required: lens\_admin

### About this task

You can define in the Lens action that ServiceNow AI Lens must be triggered from the desktop to scan the documents saved on the user system. With the post processing option, you can edit the extracted information in the preview window before saving and trigger post processing to create related list records.

### Procedure

1.  Navigate to **All** &gt; **ServiceNow Lens** &gt; **Lens Actions**.

2.  In the **Name** field, enter `Extract data from vendor agreements`.

3.  In the **Description** field, enter `Digitize and review several vendor agreements`.

4.  From the **Trigger From** option, select Desktop.

5.  In the form header, right-click and select **Save**.

6.  From the **Trigger For** option, select Others.

7.  In the **Request Context** field, select Advanced.

8.  In the **Pre Processing Script** field, enter the script to generate custom schema object for providing enhanced context.

    Here is the example of returned custom schema object:

    ```
    schemaObj =  {
      "schemaPayload": {
        "type": "json_schema",
        "json_schema": {
          "name": "schema_extraction",
          "schema": {
            "type": "object",
            "properties": {
              "vendorName": {
                "type": "string",
                "label": "Vendor Name"            
              },
              "contractTitle": {
                "type": "string",
                "label": "Contract Title"
              },
              "contractReferenceNumber": {
                "type": "string",
                "label": "Contract Reference Number"
              },
              "contractStartDate": {
                "type": "string",            
                "label": "Contract Start Date"
              },
              "contractEndDate": {
                "type": "string",
                "label": "Contract End Date"
              },
              "renewalTerminationClauses": {
                "type": "string",
                "label": "Renewal / Termination Clauses"
              }
            },
            "required": [
              "vendorName",
              "contractTitle",
              "contractReferenceNumber",
              "contractStartDate",
              "contractEndDate"
            ],
            "additionalProperties": false
          }
        }
      },
      "fieldLabels": ["vendorName", "contractTitle", "contractReferenceNumber", "contractStartDate", "contractEndDate"]  //Optional key
    }
    ```

9.  In the **Default Additional Directions** field, enter directions for the Now Assist, such as `Leave the fields empty if you do not find the relevant information. Do not hallucinate. Enter the date in the DD-MM-YYYY.`

10. Select the **Enable Post Processing** option.

11. In the **Post Processing Script** field, enter the script to provide the post processing logic for the Lens response after the Lens execution is complete.

    You can provide a post processing logic to pass the data extracted to a subflow for creating related list records.

12. Select the **Wait for processed response** field to enable the ServiceNow AI Lens to wait for ServiceNow AI Lens to display the output of post-processing on the Preview window.

    If enabled, it waits for the post processing output. Else, it doesn't wait for post processing output but post processing continues in the background.

13. In the **Max wait time \(seconds\)** field, specify the maximum time ServiceNow AI Lens waits to display the output of post-processing.

    **Note:** If the output doesn't appear within that duration, the session times out while the post-processing continues in the background until completion.

14. Add users or groups who can use this Lens action.

    1.  In the Assigned Users and Groups related list, select **New**.

    2.  Select the required users or group of users that have the lens\_user role.

        Only the assigned users or group of users can leverage the Lens action during Lens execution.

    3.  Select **Submit**.

15. Select **Update**.

16. Select **Activate** for activating the Lens action.


## Example: Auto-fill user records on a user table

Enable service agents to create user records by extracting specific information from identity documents using ServiceNow AI Lens, directly from the ServiceNow instance.

### Before you begin

Role required: lens\_admin

### About this task

A service agent must onboard multiple users by scanning their official ID cards \(for example, government-issued ID\). Instead of manually entering each user's details, the agents can trigger ServiceNow AI Lens from the instance to automate data extraction and auto-fill specific fields defined in the Lens action record.

You can define in the Lens action that ServiceNow AI Lens must be triggered from the instance to create user records and provide default directions.

### Procedure

1.  Navigate to **All** &gt; **ServiceNow Lens** &gt; **Lens Actions**.

2.  Select **New**.

3.  In the **Name** field, enter `Auto-fill the user records`.

4.  In the **Description** field, enter `Lens action to auto-create the user records on the ServiceNow instance`.

5.  From the **Trigger From** option, select Instance.

6.  In the form header, right-click and select **Save**.

7.  Confirm that the Form option is selected in the **Trigger For** field.

    The Form option is selected by default.

8.  In the **Table** field, select the User \[sys\_user\] table.

9.  Confirm that Supported Fields is selected in the **Request Context** field.

    The Supported Fields value is selected by default, and it provides context.

10. From the **Fields** field, move the fields to the Selected list.

    `userID, first_name, last_name, title, and date_of_birth`

11. In the **Default Additional Directions** field, enter `User ID must always be in lower case and uses the firstname.lastname format. Enter Date of birth in the dd-mm-yyyy format.`

12. Add users or groups who can use this Lens action.

    1.  In the Assigned Users and Groups related list, select **New**.

    2.  Select the required users or group of users that have the lens\_user role.

        Only the assigned users or group of users can leverage the Lens action during Lens execution.

    3.  Select **Submit**.

13. Select **Update**.

14. Select **Activate** for activating the Lens action.


## Auto-map Excel sheet column headers with ServiceNow table columns

Use ServiceNow AI Lens to map the column headers of an Excel sheet that you specify with ServiceNow® table columns and then insert the Excel sheet data into the table.

### Before you begin

Role required: lens\_user

Ensure that the Lens action for this purpose is already defined. To view the steps to define a Lens action, see [Define a Lens action](servicenow-lens-actions.md#). Ensure that the values in the Lens action form are exactly as specified in the following table.

|Field|Option you must select|
|-----|----------------------|
|Trigger From|Desktop|
|Trigger For|Excel Mapping|
|Table|Name of the table with which the Lens action will auto-map the Excel sheet column headers.|
|Request context|Supported Fields|
|Fields|Columns of the table|

**Tip:** A preconfigured Lens action that is designed to auto-map Excel sheet column headers with table columns is available by default on your instance. The name of the Lens action is `Import Excel Sheet data to custom table`. To use the Lens action, create a copy of this Lens action, and customize to create your own Lens action for this purpose.

### Procedure

1.  From your system, launch the ServiceNow AI Lens desktop application.

2.  On the login page, in the **Instance URL** field, enter the ServiceNow instance URL.

    For example, `https://<instance name>.service-now.com`.

3.  Select **Proceed**.

4.  Log in to your ServiceNow account by entering your username and password.

5.  On the onboarding journey widget, complete the onboarding and select **Got it**.

    ![Onboarding journey widget with three pages to show you the highlights of the application.](../image/onboarding-widget-lens.png)

    If you launch the ServiceNow AI Lens for the first time, the onboarding journey widget appears. You can select **Don't show me again** to hide the widget the next time you launch ServiceNow AI Lens.

6.  Select the Lens action that you have defined for Excel mapping.

    ![Excel mapping Lens action selected.](../image/lens-sel-excel-map-action.png)

    The **Proceed with Lens** button is disabled.

    **Note:** The **Proceed with Lens** button is disabled because to auto-map Excel sheet column headers with the table columns, ServiceNow AI Lens requires you to only attach an Excel sheet.

7.  Attach an Excel sheet by selecting **Upload** and then perform any one of the following file upload methods on the Upload file window.

    ![Excel file upload window.](../image/lens-excel-mapping-file-upload-window.png "File upload window")

<table id="choicetable_qnd_psb_13c"><thead><tr><th align="left" id="d40824e2351">

File upload method

</th><th align="left" id="d40824e2354">

File upload procedure

</th></tr></thead><tbody><tr><td id="d40824e2360">

**Add file**

</td><td>

1.  Select **+Add file**,
2.  Navigate to the location on your system and select the Excel sheet that you want to upload.

**Note:**

    -   You can upload only one Excel sheet.
    -   **Tip:** To remove an Excel sheet that you attached, select the Remove file icon \(![Remove file](../image/lens-file-attch-remove.png)\).

    -   The data only in the first worksheet of the Excel sheet will be analyzed.


</td></tr><tr><td id="d40824e2407">

**Drag and drop files**

</td><td>

1.  Navigate to the location on your system and select the Excel sheet that you want to upload.
2.  Drag the selected Excel sheet to the Drag and drop section \(![Drag and drop section.](../image/lens-drag-and-drop.png)\), and release the pointer to drop them.

**Note:**

    -   You can drag and drop only one Excel sheet.
    -   **Tip:** To remove an Excel sheet that you've attached, select the Remove file icon \(![Remove file](../image/lens-file-attch-remove.png)\).

    -   The data only in the first worksheet of the Excel sheet will be analyzed.


</td></tr></tbody>
</table>8.  Select **Next**.

9.  Select **Analyze**.

    ![Analyze button.](../image/lens-excel-map-analyze.png)

    ServiceNow AI Lens auto-maps the column headers of the attached Excel sheet and the table columns.

    ![Lens Excel and table column mapping.](../image/lens-excel-table-mapping.png)

    **Tip:** You can change the mapping by selecting one or more different table columns under the Imported as field heading.

10. Select **Submit**.

    The Excel sheet data is inserted into the table.



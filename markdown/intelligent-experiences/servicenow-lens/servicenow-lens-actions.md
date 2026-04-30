---
title: Define ServiceNow AI Lens behavior with Lens actions
description: As a Lens admin, you can create Lens actions in ServiceNow AI Lens to customize Lens behavior by providing default instructions, configuring context, and more.Create a Lens action to define custom context, trigger options, and default instructions for the ServiceNow AI Lens execution.Enable customers to scan documents related to car accident on their desktop to auto-fill the Insurance Request form on the ServiceNow instance.Enable compliance analysts to digitize and review several vendor agreements. Instead of manually entering details, they can launch ServiceNow AI Lens directly from the desktop, scan agreements, and adjust extracted values in the preview window before saving.Enable service agents to create user records by extracting specific information from identity documents using ServiceNow AI Lens, directly from the ServiceNow instance.
locale: en-US
release: yokohama
product: ServiceNow Lens
classification: servicenow-lens
topic_type: concept
last_updated: "2025-06-16"
reading_time_minutes: 16
breadcrumb: [Configure, ServiceNow AI Lens, Enable AI experiences]
---

# Define ServiceNow AI Lens behavior with Lens actions

As a Lens admin, you can create Lens actions in ServiceNow AI Lens to customize Lens behavior by providing default instructions, configuring context, and more.

Use Lens actions to define default instructions, trigger options, custom context, and post processing instructions for the Lens response. With Lens actions, you can achieve the following goals:

-   Trigger ServiceNow AI Lens from a desktop, ServiceNow instance, or Virtual Agent \(from a mobile device or a portal\)
-   Auto-fills a form on the ServiceNow instance
-   View the gathered insights in an editable preview
-   Trigger flows, subflows, or actions after Lens execution
-   Invoke AI agents
-   Run ServiceNow AI Lens as a back-end service

Whenever ServiceNow AI Lens is launched from an instance, it checks if any active Lens action is available for the table. If available, it uses the logic defined in Lens action during execution. The Lens action can only be used by the users or groups who are assigned to the Lens Actions record.

Refer to the following examples to understand the different use cases of setting up the Lens actions.

-   [Example: Scan documents to auto-fill the Insurance Request form](servicenow-lens-actions.md#)
-   [Example: Extract structured data from vendor agreements](servicenow-lens-actions.md#)
-   [Example: Auto-fill user records on a user table](servicenow-lens-actions.md#)

## Customize ServiceNow AI Lens behavior by creating a Lens action

Create a Lens action to define custom context, trigger options, and default instructions for the ServiceNow AI Lens execution.

### Before you begin

Role required: lens\_admin

### About this task

Learn about the various trigger options for ServiceNow AI Lens.

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

The Lens action can only be used by the users or groups who are assigned to the Lens Actions record.

![Lens action form with fields and Assigned users and groups related list.](../image/lens-action-form.png)

### Procedure

1.  Navigate to **All** &gt; **ServiceNow AI Lens** &gt; **Lens Actions**.

2.  Select **New**.

3.  Enter a name and description for the Lens action.

4.  In the **Trigger From** field, select one of the following options.

    |Option|Description|
    |------|-----------|
    |**Desktop**|Option to specify that this action must be used when ServiceNow AI Lens is triggered from the ServiceNow AI Lens desktop app.|
    |**Instance**|Option to specify this action must be used when ServiceNow AI Lens is triggered from a ServiceNow instance.|

5.  To save the changes, right-click the form header and select **Save**.

6.  On the Lens Actions form, fill in the fields.

<table id="table_vjg_bbk_pfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger For

</td><td>

-   **Form** - Lens action is used when ServiceNow AI Lens is triggered to auto-fill a form. Apply a transformation logic to the Lens response before the form is auto-filled by using the [servicenow-lens-actions.md\#transform-response](servicenow-lens-actions.md#transform-response) option.
-   **Service** - Lens action is used when ServiceNow AI Lens is used as a service. Select this option to trigger Lens from an instance to auto-populate a **Workspace form**, or to trigger it using Virtual Agent or Script Include.
-   **Others** - Lens action is used when ServiceNow AI Lens is triggered to display a preview of extracted data and perform post processing steps, if applicable.


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
function postProcessResponse(lensActionRecord, lensResponse) {
    
    //Add your code here

}
postProcessResponse(lensActionRecord, lensResponse);
```

Parameters accepted by the `postProcessResponse` method:

-   **lensActionRecord** \(Input\) - GlideRecord of the Lens action that is executed.
-   **lensResponse** \(Input\) - JSON object of the Lens response provided after Lens execution.


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
</table>7.  Assign users or groups who can use this Lens action.

    1.  In the Assigned Users and Groups related list, select **New**.

    2.  Add users or groups who can use this Lens action.

        You can create only one Assigned Users and Groups mapping for any Lens action.

<table><thead><tr><th>

Option

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Users

</td><td>

1.  Select the lock icon beside the **Users** field.
2.  Search and select the target user records from the reference field.
3.  Select the lock icon again to lock the field.
4.  Select **Submit**.
 **Note:** Only the users who have the lens\_user role are available for selection in the reference field.

</td></tr><tr><td>

Groups

</td><td>

1.  Select the lock icon beside the **Groups** field.
2.  Search and select the target group records from the reference field.
3.  Select the lock icon again to lock the field.
4.  Select **Submit**.
 **Note:** Ensure that you select the groups that have users with the lens\_user role.

</td></tr></tbody>
</table>    3.  Select **Submit**.

8.  Select **Update**.

9.  Select **Activate** for activating the Lens action.

    The Lens action will be available on the ServiceNow AI Lens desktop application landing page.


## Example: Scan documents to auto-fill the Insurance Request form

Enable customers to scan documents related to car accident on their desktop to auto-fill the Insurance Request form on the ServiceNow instance.

### Before you begin

Role required: lens\_admin

### About this task

You can define in the Lens action that ServiceNow AI Lens must be triggered from the desktop to auto-fill the Insurance Request form. Lens action includes the fields that must be updated with the extracted data.

![Example Lens action record for auto-filling Insurance request form.](../image/lens-action-insurance-example.png)

### Procedure

1.  Navigate to **All** &gt; **ServiceNow AI Lens** &gt; **Lens Actions**.

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

1.  Navigate to **All** &gt; **ServiceNow AI Lens** &gt; **Lens Actions**.

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

1.  Navigate to **All** &gt; **ServiceNow AI Lens** &gt; **Lens Actions**.

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



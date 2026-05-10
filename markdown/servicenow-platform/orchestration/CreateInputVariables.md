---
title: Create input variables
description: Create the variables to pass into the activity in the Inputs form of the activity designer.After you create the input variables, map them to the fields in the Execution Command form.Use the input variables you created to configure the command that Orchestration executes on the Windows target machine.You can test the input parameters of a custom activity during its development without having to run the activity in a workflow context.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Create custom activities using custom activity designer templates, Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create input variables

Create the variables to pass into the activity in the **Inputs** form of the activity designer.

## Before you begin

You must name your activity in the **General** form before you can advance to the **Inputs** stage.

Roles required: workflow\_admin or activity\_creator

**Note:** Variable strings in the **Inputs** form have a 255 character limit.

## Procedure

1.  Click the **+** icon to create a new input variable.

    The designer creates a default variable called **Input1**.

    ![Creating an input variable](../image/InputsNewVariable.png)

2.  Type your new variable name in the field.

3.  To change the name of a variable or any of its attributes, double-click the value and then select or enter a new value in the field that appears.

4.  Configure your variable using these fields:

    |Field|Description|
    |-----|-----------|
    |Type|Data type for this variable. Double-click on the field to display the choice list. In addition to the usual data types, you can create input arrays and encrypt individual variables that contain sensitive data. Encrypted variables are passed to the ECC Queue and then decrypted by the MID Server when they run on the target host. Sensitive data returned from running these variables on the host can then be passed to another activity through encrypted output variables.|
    |Mandatory|Marks an input variable as mandatory. Variables marked as mandatory are required fields in the properties form for the activity in the workflow. The input testing feature allows you to filter on mandatory variables.|
    |Default|Default value for this input variable. Default values are prepopulated for variables in the properties form for the activity in the workflow. You can override this value when you test the variables.|

5.  To reorder the variable list, select a row and then drag the row to its new location.

    When you select a row to move it, the pointer icon changes to an up/down arrow icon \(![up/down arrow icon](../image/MoveVariable.png)\).

6.  To delete a variable, click the delete icon \(![delete icon](../image/DeleteVar.png)\) in the row.

7.  Click **Continue** to advance to the **Execution Command** stage or click **Go to Pre-Processing \(Advanced\)** to create a script that runs before the activity executes.


**Parent Topic:**[Create custom activities using custom activity designer templates](create-custom-activities.md)

## Map an input variable

After you create the input variables, map them to the fields in the Execution Command form.

### Before you begin

Role required: activity\_admin, activity\_creator

### About this task

These fields contain values required by the target host or endpoint to authenticate and query for data. Included in this example are fields for a command to run on the target and the MID Server to use, if one is required.

### Procedure

1.  To map a variable, drag it into the appropriate field.

    The designer automatically expresses the variable in the syntax the system requires.

    ![Mapping input variables](../image/InputsMapping.png)


## Configure the PowerShell execution command

Use the input variables you created to configure the command that Orchestration executes on the Windows target machine.

### Before you begin

Create the input variables you need in the **Inputs** form before you can advance to the **Execution Command** stage.

Role required: activity\_creator, admin

**Note:** You can test the PowerShell connection between the MID Server and the target computer without having to run the acvitity in a workflow context. For details, see [test template outputs](CreateInputVariables.md#).

### Procedure

1.  Drag variables from the list of inputs and drop them into command fields.

    The system formats the variable in the proper syntax for the command.

    ![PowerShell execution command](../image/PowershellExecutionCommand.png "PowerShell execution command")

2.  Complete the fields shown in the table.

<table id="table_kgx_k55_cr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input

</td><td>

Input variable builder. [Create variables](CreateInputVariables.md#) to [map](CreateInputVariables.md#) to available fields.

</td></tr><tr><td>

Target host

</td><td>

Host name or IP address of the target server for this PowerShell activity.

</td></tr><tr><td>

Script type

</td><td>

Type of script to run on the PowerShell host. Available options are:-   Custom Powershell command
-   MID Server script file


</td></tr><tr><td>

MID Server script file

</td><td>

MID Server script file to run. This field is available when the **Script type** selected is MID Server script file.

</td></tr><tr><td>

Command

</td><td>

Command that this activity runs on the target host. This field is available when the **Script type** selected is Custom Powershell command. You can drag and drop input variables from the variable builder into this field to create your command.

</td></tr><tr><td>

Powershell variables

</td><td>

Name-value pairs to pass to the host with Powershell. You can create these variables manually, or drag input variables into the **Value** field. Encrypted input variables retain their encryption, regardless of the data type settings in this field. If you type in a value and select the **Encrypted** data type, your value appears in plain text in this field and is only encrypted when it passes to the ECC Queue.

</td></tr><tr><td>

Use MID service account

</td><td>

Forces this activity to authenticate on the target host using the credentials of the MID Server service account only, without trying any other credentials. When this check box is selected, the **Credential tag** field is not available.

</td></tr><tr><td>

Credential tag

</td><td>

Specific [Credential aliases for Orchestration activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/c_AssignCredsOrchActivities.md) this activity must use to run Powershell commands on the host. If this field is left blank, the MID Server tries all the available credentials until it finds a valid one, ending with the MID Server service account. If a credential alias is defined, the MID Server tries the credentials for that alias only and does not try the MID Server service account. This field is not available when the **Use MID service account** check box is selected.

</td></tr><tr><td>

Required MID Server capabilities

</td><td>

MID Server to use for querying Powershell, by capabilities. By default, the system selects a Powershell MID Server.

</td></tr></tbody>
</table>3.  Click **Save**.

4.  Click **Continue** to advance to the **Outputs** stage.


## Test activity template inputs

You can test the input parameters of a custom activity during its development without having to run the activity in a workflow context.

### Before you begin

Create input variables and map them to fields in the **Execution Command** form or provide actual values for these fields.

Role required: web\_service\_admin, activity\_admin, activity\_creator

### About this task

An input test executes only the input parameters against an endpoint and not the pre-processing or post-processing scripts. You need to use a workflow to test a pre-processing or post-processing scritp. You do not need to check out the activity to test it, and you can test input variables from any stage in the activity designer, if your activity is properly configured. Typically, the **Execution Command** stage is the point at which your inputs are ready for testing.

**Note:** If you intend to use auto-mapping, you must test your input variables.

### Procedure

1.  Click **Test Inputs**.

    The list of input source variables appears. If you added default values for these variables, those values appear in the **Substitute Value** column. Mandatory variables are marked with a red star. In this example, a SOAP endpoint returns a value for a stock quote variable.

    ![Test value for input variable](../image/TestDesignerSOAPInputValues.png)

2.  Filter the variable list with these controls:

    -   **All Inputs**: Displays all input variables. This is the default view.
    -   **Mandatory Inputs**: Displays only mandatory input variables.
    -   **Inputs Without Defaults**: Shows input variables that do not have assigned default values.
3.  Reset values as needed.

    -   **Reset default values**: Replaces any test values set in this form with the default values, if they are present.
    -   **Clear values**: Clears all values in the input variable list, even if default values exist.
4.  When your test values are configured correctly, click **OK**.

    The system runs the values for all the inputs configured against the specified target and returns the resulting payload. The buttons in the Response form display different views of the payload. The entire payload appears in the **Raw Output** window.

    ![Response payload from inputs test](../image/TestDesignerSOAPInputsResponse.png "Response payload from inputs test")

5.  To map appropriate parameter values in the payload to variables in the **Outputs** stage automatically, select an [auto-mapping option](automap-output-variable-inputs.md).

6.  Alternately, you can click **Save for parsing rules** to copy the entire payload to the parsing rules.

    This allows you to manually select values for the output variables directly from the payload. This action completely overwrites any previous payload that existed in the parsing rules.

7.  Click the **X** in the upper right corner of the window to close it.



---
title: Create a REST web service activity
description: Use this procedure to create a custom REST web service Orchestration activity.The ServiceNow activity designer allows you to map parameter values in a REST test payload to variables in the Outputs stage automatically.You use execution parameters to create the input process script in the Pre Processing form of the activity designer.These are instructions for creating JavaScript arrays using REST execution parameters.Use these parameters to create a post-processing script.Use the input variables you created to configure the command that Orchestration executes on the REST endpoint.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Orchestration custom activity templates, Orchestration activity designer, Classic Orchestration, Workflow Data Fabric]
---

# Create a REST web service activity

Use this procedure to create a custom REST web service Orchestration activity.

## Before you begin

Role required: web\_service\_admin, activity\_admin, activity\_creator

## About this task

To create and use a REST web service workflow activity:

-   Create a Create a REST message if an appropriate one is not already configured.
-   Assign the web\_service\_admin role to any user who must create or edit a custom REST activity.
-   Determine an application, or Application scope, for this activity.
-   Determine the Create a REST message to use for the activity. Use this value to override the endpoint configured in the REST message.
-   Optionally, create basic authentication credentials. Use this value to override the credentials configured in the SOAP message.

## Procedure

1.  Create a [custom activity](create-custom-activities.md).

    This action creates a custom activity using a template.

2.  After setting up [general properties](../reference/General-Flds-Templates.md) and [creating input variables](CreateInputVariables.md#), configure the REST web service Execution Command.

<table id="choicetable_g3y_2sq_vz"><tbody><tr><td id="d382148e149">

**[Map the input variables](CreateInputVariables.md#)**

</td><td>

Use the variables you created to configure the command that Orchestration executes.

</td></tr><tr><td id="d382148e165">

**REST message**

</td><td>

Name of an existing REST message to use in this activity.

</td></tr><tr><td id="d382148e174">

**REST message function**

</td><td>

REST message function to use for this activity.

</td></tr><tr><td id="d382148e183">

**Endpoint**

</td><td>

Endpoint URL for the REST web service this activity uses. Enter an endpoint in this field to override the endpoint configured in the REST message. Click the lock to open the input field.

</td></tr><tr><td id="d382148e192">

**Variable substitutions**

</td><td>

Name-value pairs to pass to the REST endpoint. You can create these parameters manually, or drag input variables into the parameter fields, and then assign a value. Parameters defined in the REST message that use **$\{\}** can be assigned data from this activity template. Use the **Additional attribute** column to configure the system to not escape the text. By default the text sent to the REST message is escaped. If the users have provided variables using Variable substitution in outbound REST messages in the REST message, then the **Name** column is automatically populated.

</td></tr><tr><td id="d382148e215">

**Additional Headers**

</td><td>

Additional HTTP header parameters for the REST message selected. You can also use these values to override parameters inherited from the REST message.

</td></tr><tr><td id="d382148e224">

**Additional Query Parameters**

</td><td>

Additional query parameters for the REST message selected. You can also use these values to override parameters inherited from the REST message.

</td></tr><tr><td id="d382148e233">

**Use MID Server**

</td><td>

Check box that determines if a MID Server should be used to invoke the REST web service.**Note:** If the REST web service message function defines a MID Server, that MID Server is used instead of the one selected here.

</td></tr><tr><td id="d382148e245">

**Required MID Server capabilities**

</td><td>

MID Server with the appropriate MID Server capabilities for connecting to the REST endpoint. By default, the system selects a MID Server with REST capabilities. This field is available when the **Use MID Server** check box is selected.

</td></tr><tr><td id="d382148e261">

**Timeout**

</td><td>

Allowed duration of the REST web service request before it times out, in seconds. The default is **10**.

</td></tr><tr><td id="d382148e273">

**Authentication**

</td><td>

Determines what type of authentication is required for the endpoint. The options are:-   **Use existing credentials in REST message**: Uses credential definitions from the REST message definition.
-   **Override with Basic Authentication credentials**: Uses Enable basic authentication for outbound SOAP credentials to override the credentials in the REST message definition. Basic authentication credentials must be provisioned before they are available for selection.
-   **Override with Certificate Authentication credentials**: Uses a certificate, such as a private key, to override the credentials in the REST message definition.
-   **Override with Both Basic and Certificate Authentication credentials**: Uses both basic authentication and certificate authentication to override the credentials in the REST message definition.
-   **Override with OAuth Authentication credentials**: Uses OAuth 2.0 credentials to override the credentials in the REST message definition. The REST message selected for this activity must have its OAuth 2.0 tutorial - create a REST message set to **OAuth 2.0** and its OAuth profiles and scopes configured appropriately.


</td></tr><tr><td id="d382148e330">

**Credentials**

</td><td>

Required REST endpoint basic authentication credentials. This field is available when **Override with Basic Authentication credentials** is selected in the **Authentication** field. Only basic authentication credentials appear in the selection list, which includes credentials stored on the instance and credential IDs from an external storage system. If you are using credentials stored in a CyberArk safe, you can override the default safe defined in the MID Server configuration file. See Configure the MID Server for CyberArk for details. Add the name of a different safe as a prefix to the credential ID, separated by a colon. For example, **newsafe:orch-test-f5**.

</td></tr><tr><td id="d382148e352">

**Protocol Profile**

</td><td>

Certificate authentication to use. This field is available when the selections in the **Authentication** are either **Override with Certificate Authentication credentials** or **Override with Both Basic and Certificate Authentication credentials**.

</td></tr><tr><td id="d382148e370">

**OAuth profile**

</td><td>

Profile for the OAuth provider for this REST message. See Specify an OAuth profile for more information.

</td></tr></tbody>
</table>    **Note:** You can map parameter values in a test payload to variables in the **Outputs** tab automatically. See [automap output variables](automap-output-variable-inputs.md).


## What to do next

Finish creating your Rest web service activity by [creating output variables](t_CreateAnOutputVariable.md#), [creating a parsing rule](t_CreateAParsingRule.md#), or [Conditions](../reference/conditions.md). Refer to the [create custom activities](create-custom-activities.md) topic to know your template options.

**Parent Topic:**[Orchestration custom activity templates](../concept/c_ActivityDesignerComponents.md)

## Auto-map REST activity output variables

The ServiceNow activity designer allows you to map parameter values in a REST test payload to variables in the **Outputs** stage automatically.

### Before you begin

Role required: web\_service\_admin, activity\_admin, activity\_creator

### About this task

**Note:** You can test input variables from any stage in the activity designer if you have provided enough information for Orchestration to contact the endpoint and return data. Typically, the **Execution Command** stage is the point at which your inputs are ready for testing.

### Procedure

1.  In the activity designer, proceed to the **Execution Command** stage.

2.  Define an appropriate MID Server, if requested.

    The test fails if the MID Server cannot be found or if it cannot connect to the target.

3.  Click **Test Activity** to test the input parameters.

    If you added actual values for the parameters and fields, the system runs those values against the specified target and returns the resulting payload. If you mapped input variables to fields and parameters, the system displays a dialog box for assigning test values to those variables.

4.  Provide test values, if requested, and click **OK** to display the payload.

    The entire payload appears in the **Raw Output** tab of the Response form.

    ![Auto-mapping controls](../image/AutoMappingButtons.png)

5.  Select one of these auto-mapping options.

    -   **Auto-Map to Local**: Directly maps values to a local variable for use within the activity.
    -   **Auto-Map to Output**: Directly maps values to the output variable to pass to other activities in the workflow. Auto-mapping to an output variable creates an array of objects, each of which contains the column names from the query result.

## REST template execution parameters

You use execution parameters to create the input process script in the **Pre Processing** form of the activity designer.

For descriptions of the REST web service command fields, see [Configure the REST execution command](t_CreateARESTWebServiceActivity.md#).

**Note:** You must use the `executionParam.` prefix with all variables in this table.

<table id="table_oyb_xdb_dr"><thead><tr><th>

Name

</th><th>

Variable

</th><th>

Type

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Web service message

</td><td>

web\_service\_message

</td><td>

Reference

</td><td>

The sys\_id of the corresponding web service message.

</td></tr><tr><td>

Web service message function

</td><td>

web\_service\_message\_function

</td><td>

Reference

</td><td>

The sys\_id of the REST message function.

</td></tr><tr><td>

Web service endpoint

</td><td>

web\_service\_endpoint

</td><td>

String

</td><td>

URL of the REST endpoint.

</td></tr><tr><td>

Parameters

</td><td>

parameters

</td><td>

Array of JavaScript objects

</td><td>

Array of JavaScript objects, expressed with the `executionParam.` prefix. For instructions on creating arrays using this parameter see [Create a JavaScript array in a REST template](t_CreateARESTWebServiceActivity.md#).

</td></tr><tr><td>

Use mid server

</td><td>

use\_mid\_server

</td><td>

Boolean

</td><td>

Selects whether or not to use the MID Server. A value of **true** uses the MID Server, and a value of **false** does not use the MID Server.

</td></tr><tr><td>

MidCapabilities

</td><td>

midCapabilities

</td><td>

String \(comma separated\)

</td><td>

List of references to required MID Server capabilities.

</td></tr><tr><td>

Time out

</td><td>

time-out

</td><td>

String

</td><td>

Allowable time out duration, expressed in seconds.

</td></tr><tr><td>

ValueCapabilities

</td><td>

valueCapabilities

</td><td>

Array of hashmap

</td><td>

Capability values used to select the MID Server. For more information, see MID Server capabilities. Use this example to customize the MID Server selection if there are additional capabilities that are assigned by value:```
var valueCapability = {'NEW_MID_CAPABIILTY':'NEW_MID_CAPABILITY_VALUE'}; executionParam.valueCapabilities.push(valueCapability);
```

</td></tr><tr><td>

Auth Type

</td><td>

auth-type

</td><td>

Boolean

</td><td>

Type of credentials to use. The choices are:-   basic\_auth\_pick\_credentials
-   use\_existing\_credentials

</td></tr><tr><td>

Credentials

</td><td>

credentials

</td><td>

Reference

</td><td>

Contains the credentials to use for this REST message when the **auth\_type** selected is **basic\_auth\_pick\_credentials**.

</td></tr></tbody>
</table>## Create a JavaScript array in a REST template

These are instructions for creating JavaScript arrays using REST execution parameters.

### Before you begin

Role required: web\_service\_admin, activity\_admin, activity\_creator

### About this task

To add more name-value pairs to the parameter's array, append the values to the existing array.

### Procedure

1.  Create a JavaScript object with the following syntax, and add it to the `executionParam.parameter` array:

    ```
    var newParameter = {"name":"parameterName","value":"parameterValue","additional_attribute":"none"}; 
    executionParam.parameters.push(newParameter);
    ```

    By adding the new parameter JavaScript object to the array, you ensure that any elements already available in the array are not impacted.

2.  Make sure to set the value in the **Additional attribute** column in the **REST message parameters** input field to **Do not escape text**.

    In this case, the system does not escape the value specified for the **value** attribute. An example of this is:

    ```
    var newParameter = {"name":"parameterName","value":"parameterValue","additional_attribute":"do_not_escape_text"}; 
    executionParam.parameters.push(newParameter);
    ```

    **Note:** If the value for the **additional\_attribute** field is **None**, then the system escapes the value specified by the **value** attribute. In the first example, `parameterValue` is escaped.


## REST template post-processing parameters

Use these parameters to create a post-processing script.

|Name|Variable|Type|Usage|
|----|--------|----|-----|
|Status code|status\_code|Integer|Contains the status code returned from the REST web service.|
|Header|header|Hashmap of JavaScript object|Hashmap of key value pairs associated with the header values passed into the web service. You can access each value with `executionResult.header[keyName]`.|
|Body|body|String|Contains a string value representing the output from the REST message|
|Error|error|String|Returns the error string from the REST web service, unless there are no errors, in which case it returns**null**.|

## Configure the REST execution command

Use the input variables you created to configure the command that Orchestration executes on the REST endpoint.

### Before you begin

Create the input variables you need in the **Inputs** form before you can advance to the **Execution Command** stage.

Role required: web\_service\_admin, activity\_admin, activity\_creator

**Note:** You can test the REST connection between the MID Server and the endpoint without having to run the acvitity in a workflow context. For details, see [test template outputs](CreateInputVariables.md#).

### Procedure

1.  Drag variables from the list of inputs and drop them into command fields.

    The system formats the variable in the proper syntax for the command.

    ![REST execution command](../image/RESTExecutionCommand.png "REST execution command")

2.  Complete the fields shown in the table.

<table id="table_bmf_m1b_dr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input

</td><td>

Input variable builder. [Create input variables](CreateInputVariables.md#) to map to available fields.

</td></tr><tr><td>

REST message

</td><td>

Name of an existing REST message to use in this activity. Users must have the web\_service\_admin role to configure this field.

</td></tr><tr><td>

REST message function

</td><td>

REST message function to use for this activity. Users must have the web\_service\_admin role to configure this field.

</td></tr><tr><td>

Endpoint

</td><td>

Endpoint URL for the REST web service this activity uses. Enter an endpoint in this field to override the endpoint configured in the REST message. Click the lock to open the input field.

</td></tr><tr><td>

Variable substitutions

</td><td>

Name-value pairs to pass to the REST endpoint. You can create these parameters manually, or drag and drop input variables into the parameter fields, and then assign a value. Parameters defined in the REST message that use **$\{\}** can be assigned data from this activity template. Use the **Additional attribute** column to configure the system to not escape the text. By default the text sent to the REST message is escaped. The **Name** column is automatically populated if the users have provided variables using Variable substitution in outbound REST messages in the REST message.

</td></tr><tr><td>

Additional Headers

</td><td>

Additional HTTP header parameters for the REST message selected. You can also use these values to override parameters inherited from the REST message.

</td></tr><tr><td>

Additional Query Parameters

</td><td>

Additional query parameters for the REST message selected. You can also use these values to override parameters inherited from the REST message.

</td></tr><tr><td>

Use MID Server

</td><td>

Check box that determines if a MID Server should be used to invoke the REST web service.**Note:** If the REST web service message function defines a MID Server, that MID Server is used instead of the one selected here.

</td></tr><tr><td>

Required MID Server capabilities

</td><td>

MID Server with the appropriate MID Server capabilities for connecting to the REST endpoint. By default, the system selects a MID Server with REST capabilities. This field is available when the **Use MID Server** check box is selected.

</td></tr><tr><td>

Timeout

</td><td>

Allowed duration of the REST web service request before it times out, in seconds. The default is **10**.

</td></tr><tr><td>

Authentication

</td><td>

Determines what type of authentication is required for the endpoint. The options are:-   **Use existing credentials in REST message**: Uses credential definitions from the REST message definition.
-   **Override with Basic Authentication credentials**: Uses Enable basic authentication for outbound SOAP credentials to override the credentials in the REST message definition. Basic authentication credentials must be provisioned before they are available for selection.
-   **Override with Certificate Authentication credentials**: Uses a certificate, such as a private key, to override the credentials in the REST message definition.
-   **Override with Both Basic and Certificate Authentication credentials**: Uses both basic authentication and certificate authentication to override the credentials in the REST message definition.
-   **Override with OAuth Authentication credentials**: Uses OAuth 2.0 credentials to override the credentials in the REST message definition. The REST message selected for this activity must have its OAuth 2.0 tutorial - create a REST message set to **OAuth 2.0** and its OAuth profiles and scopes configured appropriately.


</td></tr><tr><td>

Credentials

</td><td>

Required REST endpoint basic authentication credentials. This field is available when **Override with Basic Authentication credentials** is selected in the **Authentication** field. Only basic authentication credentials appear in the selection list, which includes credentials stored on the instance and credential IDs from an external storage system. If you are using credentials stored in a CyberArk safe, you can override the Configure the MID Server for CyberArk defined in the MID Server configuration file by adding the name of a different safe as a prefix to the credential ID, separated by a colon. For example, **newsafe:orch-test-f5**.

</td></tr><tr><td>

Protocol Profile

</td><td>

Certificate authentication to use. This field is available when the selections in the **Authentication** field is either **Override with Certificate Authentication credentials** or **Override with Both Basic and Certificate Authentication credentials**.

</td></tr><tr><td>

OAuth profile

</td><td>

Profile for the OAuth provider for this REST message. See Specify an OAuth profile for more information.

</td></tr></tbody>
</table>3.  Click **Save**.

4.  Click **Continue** to advance to the **Outputs** stage.



---
title: Create a JavaScript Probe activity
description: Create a JavaScript Probe activity to instruct a MID server to execute server-side javascript.You use execution parameters to create the input process script in the Preprocessing form of the activity designer.Use these parameters to create a post-processing script.Use the input variables you created to configure the command that Orchestration executes on the JavaScript Probe target host.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Orchestration custom activity templates, Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a JavaScript Probe activity

Create a JavaScript Probe activity to instruct a MID server to execute server-side javascript.

## Before you begin

Role required: activity\_creator or workflow\_admin

## About this task

The JavascriptProbe activity has the same functionality as making ‘Packages’ calls into standard Java libraries. It allows you to have more control over the Java libraries on the MID Server. You can load your own JAR files on the MID Server and have the JavascriptProbe make Package calls into those java files.

## Procedure

1.  Create a custom activity.

    This action creates a custom activity using a template.

2.  After setting up [general properties](../reference/General-Flds-Templates.md) and [creating input variables](CreateInputVariables.md#), configure the JavaScript probe activity Execution Command.

<table id="choicetable_jlf_3tp_vz"><tbody><tr><td id="d202780e112">

**[Map the input variables](CreateInputVariables.md#)**

</td><td>

Use the variables you created to configure the command that Orchestration executes on the MID server.

</td></tr><tr><td id="d202780e128">

**Script type**

</td><td>

Select the type of script to include. Available options are:-   Custom JavaScript
-   MID Server script include


</td></tr><tr><td id="d202780e146">

**Script**

</td><td>

Custom JavaScript to run with this probe. **Note:** This field is available when the **Script type** selected is **Custom JavaScript**.

</td></tr><tr><td id="d202780e164">

**MID Server script include**

</td><td>

Script for the MID Server to run with this probe. **Note:** This field is available when the **Script type** selected is **MID Server script include**.

</td></tr><tr><td id="d202780e182">

**Select MID Server by host**

</td><td>

MID Server on which the probe runs.

</td></tr><tr><td id="d202780e192">

**Required MID Server capabilities**

</td><td>

MID Server to use, by capabilities.

</td></tr><tr><td id="d202780e201">

**Parameters**

</td><td>

Name-value pairs to pass to the host with this probe. You can create these parameters manually, or drag input variables into the **Parameters** fields and assign a value.

</td></tr></tbody>
</table>    **Note:** You can map parameter values in a test payload to variables in the **Outputs** tab automatically. See [automap output variables](automap-output-variable-inputs.md).


## What to do next

Finish creating your JavaScript probe activity by [creating output variables](t_CreateAnOutputVariable.md#), [creating a parsing rule](t_CreateAParsingRule.md#), or Conditions. Refer to the [create custom activities](create-custom-activities.md) topic to know your template options.

**Parent Topic:**[Orchestration custom activity templates](../concept/c_ActivityDesignerComponents.md)

## JavaScript probe template execution parameters

You use execution parameters to create the input process script in the **Preprocessing** form of the activity designer.

For descriptions of the JavaScript Probe command fields, see the table in [Configure the JavaScript Probe execution command](t_CreateAJavaScriptProbeActivity.md#).

**Note:** You must use the `executionParam.` prefix with all variables in this table.

<table id="table_pbn_kh5_cr"><thead><tr><th>

Name

</th><th>

Variable

</th><th>

Type

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Script Type

</td><td>

script\_type

</td><td>

Enumerated

</td><td>

Type of script to run. The possible types are:-   custom\_javascript\_typ
-   mid\_script\_include\_type

</td></tr><tr><td>

Script

</td><td>

script

</td><td>

String

</td><td>

Script that runs custom JavaScript when the **script\_type** is **custom\_javascript\_type**.

</td></tr><tr><td>

Mid script include

</td><td>

mid\_script\_include

</td><td>

Reference

</td><td>

The sys\_id reference associated with the MID Server script include to call, when the **script\_type** is **mid\_script\_include\_type**.

</td></tr><tr><td>

Source

</td><td>

source

</td><td>

String

</td><td>

Target host on which to run the script.

</td></tr><tr><td>

MidCapabilities

</td><td>

midCapabilities

</td><td>

String \(comma separated\)

</td><td>

List of required MID Server capabilities.

</td></tr><tr><td>

Parameters

</td><td>

parameters

</td><td>

Array of JavaScript object

</td><td>

Array of JavaScript objects, expressed with the `executionParam.` prefix. To add more name-value pairs to the **parameters** array, append them to the existing array. Create a JavaScript object with the following syntax, and add it to the `executionParam.parameter` array. This assigns additional parameters to the message:```
var newParameter = {"name":"parameterName","value":"parameterValue"};
executionParam.parameters.push(newParameter);
```

</td></tr><tr><td>

ValueCapabilities

</td><td>

valueCapabilities

</td><td>

Array of hashmap

</td><td>

Capability values used to select the MID Server. For more information, see [MID Server capabilities](../../../product/mid-server/reference/r_MIDServerCapabilities.md). If there are additional capabilities that are assigned by value, use this example to customize the MID Server selection:```
var valueCapability = {'NEW_MID_CAPABIILTY':'NEW_MID_CAPABILITY_VALUE'};
executionParam.valueCapabilities.push(valueCapability);
```

</td></tr></tbody>
</table>## JavaScript probe template post-processing parameters

Use these parameters to create a post-processing script.

|Name|Variable|Type|Usage|
|----|--------|----|-----|
|Payload|payload|String|Contains raw payload returned from the JavaScript Probe.|
|Output|output|String|Contains output data returned from the JavaScript Probe.|
|EccSysId|eccSysId|String|Contains the reference ID associated with the ECC Queue input message.|
|Error Messages|errorMessages|String|Contains the error messages returned from the JavaScript probe. If no error messages are returned, this value is null.|

## Configure the JavaScript Probe execution command

Use the input variables you created to configure the command that Orchestration executes on the JavaScript Probe target host.

### Before you begin

Create the input variables you need in the **Inputs** form before you can advance to the **Execution Command** stage.

Role required: activity\_creator, admin

**Note:** You can test the JavaScript Probe connection between the MID Server and the target without having to run the acvitity in a workflow context. For details, see [test template outputs](CreateInputVariables.md#).

### Procedure

1.  Drag variables from the list of inputs and drop them into command fields.

    The system formats the variable in the proper syntax for the command.

    ![JavaScript Probe execution command](../image/JavaScriptExecutionCommand.png "JavaScript Probe execution command")

2.  Complete the fields shown in the table.

<table id="table_zmv_v25_cr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input

</td><td>

Input variable builder. [Create input variables](CreateInputVariables.md#) to [map](CreateInputVariables.md#) to available fields.

</td></tr><tr><td>

Script type

</td><td>

Select the type of script to include. Available options are:-   Custom JavaScript
-   MID Server script include


</td></tr><tr><td>

Script

</td><td>

Custom JavaScript to run with this probe. This field is available when the **Script type** selected is **Custom JavaScript**.

</td></tr><tr><td>

MID Server script include

</td><td>

Script for the MID Server to run with this probe. This field is available when the **Script type** selected is **MID Server script include**.

</td></tr><tr><td>

Select MID Server by host

</td><td>

MID Server on which the probe runs.

</td></tr><tr><td>

Required MID Server capabilities

</td><td>

MID Server to use, by capabilities.

</td></tr><tr><td>

Parameters

</td><td>

Name-value pairs to pass to the host with this probe. You can create these parameters manually, or drag input variables into the **Parameters** fields and assign a value.

</td></tr></tbody>
</table>3.  Click **Save**.

4.  Click **Continue** to advance to the **Outputs** stage.



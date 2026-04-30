---
title: Create a probe activity
description: Create an activity that runs a probe on the target host that is configured to return specific information..You use execution parameters to create the input process script in the Pre Processing form.Use these parameters to create a post-processing script.Use the input variables you created to configure the command that Orchestration executes on the target.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Orchestration custom activity templates, Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a probe activity

Create an activity that runs a probe on the target host that is configured to return specific information..

## Before you begin

Role required: activity\_creator or workflow\_admin

## About this task

For instructions on using the activity template process flow, see [create custom activities](create-custom-activities.md).

## Procedure

1.  Create a [custom activity](https://www.servicenow.com/docs/access?context=create-custom-activities&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

    This action creates a custom activity using a template.

2.  After setting up [general properties](../reference/General-Flds-Templates.md) and [creating input variables](CreateInputVariables.md#), configure the Probe Execution Command.

<table id="choicetable_bf3_bpv_vz"><tbody><tr><td id="d344628e117">

**[Map the input variables](CreateInputVariables.md#)**

</td><td>

Use the variables you created to configure the command that Orchestration executes.

</td></tr><tr><td id="d344628e133">

**Probe**

</td><td>

Probe to run with this activity, from the list of probes in the system

</td></tr><tr><td id="d344628e142">

**Target host**

</td><td>

Host name or IP address of the target server for this activity.

</td></tr><tr><td id="d344628e151">

**Parameters**

</td><td>

MID Server to use, by capabilities.

</td></tr><tr><td id="d344628e160">

**Required MID Server capabilities**

</td><td>

Name-value pairs to pass to the host with this probe. You can create these parameters manually, or drag and drop input variables into the parameter fields and assign a value.

</td></tr></tbody>
</table>    **Note:** You can map parameter values in a test payload to variables in the **Outputs** tab automatically. See [automap output variables](automap-output-variable-inputs.md).


## What to do next

-   Use [auto-mapping](automap-output-variable-inputs.md) to generate outputs and parsing rules
-   If you do not use auto-mapping, you can manually [create output variables](t_CreateAnOutputVariable.md#) and [create parsing rules](t_CreateAParsingRule.md#)

**Parent Topic:**[Orchestration custom activity templates](../concept/c_ActivityDesignerComponents.md)

## Probe template execution parameters

You use execution parameters to create the input process script in the **Pre Processing** form.

For descriptions of the command fields, see [Configure the Probe execution command](t_CreateAProbeActivity.md#).

**Note:** You must use the `executionParam.` prefix with all variables in this table.

<table id="table_pwj_qdc_dr"><thead><tr><th>

Name

</th><th>

Variable

</th><th>

Type

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Probe

</td><td>

probe

</td><td>

Reference

</td><td>

The sys\_id of the MID Server probe.

</td></tr><tr><td>

Source

</td><td>

source

</td><td>

String

</td><td>

Intended target host

</td></tr><tr><td>

Parameters

</td><td>

parameters

</td><td>

Array of JS object

</td><td>

Array of JavaScript objects, expressed with the `executionParam.` prefix. To add more name-value pairs to the **parameters** array, append them to the existing array. Create a JavaScript object with the following syntax, and add it to the `executionParam.parameter` array. This assigns additional parameters to the message:```
var newParameter = {"name":"parameterName","value":"parameterValue"}; executionParam.parameters.push(newParameter);
```

</td></tr><tr><td>

MidCapabilities

</td><td>

midCapabilities

</td><td>

String \(comma separated\)

</td><td>

List of required MID server capabilities.

</td></tr><tr><td>

ValueCapabilities

</td><td>

valueCapabilities

</td><td>

Array of hashmap

</td><td>

Capability values used to select the MID Server. For more information, see [MID Server capabilities](../../../product/mid-server/reference/r_MIDServerCapabilities.md). If there are additional capabilities that are assigned by value, use this example to customize the MID Server selection:```
var valueCapability = {'NEW_MID_CAPABIILTY':'NEW_MID_CAPABILITY_VALUE'}; executionParam.valueCapabilities.push(valueCapability);
```

</td></tr></tbody>
</table>## Probe template post-processing parameters

Use these parameters to create a post-processing script.

|Name|Variable|Type|Usage|
|----|--------|----|-----|
|Payload|payload|String|Contains raw payload returned from the probe.|
|Output|output|String|Contains output data returned from the probe.|
|EccSysId|eccSysId|String|Contains the reference ID associated with the ECC Queue input message.|

## Configure the Probe execution command

Use the input variables you created to configure the command that Orchestration executes on the target.

### Before you begin

Create the input variables you need in the **Inputs** form before you can advance to the **Execution Command** stage.

Role required: activity\_creator, admin

**Note:** You can test the activity connection between the MID Server and the target without having to run the acvitity in a workflow context. For details, see [test template outputs](CreateInputVariables.md#).

### Procedure

1.  Drag variables from the list of inputs and drop them into command fields.

    The system formats the variable in the proper syntax for the command.

    ![Probe execution command](../image/ProbeExecutionCommand.png "Probe execution command")

2.  Complete the fields shown in the table.

    |Field|Description|
    |-----|-----------|
    |Input|Input variable builder. [Create input variables](CreateInputVariables.md#) to map to available fields.|
    |Probe|Probe to run with this activity, from the list of probes in the system.|
    |Target host|Host name or IP address of the target server for this activity.|
    |Required MID Server capabilities|MID Server to use, by capabilities.|
    |Parameters|Name-value pairs to pass to the host with this probe. You can create these parameters manually, or drag and drop input variables into the parameter fields and assign a value.|

3.  Click **Save**.

4.  Click **Continue** to advance to the **Outputs** stage.



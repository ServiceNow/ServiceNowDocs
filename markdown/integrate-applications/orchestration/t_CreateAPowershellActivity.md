---
title: Create a PowerShell activity
description: Create a custom PowerShell activity return data to a workflow from a host using Microsoft PowerShell.You use execution parameters to create the input process script in the Pre Processing form of the activity designer.Use these parameters to create a post-processing script, payload parsing, and tagging.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Orchestration custom activity templates, Orchestration activity designer, Classic Orchestration, Workflow Data Fabric]
---

# Create a PowerShell activity

Create a custom PowerShell activity return data to a workflow from a host using Microsoft PowerShell.

## Before you begin

Role required: activity\_creator or workflow\_admin

## About this task

ServiceNow supports PowerShell 3.0 to 5.1.

## Procedure

1.  Create a [custom activity](create-custom-activities.md).

    This action creates a custom activity using a template.

2.  After setting up [general properties](../reference/General-Flds-Templates.md) and [creating input variables](CreateInputVariables.md#), configure the PowerShell Execution Command.

<table id="choicetable_asj_mzp_vz"><tbody><tr><td id="d594192e116">

**[Map the input variables](CreateInputVariables.md#)**

</td><td>

Use the variables you created to configure the command that Orchestration executes on the MID Server.

</td></tr><tr><td id="d594192e132">

**Target host**

</td><td>

Host name or IP address of the target server for this PowerShell activity.

</td></tr><tr><td id="d594192e141">

**Script type**

</td><td>

Type of PowerShell script to run on the PowerShell host. Available options are:-   Custom PowerShell command
-   MID Server script file


</td></tr><tr><td id="d594192e159">

**MID Server script file**

</td><td>

The MID Server script file contains the PowerShell scripts. This field is available when the **Script type** selected is MID Server script file.

</td></tr><tr><td id="d594192e171">

**Command**

</td><td>

PowerShell command the activity executes. This field is available when the **Script type** selected is Custom PowerShell command. You can create your commands by dragging and dropping input variables from the variable builder into this field.

</td></tr><tr><td id="d594192e187">

**PowerShell variables**

</td><td>

Name-value pairs to pass to the host with PowerShell. You can create these variables manually, or drag input variables into the **Value** field. Encrypted input variables retain their encryption, regardless of the data type settings in this field. If you type in a value and select the **Encrypted** data type, your value appears in plain text. It is only encrypted when it passes to the ECC Queue.

</td></tr><tr><td id="d594192e202">

**Use MID Service Account**

</td><td>

If checked, this activity authenticates on the target host using the credentials of the MID Server service account only, without trying any other credentials. **Note:** The **Credential tag** field is not available.

</td></tr><tr><td id="d594192e217">

**Credential tag**

</td><td>

Credential tag this activity must use to run PowerShell commands on the host. If this field is left blank, the MID Server tries all the available credentials until it finds a valid one, ending with the MID Server service account. If a credential tag is defined, the MID Server tries the credentials with that tag specified only and does not try the MID Server service account. **Note:** This field is not available when the **Use MID service account** check box is selected.

</td></tr><tr><td id="d594192e232">

**Required MID Server capabilities**

</td><td>

MID Server to use for querying PowerShell, by capabilities. By default, the system selects a PowerShell MID Server.

</td></tr></tbody>
</table>    **Note:** You can map parameter values in a test payload to variables in the **Outputs** tab automatically. See [automap output variables](automap-output-variable-inputs.md).


## What to do next

Finish creating your PowerShell activity by [creating output variables](t_CreateAnOutputVariable.md#), [creating a parsing rule](t_CreateAParsingRule.md#), or [Conditions](../reference/conditions.md). Refer to the [create custom activities](create-custom-activities.md) topic to know your template options.

**Parent Topic:**[Orchestration custom activity templates](../concept/c_ActivityDesignerComponents.md)

## PowerShell template execution parameters

You use execution parameters to create the input process script in the **Pre Processing** form of the activity designer.

For descriptions of the Powershell command fields, see the table in [Configure the PowerShell execution command](CreateInputVariables.md#).

**Note:** You must use the `executionParam.` prefix with all variables in this table.

<table id="table_b2b_jw5_cr"><thead><tr><th>

Name

</th><th>

Variable

</th><th>

Type

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Source

</td><td>

source

</td><td>

String

</td><td>

Target host on which to execute the command.

</td></tr><tr><td>

Script type

</td><td>

script\_type

</td><td>

Enumeration

</td><td>

Type of script to run. The possible types are:-   **command:** Custom PowerShell command.
-   **file:** Identifies the MID Server script file to run.

</td></tr><tr><td>

Command

</td><td>

command

</td><td>

String

</td><td>

Command sent to the MID Server for it to run on the target host.

</td></tr><tr><td>

MidScriptFile

</td><td>

midScriptFile

</td><td>

Reference

</td><td>

Reference sys\_id of the MID Server script file to execute, when the **script\_type** is **file**.

</td></tr><tr><td>

PowershellVariables

</td><td>

powershellVariables

</td><td>

Array of hashmap

</td><td>

Hashmap of JavaScript objects with **name**, **value**, and **type** for each object. The **type** of each object can be one of **plain**, **encrypted**, **boolean**, or **null**, corresponding to the PowerShell variable **type** selected in the inputs tab. For example, you might enter:```
var newParameter = {"name":"parameterName","value":"parameterValue", "type": "plain" };
executionParam.powershellVariables.push(newParameter);
```

</td></tr><tr><td>

Credential tag

</td><td>

credential\_tag

</td><td>

String

</td><td>

Specific credential tag this activity must use to run PowerShell commands on the host.

</td></tr><tr><td>

MidCapabilities

</td><td>

midCapabilities

</td><td>

String \(comma separated\)

</td><td>

List of required MID Server capabilities.

</td></tr><tr><td>

ValueCapabilities

</td><td>

valueCapabilities

</td><td>

Array of hashmap

</td><td>

Capability values used to select the MID Server. For more information, see MID Server capabilities. If there are additional capabilities that are assigned by value, use this example to customize the MID Server selection:```
var valueCapability = {'NEW_MID_CAPABIILTY':'NEW_MID_CAPABILITY_VALUE'};
executionParam.valueCapabilities.push(valueCapability);
```

</td></tr></tbody>
</table>## Powershell post-processing parameters and payload parsing

Use these parameters to create a post-processing script, payload parsing, and tagging.

<table id="table_grr_t2v_cr"><thead><tr><th>

Name

</th><th>

Variable

</th><th>

Type

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Tags

</td><td>

tags

</td><td>

Hashmap of tag values to return from the PowerShell command.

</td><td>

Contains the tags used to extract output using the PowerShell commands. The tag output is delimited by double percentage signs, as in **%%tagname%% … %%**. Set up the command using the format in this example:```
Write-Host %%tagname1%%
output1 line 1
output1 line 2
…
Write-Host%%

Write-Host %%tagname2%%
output2 line 1
output2 line 2
…
Write-Host%%
```

 The tags returned are JavaScript hashmap objects in which each key is prefixed with **tag** appended with the **tagname**.

 ```
{"__text__": "", 
"tagtagname1":"output1 line1\noutput1 line2\n", 
"tagtagname2":"output2 line1\noutput2 line2\n"}
```

</td></tr><tr><td>

Hresult

</td><td>

hresult

</td><td>

String

</td><td>

Contains any **hresult** returned from the PowerShell command. If no **hresult** is returned, this parameter is **null**.

</td></tr><tr><td>

Output

</td><td>

output

</td><td>

String

</td><td>

Contains the raw output from the PowerShell command.

</td></tr><tr><td>

EccSysID

</td><td>

eccSysID

</td><td>

String

</td><td>

Contains the reference ID associated with the ECC Queue input message returned by the activity.

</td></tr><tr><td>

ErrorMessages

</td><td>

errorMessages

</td><td>

String

</td><td>

Contains any error messages retrieved from the PowerShell command. This value is **null** if there are no error messages.

</td></tr></tbody>
</table>
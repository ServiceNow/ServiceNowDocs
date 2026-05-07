---
title: Create an SSH activity
description: Create an activity that extracts data from a target host that uses the SSH network protocol.Use execution parameters to create the input process script in the Pre Processing form of the activity designer.Use these parameters to create a post-processing script, payload parsing, and tagging.Use the input variables you created to configure the command that Orchestration executes on the host target.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Orchestration custom activity templates, Orchestration activity designer, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an SSH activity

Create an activity that extracts data from a target host that uses the SSH network protocol.

## Before you begin

Role required: activity\_creator or workflow\_admin

## About this task

For instructions on using the activity template process flow, see [create custom activities](create-custom-activities.md).

## Procedure

1.  Create a [custom activity](https://www.servicenow.com/docs/access?context=create-custom-activities&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

    This action creates a custom activity using a template.

2.  After setting up [general properties](../reference/General-Flds-Templates.md) and [creating input variables](CreateInputVariables.md#), configure the SSH Execution Command.

<table id="choicetable_j2l_k2s_d1b"><tbody><tr><td id="d345850e117">

**[Map the input variables](CreateInputVariables.md#)**

</td><td>

Use the variables you created to configure the command that Orchestration executes.

</td></tr><tr><td id="d345850e133">

**Target host**

</td><td>

Host name or IP address of the target server for this activity.

</td></tr><tr><td id="d345850e142">

**Command**

</td><td>

Command this activity runs on the target host. You can invoke a MID Server script from this field using any script type that the SSH command line supports. For more information, see **Advanced SSH script options** below the table.

</td></tr><tr><td id="d345850e154">

**Directory**

</td><td>

Directory on the target host where the command is run.

</td></tr><tr><td id="d345850e163">

**Credential tag**

</td><td>

The Orchestration credential tag to use when running the command.

</td></tr><tr><td id="d345850e173">

**Required MID Server capabilities**

</td><td>

MID Server with the appropriate capabilities for connecting to the host. By default, the system selects a MID Server with SSH capabilities.

</td></tr><tr><td id="d345850e182">

**Long running**

</td><td>

If checked, disables the SSH connection timeout for commands that might take longer to run than the default 60 seconds. Orchestration periodically checks the running process to determine its status until it is finished.

</td></tr><tr><td id="d345850e191">

**Must Sudo**

</td><td>

If checked, enables the use of [sudo](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) to run commands.

</td></tr></tbody>
</table>    **Note:** You can map parameter values in a test payload to variables in the **Outputs** tab automatically. See [automap output variables](automap-output-variable-inputs.md).


## Advanced SSH script options

To run a MID Server script on the target host, specify the script type and pass the name of the script into the `${syncFile()}` parameter. The system uses this parameter to locate the named script in the MID Server Script File \[ecc\_agent\_script\_file\] table and run it on the target host. For example, a bash script can be expressed as:

```
bash ${syncFile("<MID script name>")} argument1 argument2 argument3
```

A base script \(`main_script.bash`\) can reference another script \(`my_include.bash`\) as well as a separate file \(`.my_profile`\) located on the target host. Both scripts and the file referenced must be synced to the MID Server, using the `${syncFile()}` parameter, to execute properly.

```
source ${syncFile(".my_profile")}
cp ${syncFile("my_include.bash")} /usr/ssmith/my_include.bash
bash ${syncFile("main_script.bash")} one two three four five six 
rm /usr/ssmith/my_include.bash
```

A Python example with inline comments might look like this:

```
set $LIB_DIR=/usr/bin;. 
# Sync a file that is referenced inside myF5CreateLBPool.py 
cp ${syncFile("specialFunctions.py")} ~/specialFunctions.py 
# set up environment variables 
source ${syncFile(".python_profile")} 
# call script that sets up dependencies on the box from remote package repos 
python ${syncFile("setupPythonDependencies.py")} pycontrol 
# call a script that requires functions from the package as well as a function from myIncludedFile 
python ${syncFile("myF5CreateLBPool.py")} snow_pool myActualValue 
# user is responsible for their own cleanup 
rm ~/specialFunctions.py 
```

## What to do next

-   Use [auto-mapping](automap-output-variable-inputs.md) to generate outputs and parsing rules
-   If you do not use auto-mapping, you can manually [create output variables](t_CreateAnOutputVariable.md#) and [create parsing rules](t_CreateAParsingRule.md#)

**Parent Topic:**[Orchestration custom activity templates](../concept/c_ActivityDesignerComponents.md)

## SSH template execution parameters

Use execution parameters to create the input process script in the **Pre Processing** form of the activity designer.

For descriptions of the command fields, see [Configure the SSH execution command](t_CreateAnSSHActivity.md#).

**Note:** You must use the `executionParam.` prefix with all variables in this table.

<table id="table_wl1_yxc_dr"><thead><tr><th>

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

Intended target or host.

</td></tr><tr><td>

Command

</td><td>

command

</td><td>

String

</td><td>

Comment to run on the host.

</td></tr><tr><td>

Directory

</td><td>

directory

</td><td>

String

</td><td>

Directory on the host in which to run the command.

</td></tr><tr><td>

Credential tag

</td><td>

credential\_tag

</td><td>

String

</td><td>

Orchestration credential tag to use when running the command.

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

Capability values used to select the MID Server. For more information, see [MID Server capabilities](../../../product/mid-server/reference/r_MIDServerCapabilities.md). If there are additional capabilities that are assigned by value, use this example to customize the MID Server selection:```
var valueCapability = {'NEW_MID_CAPABIILTY':'NEW_MID_CAPABILITY_VALUE'};
executionParam.valueCapabilities.push(valueCapability);
```

</td></tr><tr><td>

Long running

</td><td>

long\_running

</td><td>

Boolean

</td><td>

Indicates whether or not the command is long running. A value of true indicates that the command is long running.

</td></tr><tr><td>

Must sudo

</td><td>

must\_sudo

</td><td>

Boolean

</td><td>

Indicates whether or not this activity must use sudo to run root commands. A value of true indicates that [sudo](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) must be used.

</td></tr></tbody>
</table>## SSH post-processing parameters and payload parsing

Use these parameters to create a post-processing script, payload parsing, and tagging.

<table id="table_nzv_q1d_dr"><thead><tr><th>

Name

</th><th>

Variable

</th><th>

Type

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Output

</td><td>

output

</td><td>

String

</td><td>

Contains the output returned from the SSH command.

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

Contains the error messages retrieved from the SSH command. This value is **null** if there are no error messages.

</td></tr><tr><td>

Tags

</td><td>

tags

</td><td>

Hashmap of tag values returned from the SSH command

</td><td>

Contains the tags used to extract output using the SSH commands. The tag output is delimited by double percentage signs, as in `%%tagname%% … %%`. Set up the command using the following format:```
%%tagname1%%
output1 line 1
output1 line 2
…
%%

%%tagname2%%
output2 line 1
output2 line 2
…
%%
```

The tags returned are JavaScript hashmap objects in which each key is prefixed with `tag` appended with the tagname.```
{"__text__": "", 
"tagtagname1":"output1 line1\noutput1 line2\n", 
"tagtagname2":"output2 line1\noutput2 line2\n"}
```

</td></tr></tbody>
</table>## Configure the SSH execution command

Use the input variables you created to configure the command that Orchestration executes on the host target.

### Before you begin

Create the input variables you need in the **Inputs** form before you advance to the **Execution Command** stage.

Role required: activity\_creator, admin

**Note:** You can test the SSH connection between the MID Server and the target without having to run the acvitity in a workflow context. For details, see test template outputs.

### Procedure

1.  Drag variables from the list of inputs and drop them into command fields.

    The system formats the variable in the proper syntax for the command.

    ![SSH execution command](../image/SSHExecutionCommand.png "SSH execution command")

2.  Complete the fields shown in the table.

<table id="table_xf4_kvc_dr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input

</td><td>

Input variable builder. [Create input variables](CreateInputVariables.md#) to map to available fields.

</td></tr><tr><td>

Target host

</td><td>

Host name or IP address of the target server for this activity.

</td></tr><tr><td>

Command

</td><td>

Command this activity runs on the target host. You can invoke a MID Server script from this field using any script type that is supported by the SSH command line. For more information, see **Advanced SSH script options** below the table.

</td></tr><tr><td>

Directory

</td><td>

Directory on the target host where the command is run.

</td></tr><tr><td>

Credential tag

</td><td>

The [Credential aliases for Orchestration activities](https://www.servicenow.com/docs/access?context=c_AssignCredsOrchActivities&version=australia&pubname=australia-platform-security&ft:locale=en-US) to use when running the command.

</td></tr><tr><td>

Select MID Server by capabilities

</td><td>

MID Server with the appropriate capabilities for connecting to the host. By default, the system selects a MID Server with SSH capabilities

</td></tr><tr><td>

Long running

</td><td>

Check box to disable the SSH connection timeout for commands that might take longer to run than the default 60 seconds. Orchestration periodically checks the running process to determine its status until it is finished.

</td></tr><tr><td>

Must Sudo

</td><td>

Check box to allow the use of [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) to run commands.

</td></tr></tbody>
</table>3.  Click **Save**.

4.  Click **Continue** to advance to the **Outputs** stage.



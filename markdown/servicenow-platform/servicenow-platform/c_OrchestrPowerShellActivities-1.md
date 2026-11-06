---
title: PowerShell activities
description: PowerShell is built on the Windows .NET Framework and is designed to control and automate the administration of Windows machines and applications.The Run PowerShell activity executes Windows PowerShell commands on a MID Server.When a PowerShell script encounters an error, the Windows machine may return an HResult code as part of the error message.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
---

# PowerShell activities

PowerShell is built on the Windows .NET Framework and is designed to control and automate the administration of Windows machines and applications.

PowerShell must be installed on any MID Server that uses these activities. MID Servers using PowerShell must be installed on a supported Windows operating system. ServiceNow supports PowerShell 3.0 to 5.1.

The ServiceNow [Orchestration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/r_ListOfOrchestrationActivities.md) plugin adds these basic PowerShell activities to workflows. For instructions on using activities from the PowerShell activity pack, see [PowerShell activity pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/c_OrchestrPwrshellActivityPack.md)

**Parent Topic:**[Deprecated Orchestration activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/r_OrchestrationBasicActivities.md)

## Legacy Run PowerShell activity

The Run PowerShell activity executes Windows PowerShell commands on a MID Server.

**Important:** This activity is deprecated and is unavailable for new workflows. To replace the functionality of this activity, use the [Powershell activity template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/orchestration/t_CreateAPowershellActivity.md) to create a custom, scoped activity. Workflows from a previous release that use the Run PowerShell activity can continue to do so.

### Result Values

The workflow designer can assign a result value using activity.result from within a script field of the activity. By default, the success or failure of the PowerShell commands used determines the result value of the Run PowerShell activity. Possible result values are:

-   Success
-   Failure

### Scratchpad Entries

Information written to *stdout* by the executing script is captured and returned to the activity in the*activity.output* variable. This information can be parsed, processed, or saved \(to a scratchpad variable, for example\) for future processing in the activity’s sensor script.

An example would be to run the get-date command to get the MID Server’s current time. This sensor script saves the full output received, but we can process it to return and save only the time.

\[Omitted image "RBAPowershellActivity.png"\] Alt text: PowerShell activity

**Note:** This is an over-simplified example. In most cases, the script operates against some remote Windows computer. However, the principal is the same – whatever is written to `stdout` is returned in `activity.output` and available to process.

### Input Variables

<table id="table_kh2_mys_hp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hostname

</td><td>

IP address of the target Windows machine. This value is mapped to the *$computer* variable for use in commands \(see the example in the **Command** field\). A PowerShell credential variable called *$cred* that is based on information in the ServiceNow Credentials table will authenticate on the computer pointed to by **Hostname**.

</td></tr><tr><td>

Command

</td><td>

Enter the PowerShell command to run. For example, to execute a simple WMI query against a remote machine pointed to by the *hostname* variable, the command is:```
get-wmiobject <class> -computer $computer -credential $cred
```

 If no credentials authenticate on the computer, the command runs in the context of the MID Server user.

 You cannot run both a command and a script file. Specifying a command hides the *Script file* variable.

</td></tr><tr><td>

Sensor script

</td><td>

The script to run using the results of the probe. The output from the probe is contained in a variable called *output*. Any error from the probe is contained in a variable called *error*.

</td></tr><tr><td>

Script file

</td><td>

The [Enable script file synchronization for Windows enhanced security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-script-attach.md). You cannot run both a script file and a command. Selecting a script file hides the *Command* variable.

</td></tr><tr><td>

PowerShell script variables

</td><td>

Additional parameters, in JSON format, used by the specified script file.

</td></tr></tbody>
</table>### States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Executing|The workflow engine knows to start the onExecute function of the activity.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activty, was cancelled.|

Add workflow variables for the command line using the normal workflow variable syntax. In the example above, if the &lt;class&gt; was in a workflow input variable called *myclass*, the command would look like:

```
get-wmiobject $ {workflow. inputs. myclass } -computer $computer –credential $cred
Similarly  if the variable  is a scratchpad variable named myclass , the command would look like :
get -wmiobject $ {workflow. scratchpad. myclass } -computer $computer –credential $cred
```

## HResult codes

When a PowerShell script encounters an error, the Windows machine may return an HResult code as part of the error message.

PowerShell activities can read and interpret this code. Not all PowerShell errors include an HResult code. In the event of a failed PowerShell script, you can use the HResult code to move the workflow through a specific condition.

For example, when resetting an Active Directory password to a password that does not meet policy requirements, such as minimum length or complexity, the PowerShell script returns the HResult code -2146022651. To use this code, create an activity condition with the **Condition** value of *activity.hresult = -2146022651*. If the PowerShell script returns this code when the activity runs, the workflow transitions through this new condition.


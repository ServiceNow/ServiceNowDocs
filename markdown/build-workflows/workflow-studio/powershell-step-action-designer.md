---
title: PowerShell step
description: Run PowerShell scripts on remote machines from your ServiceNow instance through a MID Server.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Workflow Studio steps, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# PowerShell step

Run PowerShell scripts on remote machines from your ServiceNow instance through a MID Server.

PowerShell is built on the Windows .NET Framework and is designed to control and automate the administration of Windows machines and applications. ServiceNow supports PowerShell 3.0 to 5.1. PowerShell 3.0 does not support Windows 2003 Server.

**Note:** This step requires an Integration Hub subscription. For more information, see [Legal schedules - Integration Hub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Roles and availability

Available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Fields

<table id="table_tq4_bxp_4cb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection

</td><td>

Type of connection to use. -   **Define Connection Inline**: Define connection information within the action step.
-   **Use Connection Alias**: Define connection information using the Connection Alias table. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action.

 To learn more about connections and credentials, see [Introduction to credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Connection Alias

</td><td>

Connection &amp; Credential alias record that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action. To learn more about connections and credentials, see [credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US). The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel. **Note:** This field is available when **Use Connection Alias** is selected from the Connection list.

</td></tr><tr><td>

Credential Alias

</td><td>

Credential alias that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials when using an action in multiple environments. Likewise, if the credential information changes, you don't need to update your custom action. To learn more about connections and credentials, see [credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US). The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel. **Note:** This field is available when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

Host

</td><td>

Specify the fully-qualified domain name of the target host where the system runs the action step. For example, host.domain.com. **Note:** This field is only visible when the **Connection** is **Define Connection Inline**.

</td></tr><tr><td>

Port

</td><td>

Specify the communications port on which the target host listens for connections. For example, 5985. Leave blank to use the default port. **Note:** This field is only visible when the **Connection** is **Define Connection Inline**.

</td></tr><tr><td>

MID Selection

</td><td>

Option to select a specific MID Server or MID Cluster. Choose any one of the following options. -   **Auto-Select MID Server**: Your ServiceNow instance selects the MID Server without manual input.
-   **Specific MID Server**: Your ServiceNow instance uses MID Server that you specify.
-   **Specific MID Cluster**: Your ServiceNow instance uses the MID Cluster that you specify.

A MID Cluster is a group of MID Servers that enables your ServiceNow instance to handle multiple integrations, and improve integration speed. For more information, see [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


 This field is available when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

MID Application

</td><td>

Specify the application the MID Server must support to be eligible for selection. The system runs the action step from a MID Server that supports the selected application. If you use a data pill for this field, the pill must reference the MID Application's name, not the MID Application record. This field is available when **Define Connection Inline** is selected from the Connection list and **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

Capabilities

</td><td>

Capabilities the MID Server must support to be eligible for selection. The system runs the action step from a MID Server that supports the selected capabilities. This field is available when **Define Connection Inline** is selected from the Connection list and **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Server

</td><td>

Data pill containing a sys\_id reference to a MID Server \[ecc\_agent\_list\] record. This field is available when **Define Connection Inline** is selected from the Connection list and **Specific MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Cluster

</td><td>

Data pill for the MID Cluster you want to use. This field is available when **Define Connection Inline** is selected from the Connection list, and **Specific MID Cluster** is selected from the MID Selection list.

</td></tr><tr><td>

Remoting Type

</td><td>

The location where the PowerShell script runs such as the MID or a remote server.-   **Explicit Remoting \(Most Common\)**: Establish a connection with and run the script on a remote server.
-   **Implicit Remoting \(Advanced\)**: Run a script on a MID Server while importing necessary modules from a remote server. If selected, define the **Remote name prefix** and **Modules to import** fields. For optimal performance, only import modules necessary to the step. If blank, all available modules are imported from the server.
-   **Run on a MID Server or have your script establish a remote session**: Run a script directly on a MID Server, or define remoting specifications within the script. This value is the default.

 **Note:** To invoke a function in a PowerShell script command or PowerShell script file, the command must define the function param block if the function has input parameters. This requirement applies to explicit and implicit remoting. For additional information on param block, see Microsoft's documentation on Windows Powershell parameters at [https://technet.microsoft.com/](https://technet.microsoft.com/).

</td></tr><tr><td>

Remote name prefix

</td><td>

The file path, excluding file names, to the modules to load from the remote server. **Note:** This field is only visible when the **Remoting Type** is **Implicit Remoting \(Advanced\)**.

</td></tr><tr><td>

Modules to import

</td><td>

The comma-separated list of modules to import from the remote server at the defined file path. **Note:** This field is only visible when the **Remoting Type** is **Explicit Remoting \(Most Common\)** or **Implicit Remoting \(Advanced\)**.

</td></tr><tr><td>

Test PowerShell Step

</td><td>

Button to test the configured credential for the PowerShell step. For more information, see [Test a credential for the PowerShell step](https://www.servicenow.com/docs/access?context=test-credential-powershell&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

</td></tr><tr><td>

Script type

</td><td>

The type of script to run on the PowerShell host.-   **Inline script**: Enter the script to run in the **Command** field of the step.
-   **MID Server Script File**: Select the PowerShell script to run from the MID Server Script Files \[ecc\_agent\_script\_file\] table. This is the default value and separates scripting logic from the action, enabling you to update the script without having to modify and redeploy the action.

</td></tr><tr><td>

MID Server Script

</td><td>

Pre-defined PowerShell script from the MID Server Script Files table \[ecc\_agent\_script\_file\]. **Note:** This field is only available if the **Script type** is **MID Server Script File**.

</td></tr><tr><td>

Script path

</td><td>

Read-only path to the selected MID Server script.**Note:** This field is only visible when the **Script type** is **MID Server Script File**.

</td></tr><tr><td>

Input variables

</td><td>

The optional name-value pairs that represent the values of PowerShell script variables. You can use action inputs and data from other steps within the PowerShell script. Define the following fields for each variable: -   **Name**: The name of the script variable to pass a value to. The name cannot match a reserved or prohibited PowerShell variable. Some variable names are reserved for internal processing and should not be used as input variables. See **Reserved variables** in **PowerShell scripting variables**.
-   **Type**: The type of PowerShell variable. Select plain text, encrypted, or boolean. If encrypted is selected, the value appears in plain text in this field and is only encrypted when it passes to the ECC Queue.
-   **Value**: The value to map to the variable. Manually enter a value, or drag a data pill into the field.

</td></tr><tr><td>

Command

</td><td>

The inline PowerShell script to run on the target host.**Note:** This field is only visible when the **Script type** is **Inline script**.

</td></tr></tbody>
</table>## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see [Action error evaluation](../concept/action-error-evaluation.md).


## PowerShell scripting variables

To access input variables from the **Command** field, you must call them using special syntax. The syntax you use depends on the value of a system property. If the **Remoting Type** is **Run on a MID Server or have your script establish a remote session**, some reserved variables are available in addition to input variables.

-   **Input variable syntax**

    By default, prefix variable names with a $ character. For example, if an input variable is named **message**, use $message to access the variable in script.

    If the **mid.powershell.command.script.parameter\_passing** parameter is set to false, prefix the variable name with $env:SNC\_. For example, if an input variable is named **message**, use $env:SNC\_message to access the variable in script. To learn more about the **mid.powershell.command.script.parameter\_passing** parameter, see [MID Server parameters](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

-   **Reserved variables**

    When the **Remoting Type** is **Run on a MID Server or have your script establish a remote session**, the following variables are available for use in script. Reserved variables cannot be used as custom input variable names.

    |Reserved variable|Description|
    |-----------------|-----------|
    |$computer|Host IP address defined in the Connection alias record.|
    |$cred|Credential object that contains the credentials defined in the connection record. Use this variable with any PowerShell cmdlet that supports the credential parameter. For example, `New-PSSession -credential $cred`.|
    |$log\_info|If the **mid.property.powershell.log\_info** property is set to true, adds logging information to a PowerShell script.|

    The following variable names are reserved for internal processing and should not be used as input variables.

    -   script
    -   useCred
    -   isMid
    -   isDiscovery
    -   debug
    -   user
    -   password
    -   executingScriptDirectory
    -   midScriptDirectory
    -   hresult

**Parent Topic:**[Workflow Studio steps](../concept/steps.md)


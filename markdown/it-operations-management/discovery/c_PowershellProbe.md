---
title: PowerShell probe
description: The PowerShell Probe executes PowerShell V2 scripts on the MID Server host.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [List of Discovery probes, Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# PowerShell probe

The PowerShell Probe executes PowerShell V2 scripts on the MID Server host.

PowerShell scripts are defined as probe parameters with the filename as the parameter name. It is available as a Probe probe type by specifying PowerShell as the probe's ECC queue topic.

## PowerShell probe parameters

<table id="table_thk_ngg_dcb"><thead><tr><th>

Parameter name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

source

</td><td>

\[Required\] The initial host to connect to. **Default:** None

</td></tr><tr><td>

&lt;script name&gt;.ps1

</td><td>

\[Required\] The filename of the PowerShell script to run. Replace **&lt;script name&gt;** with a valid filename prefix.**Default:** None

</td></tr><tr><td>

powershell\_command\_parameter\_passing

</td><td>

Specifies whether to pass script parameters on the command line. Regardless of this parameter's value, ServiceNow makes all script parameters on the command line automatically available to PowerShell scripts as environment variables.

 **Default:** false

</td></tr><tr><td>

powershell\_param\_&lt;script parameter name&gt;

</td><td>

Passes additional parameters to the PowerShell script to be executed. Each parameter will appear to the script as an environment variable in the format **$env:SNC\_&lt;script parameter name&gt;**. Parameters with this prefix are not considered encrypted and are passed through to the script untouched. Make sure you select the appropriate parameter between **powershell\_param\_&lt;script parameter name&gt;** and **powershell\_&lt;script parameter name&gt;**. Using the wrong prefix results in errors in the PowerShell execution, which is passed back to the instance in the ECC queue input.**Default:** None

</td></tr><tr><td>

powershell\_&lt;script parameter name&gt;

</td><td>

Passes additional parameters to the PowerShell script to be executed. Each parameter will appear to the script as an environment variable in the format **$env:SNC\_&lt;script parameter name&gt;**. The MID Server assumes that any parameter with this prefix is encrypted and attempts to decrypt it. Make sure you select the appropriate parameter between **powershell\_param\_&lt;script parameter name&gt;** and **powershell\_&lt;script parameter name&gt;**. Using the wrong prefix results in errors in the PowerShell execution, which is passed back to the instance in the ECC queue input**Default:** None

</td></tr><tr><td>

debug

</td><td>

Enables debug log output during the probe.**Default:** false

</td></tr><tr><td>

credentials\_debug

</td><td>

Displays a &lt;credentials\_debug&gt; section in the ECC queue, which can help you troubleshoot credentials. If you set this property to true, credential troubleshooting information is output to the ECC queue, even if the credentials succeed. **Default:** false

</td></tr></tbody>
</table>## Scripting requirements

Any custom PowerShell scripts must use environment variables to pass any non-Boolean command line parameter. Replace non-Boolean parameters in the Param\(\) portion of the script with script variables of the same name. Define the script variable as part of the environment with an SNC\_ prefix. So a string parameter such as this:

```
Param([string]$paramName)
```

Becomes a script variable such as the following:

```
if(test-path env:\SNC_paramName) {
    $paramName = $env:SNC_paramName
}
```

For example, this parameter definition from the PSScript.ps1 script contains several string parameters that need to be redefined as script variables:

```
Param([string]$computer, [string]$script, [string]$user, [string]$password, [boolean]$useCred, [boolean]$isDiscovery, [boolean]$debug)
```

Defining the non-Boolean parameters as script variables would result in this type of script:

```
Param([boolean]$useCred, [boolean]$isDiscovery, [boolean]$debug)
 
# Copy the environment variables to the params
if(test-path env:\SNC_computer) {
  $computer=$env:SNC_computer
}
 
if(test-path env:\SNC_script) {
  $script=$env:SNC_script
}
 
if(test-path env:\SNC_user) {
  $user=$env:SNC_user
  $password=$env:SNC_password
}
```

-   **[Create a custom PowerShell probe](../../orchestration/task/t_CreateACustomPowershellProbe.md)**  
You can create your own PowerShell probe and configure probe parameters.

**Parent Topic:**[List of Discovery probes](../reference/r_ListOfDiscoveryProbes.md)


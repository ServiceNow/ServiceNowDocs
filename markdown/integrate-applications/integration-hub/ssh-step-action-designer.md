---
title: SSH step
description: The SSH step executes SSH commands on an external \*nix system through a ServiceNow MID Server. The step also stores scripts and commands for the \*nix systems.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integration steps, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SSH step

The SSH step executes SSH commands on an external \*nix system through a ServiceNow® MID Server. The step also stores scripts and commands for the \*nix systems.

**Note:**

-   This step requires an Integration Hub subscription. For more information, see [Legal schedules - Integration Hub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).
-   Integration Hub supports ServiceNow SSH only.

## Roles and availability

The SSH step is available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Sanitizing inputs

Escape all user inputs to eliminate the possibility of a malicious user executing arbitrary commands on your target server. Escape and validate data pills before the command field uses them by sanitizing arguments using Sanitize shell arguments transform functions. This transform function category automatically appears when a data pill is dropped into the **Command** input.

## Fields

<table id="table_qhj_3tt_khb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Connection Details

</td></tr><tr><td>

Connection

</td><td>

Type of connection to use.-   **Define Connection Inline**: Define connection information within the action step.
-   **Use Connection Alias**: Define connection information using the Connection Alias table. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action.

 To learn more about connections and credentials, see Introduction to credentials, connections, and aliases.

</td></tr><tr><td>

Connection Alias

</td><td>

Connection &amp; Credential alias record that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using an action in multiple environments. Likewise, if the connection information changes, you don't need to update your custom action. To learn more about connections and credentials, see credentials, connections, and aliases. The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel. This field is available when **Use Connection Alias** is selected from the Connection list.

</td></tr><tr><td>

Credential Alias

</td><td>

Credential alias that the system uses to run the action step. Users with the flow\_designer or admin role can create or select an associated Connection record. Using an alias eliminates the need to configure multiple credentials when using an action in multiple environments. Likewise, if the credential information changes, you don't need to update your custom action. To learn more about connections and credentials, see credentials, connections, and aliases. The credential value is displayed as a Password \(2 Way Encrypted\) data pill on the data panel. This field is available when **Define Connection Inline** is selected from the Connection list.**Note:** The SSH step requires a credential record that supports either SSH private key credentials or SSH credentials. This step does not support Windows credentials where the **Use MID Server service account** option is selected.

</td></tr><tr><td>

Host

</td><td>

Host name or IP address of the target server. This field is available when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

Port

</td><td>

Port number to communicate with the server. This field is available when **Define Connection Inline** is selected from the Connection list.**Note:** Provide valid value between `1` and `65535`. If you provide any other value, the value will be set `22` by default.

</td></tr><tr><td>

MID Selection

</td><td>

Option to select a specific MID Server or MID Cluster. Choose any one of the following options. -   **Auto-Select MID Server**: Your ServiceNow instance selects the MID Server without manual input.
-   **Specific MID Server**: Your ServiceNow instance uses MID Server that you specify.
-   **Specific MID Cluster**: Your ServiceNow instance uses the MID Cluster that you specify.

A MID Cluster is a group of MID Servers that enables your ServiceNow instance to handle multiple integrations, and improve integration speed. For more information, see Configure a MID Server cluster.


 This field is available when **Define Connection Inline** is selected from the Connection list.

</td></tr><tr><td>

MID Application

</td><td>

Option to use a MID Server to run the SSH step. This field is available when **Define Connection Inline** is selected from the Connection list and **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

Capabilities

</td><td>

Capability of the MID Server. Select **SSH**. This field is available when **Define Connection Inline** is selected from the Connection list and **Auto-Select MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Server

</td><td>

Data pill of the required MID Server. This field is available when **Define Connection Inline** is selected from the Connection list and **Specific MID Server** is selected from the MID Selection list.

</td></tr><tr><td>

MID Cluster

</td><td>

Data pill for the MID Cluster you want to use. This field is available when **Define Connection Inline** is selected from the Connection list, and **Specific MID Cluster** is selected from the MID Selection list.

</td></tr><tr><td colspan="2">

SSH Configuration

</td></tr><tr><td>

Working Directory

</td><td>

Optional target directory on the target host where the command is run.

</td></tr><tr><td>

Command

</td><td>

Command that runs on the target directory. The command can also include MID Server scripts. See [Advanced SSH script options](ssh-step-action-designer.md#adv-ssh-section_l1v_jqk_phb) for more information.**Note:** Escape and validate data pills before the command field uses them by sanitizing arguments using a preprocessing Script step. For more information, see [Sanitizing arguments using the escape class and function](jdbc-step.md#section_gqd_cy4_qhb).

</td></tr><tr><td>

Long Running

</td><td>

Option to disable the SSH connection timeout for commands that might take longer than the default time of 120 seconds to run. When selected, the engine detaches from the execution thread until completion.

</td></tr><tr><td>

Sudo Mode

</td><td>

Option to elevate privileges to execute the script.

</td></tr></tbody>
</table>For more information, see SSH credentials.

## Action error evaluation

-   **If this step fails**

    Data type: **Choice**

    Option to continue running the next step or go to error evaluation. To use the step status code or message for a custom action error condition, see Action error evaluation.


## Advanced SSH script options

To run a MID Server script on the target host, specify the script type and pass the name of the script into the `${syncFile()}`parameter. The system uses this parameter to locate the named script in the MID Server Script File \[ecc\_agent\_script\_file\] table and run it on the target host. For example, a bash script can be expressed as:

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

To see the list of available MID Server scripts, navigate to **MID Server** &gt; **Script Files**.


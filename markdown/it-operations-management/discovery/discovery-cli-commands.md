---
title: Discovery CLI commands
description: A list of commands that are available to the Discovery Command Line Interface \(CLI\) in the Pattern Designer Enhancements application.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 12
breadcrumb: [Discovery reference, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery CLI commands

A list of commands that are available to the Discovery Command Line Interface \(CLI\) in the Pattern Designer Enhancements application.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## discovery-insights

Retrieves details about your discovery configurations and patterns. The details include custom pattern information, instance details, and plugin details.

-   **Command group**

    Parent group: discovery

-   **Roles required**

    discovery\_admin

    If using a service related to Discovery, you must have the required roles for that service.

-   **Command structure**

    ```
    snc discovery discovery-insights
    ```

-   **Example**

    Retrieve details about your discovery configurations and patterns by executing the following command:

    ```
    snc discovery discovery-insights
    ```

    The command returns a JSON object \(default format\) containing the information in the following table.

<table id="table_ks3_24p_dzb"><thead><tr><th>

Object

</th><th>

Details

</th></tr></thead><tbody><tr><td>

`customizedPatterns`

</td><td>

-   `patternName`: Name of the customized pattern
-   `source`: Location where the customized changes are contained \(for example, Default\)


</td></tr><tr><td>

`instanceDetails`

</td><td>

-   `buildDate`: Date of the instance build \(format: MM-DD-YYYY\_HHMM\)
-   `buildName`: Name of the instance build


</td></tr><tr><td>

`pluginDetails`

</td><td>

Plugins related to discovery configuration or that are necessary to run CLI.

</td></tr></tbody>
</table>-   **Return value**

    ```
    ✔ Discovery diagnostics successfully completed.
    {
       "customizedPattern": [
          {
             "patternName": "A10",
             "source": "Default"
          },
          {
             "patternName": ".NET Application",
             "source": "Default"
          }
       ],
       "instanceDetails": {
          "buildDate": "09-16-2023_2010",
          "buildName": "utah-p0"
       },
       "pluginDetails": {
          "CMDB CI Class Models": "1.48",
          "Discovery and Service Mapping Patterns": "1.8.0",
          "Pattern Designer Enhancements": "3.1.0",
          "Visibility Content": "6.13.0"
       }
    }
    ```


## get-discovery-credentials

Retrieves the list of discovery credentials.

-   **Command group**

    Parent group: discovery

-   **Roles required**

    discovery\_admin

    If using a service related to Discovery, you must have the required roles for that service.

-   **Command structure**

    ```
    snc discovery get-discovery-credentials [arguments]
    ```

-   **Argument:**

    `--testableonly`: Includes only credentials that can be tested. Possible values: true or false.

-   **Examples**

    Retrieve a list of the discovery credentials by executing the following command:

    ```
    snc discovery get-discovery-credentials
    ```

    List only testable discovery credentials by executing the command with the following argument:

    ```
    snc discovery get-discovery-credentials --testableonly="true"
    ```

-   **Return value**

    ```
    ✔ Get only testable credentials [ssh, snmpv3, snmp, ssh_private_key, windows, vmware, jdbc, jms]: true
    ✔ Discovery credentials details retrieved
    {
       "credentials": [
          {
             "active": true,
             "name": "shCred",
             "type": "ssh",
             "updated": "2023-10-16 10:57:27"
          },
          {
             "active": true,
             "name": "WindowsCred",
             "type": "windows",
             "updated": "2023-10-10 12:18:17"
          },
          {
             "active": true,
             "name": "Azure",
             "type": "azure",
             "updated": "2022-10-19 05:57:21"
          },
          {
             "active": true,
             "name": "public",
             "type": "snmp",
             "updated": "2023-09-28 07:40:35"
          },
          {
             "active": true,
             "name": "Windows MID Server Service Account",
             "type": "windows",
             "updated": "2023-10-16 10:57:23"
          },
          …
       ]
    }
    ```


## get-discovery-logs

Retrieves discovery logs with flexible options, including:

-   Status filtering
-   Device inclusion
-   External Communication Channel \(ECC\) queue logs
-   Pattern logs
-   Output format choices

-   **Command group**

    Parent group: discovery

-   **Roles required**

    discovery\_admin

    If using a service related to Discovery, you must have the required roles for that service.

-   **Command structure**

    ```
    snc discovery get-discovery-logs [arguments]
    ```

-   **Arguments**

<table id="table_rqz_dtp_dzb"><thead><tr><th>

Argument

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`--status-id`

</td><td>

Discovery status number by which to filter logs.

</td></tr><tr><td>

`--devices`

</td><td>

Includes device-specific logs. Possible values: true or false.

</td></tr><tr><td>

`--ecc-queue-logs`

</td><td>

Includes associated ECC queue logs. Possible values: true or false.

</td></tr><tr><td>

`--pattern-logs`

</td><td>

Includes pattern execution logs. Possible values: true or false.

</td></tr><tr><td>

`--pattern-log-level`

</td><td>

Maximum severity level by which to filter pattern logs. The available options are: -   DEBUG: Includes only DEBUG log messages \(default\)
-   ERROR: Includes ERROR and DEBUG messages
-   WARN: Includes WARN, ERROR, and DEBUG messages
-   INFO: Includes all messages


</td></tr><tr><td>

`--log-limit`

</td><td>

Maximum number of log records to return between 1-100 \(default: 100\). Applies to ECC queue and pattern logs only.

</td></tr><tr><td>

`--output-format`

</td><td>

Output format for the logs. Supported formats are JSON \(default format\) or table.

</td></tr></tbody>
</table>-   **Examples**

    Retrieve discovery logs by executing the following command:

    ```
    snc discovery get-discovery-logs [options]
    ```

    Customize the log retrieval by including the arguments either one at a time or as a single command.

    -   To execute the command one argument at a time:

        ```
        snc discovery get-discovery-logs
        Discovery status number: DIS0010013
        Include Devices: true
        Include ECC Queue logs: true
        Include pattern execution logs: true
        Pattern max log level (INFO, WARN, ERROR, DEBUG): DEBUG
        Maximum number of log records to return: 100
        Output format [supported: json(default), table]: json
        ```

    -   To execute the command as a single command:

        ```
        snc discovery get-discovery-logs --status-id="DIS0010013" --ecc-queue-logs="true" --devices="true" --pattern-logs="true" --output-format="json"
        ```

    If the maximum number of log records to return is high, consider using a table output format.

-   **Return value**

    ```
    ✔ Discovery Status details retrieved
    {
       "Devices": [
          {
             "CMDBCI": "",
             "ClassificationProbe": "Windows - Classify",
             "Completed": "4",
             "CompletedActivity": "Updated CI",
             "Created": "2023-10-17 09:25:33",
             "CurrentActivity": null,
             "Issues": "0",
             "ScanStatus": "Completed 4",
             "Started": "4",
             "Status": "DIS0010136"
          }
       ],
       "DiscoveryLogs": [
          {
             "CI": "",
             "Created": "2023-10-17 09:25:24",
             "Device": "",
             "ECCQueueInput": "",
             "Level": "0",
             "Message": "Discovery started",
             "Source": "Discovery",
             "Status": "DIS0010136"
          },
          {
             "CI": "",
             "Created": "2023-10-17 09:26:49",
             "Device": "192.168.1.100",
             "ECCQueueInput": "HorizontalDiscoveryProbe",
             "Level": "0",
             "Message": "Exploring CI Pattern, Pattern name: Windows OS - Servers",
             "Source": "DiscoverySensor",
             "Status": "DIS0010136"
          },
          {
             "CI": "",
             "Created": "2023-10-17 09:27:01",
             "Device": "192.168.1.100",
             "ECCQueueInput": "",
             "Level": "0",
             "Message": "Discovery completed",
             "Source": "Discovery",
             "Status": "DIS0010136"
          }
       ],
       "DiscoveryStatus": [
          {
             "Completed": "5",
             "Created": "2023-10-17 09:25:24",
             "Description": "Discover Now",
             "Discover": "CIs",
             "Duration": "1970-01-01 00:01:37",
             "Number": "DIS0010136",
             "Schedule": "WinServer",
             "Started": "5",
             "State": "Completed",
             "Updated": "2023-10-17 09:27:08"
          }
       ],
    …
    }
    ```


## get-midservers

Retrieves detailed information about MID Servers, including status and validation details. Optionally, you can include MID Servers issue logs in the output.

-   **Command group**

    Parent group: discovery

-   **Roles required**

    discovery\_admin

    If using a service related to Discovery, you must have the required roles for that service.

-   **Command structure**

    ```
    snc discovery get-midservers [arguments]
    ```

-   **Argument**

    `--include-issues`: Includes issue logs with each MID Server. Possible values: True or false \(default: true\).

-   **Example**

    Retrieve details about the MID Servers by executing the following command:

    ```
    snc discovery get-midservers
    ```

    Retrieve a list of MID Servers and their issue logs by executing the command with the following argument:

    ```
    snc discovery get-midservers --include-issues=true
    ```

-   **Return value**

    ```
    ✔ MID Server details were fetched successfully.
    {
       "mid_servers": [
          {
             "home_directory": "C:\\Users\\admin\\Desktop\\midInstallationFolder\\agent",
             "host_name": "LocalLab",
             "host_os_version": "10.0.xxxx",
             "ip_address": "192.168.0.1",
             "issues": [],
             "last_refreshed": "2023-10-01 00:00:00",
             "name": "WindowsMidServer",
             "started": "2023-10-01 00:01:01",
             "status": "Up",
             "sys_id": "cb8d1625c3fdb110c72691477d01312e",
             "unresolved_issues": "0",
             "validated": "true",
             "validated_at": "2023-10-01 00:01:01"
          }
       ]
    }
    ```


## get-pattern-commands

Retrieves a comprehensive list of commands associated with a specified discovery pattern, identified by either its name or its sys\_id.

-   **Command group**

    Parent group: discovery

-   **Roles required**

    discovery\_admin

    If using a service related to Discovery, you must have the required roles for that service.

-   **Command structure**

    ```
    snc discovery get-pattern-commands [arguments]
    ```

-   **Argument**

    `--pattern`: Pattern name or sys\_id

-   **Examples**

    Retrieve a list of commands associated with the specified pattern by executing the command with either the pattern name or the sys\_id.

    -   Execute the command by entering the pattern name `Windows OS - Servers`:

        ```
        snc discovery get-pattern-commands --pattern="Windows OS - Servers"
        ```

    -   Execute the command by entering the pattern sys\_id `670e55a4db702200c06776231f961942`:

        ```
        snc discovery get-pattern-commands --pattern="670e55a4db702200c06776231f961942"
        ```

-   **Return value**

    ```
    ✔ Commands fetched successfully. 
    [
       {
          "Command": "\"\\root\\CIMV2\" \"SELECT Caption,IPAddress,MACAddress,DHCPEnabled,Index,InterfaceIndex,IPEnabled FROM Win32_NetworkAdapterConfiguration\"",
          "Command Type": "wmi",
          "sys_id": "2e677c4ec3adb1106618b10ad0013185"
       },
       {
          "Command": "\"\\root\\CIMV2\" \"SELECT Index,InterfaceIndex,Name,Manufacturer,NetConnectionID FROM Win32_NetworkAdapter\"",
          "Command Type": "wmi",
          "sys_id": "6a677c4ec3adb1106618b10ad0013185"
       },
       {
          "Command": "powershell -command \\Get-NetRoute -AddressFamily IPv6\\",
          "Command Type": "shell",
          "sys_id": "a6677c4ec3adb1106618b10ad0013185"
       },
       {
          "Command": "\"\\root\\CIMV2\" \"SELECT Destination,Mask,NextHop, InterfaceIndex FROM Win32_IP4RouteTable\"",
          "Command Type": "wmi",
          "sys_id": "e2677c4ec3adb1106618b10ad0013185"
       },
       {
          "Command": "\"\\root\\CIMV2\" \"SELECT DefaultIPGateway FROM Win32_NetworkAdapterConfiguration\"",
          "Command Type": "wmi",
          "sys_id": "e6677c4ec3adb1106618b10ad00131ab"
       },
    …
    ]
    ```


## get-patterns

Retrieves a comprehensive list of available discovery patterns.

-   **Command group**

    Parent group: discovery

-   **Roles required**

    discovery\_admin

    If using a service related to Discovery, you must have the required roles for that service.

-   **Command structure**

    ```
    snc discovery get-patterns
    ```

-   **Example**

    Retrieve a list of available discovery patterns by executing the following command:

    ```
    snc discovery get-patterns
    ```

-   **Return value**

    ```
    ✔ Details of Discovery Patterns successfully retrieved.
    [
       {
          "active": true,
          "ci_type": "cmdb_ci_appl_dot_net",
          "name": ".NET Application",
          "pattern_type": "1 - Application"
       },
       {
          "active": true,
          "ci_type": "cmdb_ci_lb_service",
          "name": "A10",
          "pattern_type": "1 - Application"
       },
       {
          "active": true,
          "ci_type": "cmdb_ci_lb_a10",
          "name": "A10 Load Balancer",
          "pattern_type": "3 - Infrastructure"
       },
       {
          "active": true,
          "ci_type": "cmdb_ci_lb_a10",
          "name": "A10 Load Balancer SSH",
          "pattern_type": "3 - Infrastructure"
       },
       {
          "active": true,
          "ci_type": "cmdb_ci_appl_generic",
          "name": "A10 SSH Hosting Formatting",
          "pattern_type": "2 - Shared library"
       },
       …
    ]
    ```


## midserver-action

Executes various actions on MID Servers, for example: stop, resume, or restart.

-   **Command group**

    Parent group: discovery

-   **Roles required**

    discovery\_admin

    If using a service related to Discovery, you must have the required roles for that service.

-   **Command structure**

    ```
    snc discovery midserver-action [arguments]
    ```

-   **Arguments**

<table id="table_fjl_klq_dzb"><thead><tr><th>

Argument

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`-m` or `--mid-server`

</td><td>

Name or sys\_id of the MID Server

</td></tr><tr><td>

`-a` or `--action`

</td><td>

Action to perform on the MID Server. The available options are:-   invalidate
-   resume
-   stop
-   pause
-   autoUpgrade
-   upgrade
-   restart
-   file\_discovery\_refresh
-   grab\_logs
-   validate


</td></tr></tbody>
</table>-   **Example**

    Perform an action on a MID Server with the following command:

    ```
    snc discovery midserver-action [options]
    ```

    Restart the MID Server `WinMidServer` by executing the following command:

    ```
    snc discovery midserver-action --mid-server="WinMidServer" --action="restart"
    ```

-   **Return value**

    ```
    ✔ Successfully submitted mid-server action
    {
       "Action": "restart",
       "MidServer": "cb8d1625c3fdb110c72691477d01312e",
       "Output": "Mid server restart in-progress."
    }
    
    ✔ Mid server action executed successfully
    restart executed successfully.
    ```


## quick-discovery

Executes a quick discovery against a specified configuration item \(CI\) or IP address.

**Note:** When the callback retries exceed the maximum limit, you might receive the following error message:

```
✗ Discovery Failed.
{
"CurrentActivity": "",
"DiscoveryStatus": {},
"State": "Active"
}
```

The message indicates that callback retries were exceeded but although discovery failed, it’s still running in the background. Check the discovery logs by either executing the command `snc discovery get-discovery-logs` or checking the ServiceNow® instance for updates on the discovery status.

-   **Command group**

    Parent group: discovery

-   **Roles required**

    discovery\_admin

    If using a service related to Discovery, you must have the required roles for that service.

-   **Command structure**

    ```
    snc discovery quick-discovery [arguments]
    ```

-   **Arguments**

<table id="table_xx2_bnq_dzb"><thead><tr><th>

Argument

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`--type`

</td><td>

Target host type: either IP or CI.

</td></tr><tr><td>

`--target`

</td><td>

Details of the target host. -   IP: IP address
-   CI: The available options are:
    -   Name
    -   Sys\_id
    -   Serial number


</td></tr><tr><td>

`--error-logs-only`

</td><td>

Includes error logs only. Possible values: true or false \(default: true\).

</td></tr></tbody>
</table>-   **Examples**

    Execute a quick discovery against a target entity using a specified criteria.

    ```
    snc discovery quick-discovery
    ```

    -   Execute a quick discovery against the IP address `192.168.1.100` by executing the following command and argument:

        ```
        snc discovery quick-discovery --type="ip" --target="192.168.1.100"
        ```

    -   Execute a quick discovery against the specified CI by executing the command with the name, sys\_id, or serial number.
        -   To execute a quick discovery against the CI name `ecommerce001`, enter:

            ```
            snc discovery quick-discovery --type="ci" --target="ecommerce001"
            ```

        -   To execute a quick discovery against the CI sys\_id `d0e8761137201000deeabfc8bcbe5da7`, enter:

            ```
            snc discovery quick-discovery --type="ci" --target="d0e8761137201000deeabfc8bcbe5da7"
            ```

        -   To execute a quick discovery against the CI serial number `L3BB911`, enter:

            ```
            snc discovery quick-discovery --type="ci" --target="L3BB911"
            ```

-   **Return value**

    ```
    snc discovery quick-discovery --type="ip" --target="192.168.1.100"
    ✔ Discovery job submitted
    Status Number: DIS0010054
    ✔ Discovery is complete
    {
       "DiscoveryLogs": [],
       "DiscoveryStatus": [
          {
             "Completed": "5",
             "Created": "2023-10-17 10:59:52",
             "Description": "Discover CI",
             "Discover": "CIs",
             "Duration": "1970-01-01 00:01:41",
             "Number": DIS0010054,
             "Schedule": "",
             "Started": "5",
             "State": "Completed",
             "Updated": "2023-10-17 11:02:06"
          }
       ],
       "State": "Completed"
    }
    ```


## run-command

Executes commands on remote devices using specified credentials, targets, and MID Servers.

-   **Command group**

    Parent group: discovery

-   **Roles required**

    discovery\_admin

    If using a service related to Discovery, you must have the required roles for that service.

-   **Command structure**

    ```
    snc discovery run-command [arguments]
    ```

-   **Arguments**

    |Argument|Description|
    |--------|-----------|
    |`--command`|Command to be executed.|
    |`--command-type`|Operation type to be performed.|
    |`--credential`|Credential used to execute the command.|
    |`--midserver`|Name of the MID Server used to communicate with the target.|
    |`--os-server`|CI class that represents the server operating system \(server OS\) on which to run the commands. For example, enter cmdb\_ci\_linux\_server for the Linux server.|
    |`--target`|Host IP address on which you want to run the command.|

-   **Example**

    Execute the following command to have the Windows Management Instrumentation \(`WMI`\) query ask the system to retrieve the **UUID** and **IdentifyingNumber** properties from the Win32\_ComputerSystemProduct class in the `\root\CIMV2` namespace:

    ```
    snc discovery run-command --command="\"\\root\\CIMV2\" \"SELECT UUID,IdentifyingNumber FROM Win32_ComputerSystemProduct\"" --command-type="wmi" --credential="WinCred" --midserver="WinMidServer" --os-server="cmdb_ci_win_server" --target="192.168.1.1"
    ```

-   **Return value**

    ```
    ✔ The command is sent for execution.
    {
    "eccQueueOutputSysId": "9a3c55a3c33db910c72691477d0131cd"
    }
    
    ✔ Command Executed Successfully...
    {
    "result": {
    "IdentifyingNumber": "VMware-00 00 00 00 00 00 00 00-00 00 00 00 00 00 00 00",
    "Name": "VMware Virtual Platform",
    "Object Reference": null,
    "UUID": "61410042-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
    "Version": "None",
    "__CLASS": "Win32_ComputerSystemProduct",
    "internal_classname": "Win32_ComputerSystemProduct",
    "internal_namespace": "root/cimv2"
    }
    }
    ```


## test-discovery-credential

Validates the discovery credentials against a specified target system using a designated MID Server. The command checks only credential readiness for network discovery tasks. It doesn't modify or affect the configuration of either the discovery credential or the target system.

**Important:**

This command requires a specific XML file to have been imported into the Module Access Policy list. For more information, see the [Discovery CLI \[KB1553142\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1553142) article in the Now Support Knowledge Base.

-   **Command group**

    Parent group: discovery

-   **Roles required**

    discovery\_admin

    If using a service related to Discovery, you must have the required roles for that service.

-   **Command structure**

    ```
    snc discovery test-discovery-credential [arguments]
    ```

-   **Arguments**

<table id="table_hfm_nxv_dzb"><thead><tr><th>

Argument

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`--dbname`

</td><td>

Name of the database on which to test these credentials.

</td></tr><tr><td>

`--dbtype`

</td><td>

Type of database on which to test these credentials. The available options are: -   MSSQL—for Microsoft SQL Server
-   MySQL
-   Oracle


</td></tr><tr><td>

`--icf`

</td><td>

Name of the Java Naming and Directory Interface \(JNDI\) class that is used to create the InitialContext. The name of the JNDI class must include first the package name and then the class name. For example, to connect to the ActiveMQ JNDI class, you would enter: `org.apache.activemq.jndi.ActiveMQInitialContextFactory`.

</td></tr><tr><td>

`--midserver`

</td><td>

Name of the MID Server to use for this test. To test Windows credentials, you must use a Windows MID Server.

</td></tr><tr><td>

`--name`

</td><td>

Name of the credential.

</td></tr><tr><td>

`--port`

</td><td>

Port on the target to use for this test. The system pre-populates this field with the default port for the selected credential type.

</td></tr><tr><td>

`--target`

</td><td>

Target host on which these credentials are run. This value must be an IP address for all credential types except VMware, for which the value can be the host URL.

</td></tr></tbody>
</table>-   **Example**

    Test the discovery credential `WinCred` against MID Server `WinMidServer` by executing the following command:

    ```
    snc discovery test-discovery-credential --name="WinCred" --target="192.168.1.1" --midserver="WinMidServer"
    ```

    The command returns a success message when the following conditions are met:

    -   The credential is valid
    -   The connection to the target system is successful
    -   The specified MID Server is operational
    If these conditions aren’t met, an error message detailing the issues is displayed.

-   **Return value**

    ```
    ✔ Discovery credentials tested successfully
    Credential Test Id [ecc-sys-id]: "2b36e40ec3727990c72691477d0131c6"
    ✔ The credential test is complete
    {
       "output": "Test Succeeded"
    }
    ```


For more information about Discovery CLI, see the [Discovery CLI \[KB1553142\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1553142) article in the Now Support Knowledge Base.

**Parent Topic:**[Discovery reference](discovery-references.md)


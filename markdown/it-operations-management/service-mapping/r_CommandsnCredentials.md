---
title: Service Mapping commands requiring a privileged user
description: Service Mapping uses commands requiring elevated rights to discover and map Unix-based hosts in your organization. In addition to configuring necessary credentials, configure servers in your organization to allow Service Mapping to run these commands with elevated rights.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 16
breadcrumb: [Prerequisites for performing top-down discovery using Service Mapping, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service Mapping commands requiring a privileged user

Service Mapping uses commands requiring elevated rights to discover and map Unix-based hosts in your organization. In addition to configuring necessary credentials, configure servers in your organization to allow Service Mapping to run these commands with elevated rights.

You do not run these commands directly. Service Mapping uses commands requiring elevated rights as part of the following processes:

-   host detection
-   process identification on port
-   discovering CIs using patterns

Some of these commands do not require elevated rights, unless directories that Service Mapping must access are protected. For more information, see [Service Mapping commands not requiring a privileged user](r_NonSudoCommands.md).

## Operating system commands requiring elevated rights

<table id="table_cwj_cjz_j5"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`cat`

</td><td>

**file-name**

</td><td>

Shows the file content.

</td></tr><tr><td>

`ls`

</td><td>

**-F-1**

 **-1HF**

 **-w 1**

 **-1**

</td><td>

Lists the directory content.

</td></tr><tr><td>

`procwdx`

</td><td>

**Process\_id**

</td><td>

Gets working directory of a process.

</td></tr><tr><td>

`rmsock`

</td><td>

**Socketname tcpcp**

</td><td>

Finds process listening on a specific port.

</td></tr><tr><td>

`lsof`

</td><td>

**-Pnl +M -i**

</td><td>

Shows files or connections associated with the process.

</td></tr><tr><td>

`lstat`

</td><td>

Various options

</td><td>

Fetches information about a link.

</td></tr><tr><td>

`ps`

</td><td>

**eww**

</td><td>

Fetches environment variables for the process on AIX.

</td></tr></tbody>
</table><table id="table_frk_skz_j5"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`cat`

</td><td>

**file-name**

</td><td>

Shows the file content.

</td></tr><tr><td>

`ls`

</td><td>

**-F-1**

 **-1HF**

 **-w 1**

 **-1**

</td><td>

Lists the directory content.

</td></tr><tr><td>

`pfiles`

</td><td>

**Process\_id**

</td><td>

Shows files or connections associated with the process.

</td></tr><tr><td>

`lsof`

</td><td>

**-Pnl +M -i**

</td><td>

Shows files or connections associated with the process.

</td></tr></tbody>
</table><table id="table_fkb_2mz_j5"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`cat`

</td><td>

**File\_name**

</td><td>

Shows the file content.

</td></tr><tr><td rowspan="2">

`ls`

</td><td>

**ls -F-1**

 **ls -1HF**

 **ls -w 1**

 **ls -1**

</td><td>

Lists the directory content.

</td></tr><tr><td>

**e-l**

</td><td>

Fetches file attributes used for file caching decision.

</td></tr><tr><td>

`pargs`

</td><td>

**-e**

</td><td>

Gets the executable directory.

</td></tr><tr><td>

`pargs`

</td><td>

**-a**

</td><td>

Gets the process.

</td></tr><tr><td>

`lsof`

</td><td>

**-Pnl +M -i**

</td><td>

Shows files and connections associated with the process.

</td></tr><tr><td>

`netstat`

</td><td>

**-anu**

</td><td>

Lists the open ports. Required for Solaris version 11.2 or later.

</td></tr><tr><td>

`Ifconfig`

</td><td>

**Ifconfig -a**

</td><td>

Shows interface information \(need sudo to get the MAC addresses\).

</td></tr><tr><td>

`pwdx`

</td><td>

**Process\_id**

</td><td>

Gets the process information.

</td></tr><tr><td>

`pargs`

</td><td>

**-e process\_id**

</td><td>

Gets the process information.

</td></tr><tr><td>

`ps`

</td><td>

**-eo user, pid, ppid, comm, args**

</td><td>

Gets the process list.

</td></tr><tr><td>

`inetadm`

</td><td>

**-l or without params**

</td><td>

Handles the case of application using the inet daemon.

</td></tr></tbody>
</table><table id="table_hbb_vtz_j5"><thead><tr><th>

Commands

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`cat`

</td><td>

**File\_name**

 **scsi**

 **tr '\\\\n'**

 **/proc**

 **/proc/cpuinfo**

 **sys**

 **sys/hypervisor**

 **sys/hypervisor/compilation**

 **sys/hypervisor/compilation/compiled by**

</td><td>

Shows information about file content.

</td></tr><tr><td>

`cut`

</td><td>

**-d**

 **-f1**

</td><td>

Shows the entire output of a file.

</td></tr><tr><td>

`dmidecode`

</td><td>

**-t 17**

 **-s bios-vendor**

 **-t 1**

 **-t 2**

 **-t 3**

</td><td>

Shows information about hardware of the Linux server in a readable format.

</td></tr><tr><td>

`lshw`

</td><td>

 

</td><td>

Shows information about hardware of the Linux server in a readable format.

</td></tr><tr><td>

`ls`

</td><td>

**ls -F-1**

 **ls -1HF**

 **ls -w 1**

 **ls -1**

 **ls -l**

</td><td>

Lists directory content.

</td></tr><tr><td>

`netstat`

</td><td>

**-ltnup**

 **-ltnp**

 **-ntup**

 **-an**

</td><td>

Shows the open network connections.

</td></tr><tr><td>

`Isof`**Note:** Used in some cases as an alternative to netstat.

</td><td>

**-Pnl +M -i**

</td><td>

Shows files and connections associated with the process.

</td></tr><tr><td>

`ss`

</td><td>

**-ltnup**

 **-ntup**

 **-an**

</td><td>

Shows the open network connections.

</td></tr><tr><td>

`stat`

</td><td>

**--format="%Y"**

 **-L file\_name**

</td><td>

Shows the modification time of the file.

</td></tr><tr><td>

`fdisk`

</td><td>

**-l**

</td><td>

Displays all disk partitions

</td></tr></tbody>
</table>## Application commands requiring elevated rights

Service Mapping uses some of these commands in patterns.

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|
|`ls`|Various options|Lists files and folders in the specified folder.|

<table id="table_zll_fwl_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`grep`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr><tr><td>

`ls`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`cat`

</td><td>

**-**

</td><td>

Shows the file content.

</td></tr><tr><td>

`netstat`

</td><td>

Various options

</td><td>

Lists the open ports.

</td></tr><tr><td>

`ss`

</td><td>

Various options

</td><td>

Lists open ports.

</td></tr><tr><td>

`find`

</td><td>

**-name**

</td><td>

This command is used only for creating the web services connections. Finds specific strings in files and folders.

</td></tr></tbody>
</table><table id="table_j1y_fwl_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`grep`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr><tr><td>

`ls`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`cat`

</td><td>

**-**

</td><td>

Shows the file content.

</td></tr><tr><td>

`version.sh/version.bat`

</td><td>

**-**

</td><td>

Gets the Tomcat version.

</td></tr><tr><td>

`netstat`

</td><td>

Various options

</td><td>

Lists the open ports.

</td></tr><tr><td>

`ss`

</td><td>

Various options

</td><td>

Lists open ports.

</td></tr><tr><td>

`find`

</td><td>

**-name**

</td><td>

This command is used in connection sections of the pattern for discovering Apache Tomcat WAR connections. Finds specific strings in files and folders.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|
|`grep`|Various options|Extracts strings from the output.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`ping`|**-a -c 1 \[url\[1\].host\]**|Gets the host IP.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|

<table id="table_mbs_1y2_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`grep`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr><tr><td>

`find`

</td><td>

Various options

</td><td>

This command is used only to create connections to Control M Server.Finds file and folder paths.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`show`|Various options|Retrieves Netscaler IP address.|

<table id="table_ivx_1yy_lz"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`find`

</td><td>

Various options

</td><td>

Finds connections to Docbase.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|\(On Unix only\) Extracts strings from the output.|
|`ls`|Various options|\(On Unix only\) Lists files and folders in the specified folder.|
|`cat`|**-**|\(On Unix only\) Shows the file content.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|
|`grep`|Various options|Extracts strings from the output.|

<table id="table_cmw_1y2_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`grep`

</td><td>

Various options

</td><td>

\(For Unix only\) Extracts strings from the output.

</td></tr><tr><td>

`find`

</td><td>

Various options

</td><td>

\(For Unix only\)Finds file and folder paths.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|\(For Unix only\) This command is used only to create CICS connections. Extracts strings from the output.|
|`cat`|**-**|\(For Unix only\) This command is used only to create CICS connections. Displays the file content in the output.|
|`find`|Various options|\(For Unix only\) This command is used only to create CICS connections. Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`cat`|**-**|Displays the file content in the output.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|
|`find`|**-name**|Finds files and folders in the specified folder.|

<table id="table_mym_3wl_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`grep`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr><tr><td>

`ls`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`cat`

</td><td>

**-**

</td><td>

Shows the file content.

</td></tr><tr><td>

`find`

</td><td>

**-name**

 **-type**

</td><td>

This command is used only for creating the Web Services connections. Finds files and folders for the specific name.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|
|`netstat`|Various options|Lists the open ports.|
|`ss`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|
|`ps`|**-ef**|Gets the process information.|
|`netstat`|Various options|Lists the open ports.|
|`ss`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`ps`|**-ef**|Gets the process information.|
|`netstat`|Various options|Lists the open ports.|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`ls`|Various options|\(On Unix only\) Lists files and folders in the specified folder.|
|`grep`|Various options|Extracts strings from the output.|
|`dir`|Various options|\(On Windows only\) Lists files and folders in the specified folder.|
|`find`|Various options|\(For Windows only\) Finds specific strings in files and folders.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`grep`|Various options|Extracts strings from the output.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`Get-ExchangeServer`|**-status -Identity "+$hostname+"\| export-clixml $env:TEMP\\exchange\_pwrshell\_output.xml**|Extracts the list of Microsoft Exchange hosts and role|
|`Get-ExchangeServer`|**format-table -autosize -HideTableHeaders Name,Fqdn,IsMailboxServer**|Extracts the list of Microsoft Exchange hosts and role in table format|
|`Get-MailboxServer`|**format-list**|Extracts the list of Microsoft Exchange Mailbox servers.|
|`Get-ClusteredMailBoxServerStatus`|**format-table -Property OperationalMachines**|Extracts information about Microsoft Exchange Mailbox clusters.|
|`Get-ExchangeServer`|**format-table -autosize -HideTableHeaders Name,Fqdn,IsHubTransportServer**|Extracts information on Microsoft Exchange Hub Transport servers|
|`Get-StorageGroup`|**-server "+$hname+" \| select SystemFolderPath \| Export-Csv out.csv -notype;cat out.csv**|Extracts information about storage and exports it into a file.|
|`Get-MailboxDatabase`|**\| select LogFolderPath \| format-table -autosize -hideTableHeaders; Get-MailboxDatabase \| select EdbFilePath\| format-table -autosize -hideTableHeaders;Get-MailboxDatabase \| select TemporaryDataFolderPath\| format-table -autosize -hideTableHeaders**|Extracts information about the Microsoft Exchange Mailbox database.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|\(On Unix only\) Extracts strings from the output.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|
|`ps`|**--pid=\[process.pid\] --no-headers -o " %U : %p : %a”**|Gets the userid parameter value.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|
|`ps`|**--pid=\[process.pid\] --no-headers -o " %U : %p : %a”**|\(On Unix only\) Gets the userid parameter value.|

<table id="table_thl_2nk_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`netstat`

</td><td>

Various options

</td><td>

Lists open ports.

</td></tr><tr><td>

`ss`

</td><td>

Various options

</td><td>

Lists open ports.

</td></tr><tr><td>

`ps`

</td><td>

**--pid=\[process.pid\] --no-headers -o " %U : %p : %a”**

</td><td>

Gets the userid parameter value.

</td></tr><tr><td>

`ls`

</td><td>

**\[IncludeTabletmp\[\].files\]**

</td><td>

This command is used if necessary to create HTTP connections. Lists files and folders in the specified folder.

</td></tr><tr><td>

`cat`

</td><td>

**\[IncludeTabletmp\[\].files\]**

</td><td>

This command is used if necessary to create HTTP connections.Shows the file content.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`grep`|Various options|Extracts strings from the output.|
|`export`|**-**|Sets variables.|
|`echo`|Various options|Prints strings in the output.|
|`sqlplus`|Various options|Creates the connection to the Oracle instance.|
|`awk`|Various options|Manipulates the output.|
|`netstat`|Various options|Gets open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|\(For Unix only\) Extracts strings from the output.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|
|`awk`|Various options|\(For Unix only\) Manipulates the output.|
|`ls`|Various options|\(For Unix only\) Lists files and folders in the specified folder.|
|`cat`|**-**|\(For Unix only\) Displays the file content in the output.|
|`find`|Various options|Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`grep`|Various options|Extracts strings from the output.|
|`cat`|**-**|Shows the file content.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`grep`|Various options|Extracts strings from the output.|
|`cat`|**-**|Shows the file content.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|
|`ps`|**-ef**|Gets the process information.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|\(For Unix only\) Lists files and folders in the specified folder.|
|`cat`|**-**|\(For Unix only\) Shows the file content.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|

<table id="table_k1y_fwl_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`grep`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr><tr><td>

`ls`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`cat`

</td><td>

**-**

</td><td>

Shows the file content.

</td></tr><tr><td>

`find`

</td><td>

**-name**

 **-type**

</td><td>

This command is used only for creating the Web Services connections. Finds files and folders for the specific name.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**-**|Shows the file content.|

<table id="table_mnv_5jp_55"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`grep`

</td><td>

Various

</td><td>

Extracts strings from the output

</td></tr><tr><td>

`ls`

</td><td>

Various

</td><td>

Lists files and folders on the given folder.

</td></tr><tr><td>

`cat`

</td><td>

**-**

</td><td>

Displays the file content in the output.

</td></tr><tr><td>

`find`

</td><td>

**-name**

</td><td>

This command is used only to create web service connections.

Finds files and folders for specific name.

</td></tr><tr><td>

`netstat`

</td><td>

Various

</td><td>

Gets open ports.

</td></tr><tr><td>

`ss`

</td><td>

Various options

</td><td>

Lists open ports.

</td></tr><tr><td>

`ps`

</td><td>

**-ef**

</td><td>

\(For Unix only\) Gets process attributes.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various|Extracts strings from the output|
|`ls`|Various|Lists files and folders on the given folder.|
|`cat`|**-**|Displays the file content in the output.|

<table id="table_cgq_fnk_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`ls`

</td><td>

**\[IncludeTabletmp\[\].files\]**

</td><td>

This command is used only to create the HTTP connections.Lists files and folders in the specified folder.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`ps - ef`|**ps -ef \| grep "+$process.parentProcessId+" \|egrep -v -e grep -e beam**|Gets the parent process.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`clustat`|**-x**|Displays the cluster configuration and the status in XML format.|

<table id="id_unw_5zc_qrb"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`pargs`

</td><td>

**-e**

</td><td>

Gets the executable directory.

</td></tr><tr><td>

`ls`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`ping`

</td><td>

**-c 1**

</td><td>

Verifies that the host is answering.

</td></tr><tr><td>

`netstat`

</td><td>

Various options

</td><td>

Lists open ports.

</td></tr><tr><td>

`Isof`**Note:** Used in some cases as an alternative to netstat.

</td><td>

**-Pnl +M -i**

</td><td>

Shows files and connections associated with the process.

</td></tr><tr id="SAPCommands-CVERS"><td>

`CVERS`

</td><td>

**-**

</td><td>

Retrieves the version of installed SAP modules.

</td></tr><tr id="SAPCommands-DBCONS"><td>

`DBCONS`

</td><td>

**-**

</td><td>

Retrieves the connection strings to SAP DB.

</td></tr><tr id="SAPCommands-RFCDES"><td>

`RFCDES`

</td><td>

**-**

</td><td>

Retrieves the connection string to systems integrated with SAP.

</td></tr><tr><td>

`sapcontrol`

</td><td>

**-function ABAPGetComponentList**

</td><td>

Retrieves the sysid for SAP applications and components.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`netstat`|Various options|Lists the open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`netstat`|Various options|Lists the open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`grep`|Various options|Extracts strings from the output.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`ls`|Various options|Lists files and folders in the specified folder.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`cat`|**-**|Shows the file content.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`hostname`|**-**|Gets the hostname.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`grep`|Various options|Extracts strings from the output.|
|`cat`|**-**|Shows the file content.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|

<table id="table_avh_x1y_n5"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`hostname`

</td><td>

**-**

</td><td>

Gets the hostname.

</td></tr><tr><td>

`ls`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`grep`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr><tr><td>

`cat`

</td><td>

**-**

</td><td>

Shows the file content.

</td></tr><tr><td>

`findstr`\(for Windows\)

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr><tr><td>

`netstat`

</td><td>

Various options

</td><td>

Lists open ports.

</td></tr><tr><td>

`ss`

</td><td>

Various options

</td><td>

Lists open ports.

</td></tr><tr><td>

`cut`

</td><td>

Various options

</td><td>

Splits the output line.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`ls`|Various options|Lists files and folders in the specified folder.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`ls`|Various options|Lists files and folders in the specified folder.|

**Parent Topic:**[Prerequisites for performing top-down discovery using Service Mapping](prerequisites-service-mapping.md)

**Related topics**  


[Service Mapping commands not requiring a privileged user](r_NonSudoCommands.md)


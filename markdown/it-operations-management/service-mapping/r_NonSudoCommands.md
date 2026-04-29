---
title: Service Mapping commands not requiring a privileged user
description: Most of commands utilized by Service Mapping for discovery and mapping do not require elevated rights.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 40
breadcrumb: [Prerequisites for performing top-down discovery using Service Mapping, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service Mapping commands not requiring a privileged user

Most of commands utilized by Service Mapping for discovery and mapping do not require elevated rights.

Review this list of commands to understand how Service Mapping uses them and to make sure that the virtual security of your company is not compromised.

You do not run these commands directly. Service Mapping uses commands requiring elevated rights as part of the following processes:

-   host detection
-   process identification on port
-   discovering CIs using patterns

## Operating systems

<table id="table_cwj_cjz_j5"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`awk`

</td><td>

various options

</td><td>

Parses the string.

</td></tr><tr><td>

`istat`

</td><td>

**file\_name**

</td><td>

Gets last modification time of file.

</td></tr><tr><td>

`nslookup`

</td><td>

**hostname**

</td><td>

Resolve DNS host name.

</td></tr><tr><td>

`ping`

</td><td>

**-c count ip/host**

</td><td>

Pings the host.

</td></tr><tr><td>

`arp -an`

</td><td>

various options

</td><td>

Shows ARP table.

</td></tr><tr><td>

`grep`

</td><td>

String to search

</td><td>

Finds string in previous command output.

</td></tr><tr><td>

`traceroute`

</td><td>

**-n ip\_address**

</td><td>

Shows layer 3 network route to target host.

</td></tr><tr><td>

`netstat`

</td><td>

**-an**

 **-Aan**

</td><td>

Shows open network connections.

</td></tr><tr><td>

`ps`

</td><td>

**-eo user, pid, ppid, comm, args**

</td><td>

Gets the process list.

</td></tr><tr><td>

`find`

</td><td>

Directory and parameters to search

</td><td>

Searches for files by name or type.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`ping`|**-c count ip/host**|Pings the host.|
|`arp -an`| |Shows the ARP table.|
|`grep`|String to search|Finds string in previous command output.|
|`awk`|various options|Parses the string.|
|`traceroute`|**-n ip\_address**|Shows layer 3 network route to target host.|
|`netstat`|**-an**|Shows open network connections.|
|`ps`|**-eo user, pid, ppid, comm, args**|Gets the process list.|
|`find`|Directory and parameters for search|Searches for files by name or type.|

|Commands|Parameter|Description|
|--------|---------|-----------|
|`sysvar`|**SYSNAME**|Gets the system name.|
|`hostname`| |Retrieves the device name.|
|`grep`|String to search|Finds the string in command output.|
|`hostname`|**-**|Gets the hostname.|
|`netstat`|**-g \| awk '\{if \(NR&gt;4\) print \\$1,\\$3\}'**|Gets network information.|
|`netstat`|**-r \| awk '\{if \(NR&gt;3\) print \\$1,\\$2,\\$5\}'**|Gets gateway information.|
|`netstat`|**-h \| awk '\{if \(NR&gt;4\) print \\$1\}' \| grep -v '127.0.0.1'**|Gets IP array.|
|`netstat`|**-R ALL \| awk '\{if \(NR&gt;1\) print \\$0\}'**|Gets interfaces.|
|`netstat`|**df -k \| awk '\{print \\$1,\\$2\}' \|sed -e s'/\(//' \| sed -e s'/\)//' 2&gt; /dev/null**|Gets the file system information.|
|`ps`|**-**|Gets the process list.|
|`ls`|Various options|Lists files and folders in the specified folder.|
|`cat`|**file-name**|Shows the file content.|
|`cut`|Various options|Splits the output according to entered parameters.|
|`uname`|**l, v, rm, s**|Gets the OS type.|

<table id="table_nss_llv_p5"><thead><tr><th>

Commands

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`nslookup`

</td><td>

**hostname**

</td><td>

Resolves the DNS host name.

</td></tr><tr><td>

`ping`

</td><td>

**-c count ip**

 **host**

</td><td>

Pings the host.

</td></tr><tr><td>

`arp`

</td><td>

**-an/n**

</td><td>

Shows the ARP table.

</td></tr><tr><td>

`lp n`

</td><td>

**-an/n**

</td><td>

Shows the ARP table.

</td></tr><tr><td>

`grep`

</td><td>

String to search

 **-v**

 **hypervisor**

 **proc**

 **cpuinfo**

 **-i 'attached scsi'**

 **var**

 **log**

 **dmesg**

 **'SCSI device'**

 **'Disk**

 **UUID**

</td><td>

Finds the string in previous command output.

</td></tr><tr><td>

`awk`

</td><td>

Various options

</td><td>

Parses the string.

</td></tr><tr><td>

`netstat`

</td><td>

**-an**

</td><td>

Shows open network connections.

</td></tr><tr><td>

`ss`

</td><td>

**-an**

</td><td>

Shows open network connections.

</td></tr><tr><td>

`ps`

</td><td>

**-eo user, pid, ppid, comm, args, wwwx**

</td><td>

Gets the process list.

</td></tr><tr><td>

`egrep`

</td><td>

Various options

</td><td>

Searches text in previous command output.

</td></tr><tr><td>

`find`

</td><td>

Directory and parameters for search

</td><td>

Searches for files by name or type.

</td></tr><tr><td>

`traceroute`

</td><td>

**-n ip\_address**

</td><td>

Shows the layer 3 network route to target host.

</td></tr><tr><td>

`df`

</td><td>

**-kP, echo**

</td><td>

Extracts the information about the file system, including the size in KB.

</td></tr><tr><td>

`uptime`

</td><td>

Various options

</td><td>

Shows the current time, how long the system has been running, how many users are currently logged on, and the system load averages for the past 1, 5, and 15 minutes.

</td></tr><tr><td>

`date`

</td><td>

Various options

</td><td>

Displays the date in the time zone on which Linux operating system is configured.

</td></tr><tr><td>

`perl`

</td><td>

**-e 'print time**

</td><td>

Opens the Perl shell and prints time.

</td></tr><tr><td>

`command`

</td><td>

**-v vxprint**

</td><td>

This command is used in the Debug mode.

</td></tr><tr><td>

`uname`

</td><td>

**-a**

 **-r**

</td><td>

Displays the information about the system.

</td></tr><tr><td>

`ipfconfig`

</td><td>

**-a**

</td><td>

Shows the configuration of the network interface.

</td></tr><tr><td>

`ip`

</td><td>

route list

 **-4 -o addr show**

 **-6 -o a**

 **r**

 String to parse

</td><td>

Displays information about network interface, including the routing table.

</td></tr><tr><td>

`route`

</td><td>

**-n**

</td><td>

Shows the IP routing table.

</td></tr><tr><td>

`ip r`

</td><td>

 

</td><td>

Shows the IP routing table.

</td></tr><tr><td>

`sed`

</td><td>

**-n '2!p'**

</td><td>

Executes a function using the SED stream editor.

</td></tr><tr><td>

`bash`

</td><td>

**-c**

</td><td>

Executes the command using the UNIX shell or command language.

</td></tr><tr><td>

`waagent`

</td><td>

**-version 2&gt;/dev/null**

</td><td>

Displays the information extracted from the Microsoft Azure Linux agent.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`nslookup`|**hostname**|Resolves the DNS host name.|
|`ping`|**-c count ip/host**|Pings the host.|
|`arp`|**-an**|Shows the ARP table.|
|`grep`|String to search|Finds the string in previous command output.|
|`awk`|Various options|Parses the string.|
|`traceroute`|**-n ip\_address**|Shows the layer 3 network route to target host.|
|`netstat`|**-an**|Shows the open network connections.|
|`zoneadm`|**List**|Shows the list of zones.|
|`egrep`|Various options|Searches text in previous command output.|
|`find`|Directory and parameters|Searches for files by name or type.|

|Query|Description|
|-----|-----------|
|`Select * from Win32_ComputerSystem`|Gets the server basic information like serial number.|
|`Select LastModified from CIM_LogicalFile Where Name=...`|Gets the last modification time of a file.|
|`Select AddressWidth from Win32_Processor`|Gets the computer architecture \(32 bit or 64 bit\).|
|`Select * From Win32_Process where (ProcessId = ?)`|Gets the process list running on the computer.|
|`Select Name from CIM_LogicalDisk`|Gets the file systems on the computer, such as C: or D:.|
|`Select FileName, Extension from CIM_Directory where Drive=’drive’ and Path='path'`|Gets the list of files in a specific directory.|

<table id="table_cqd_svz_j5"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`get_process_info.exe`

</td><td>

**Process\_id**

</td><td>

Extracts information on the processes using executable created by ServiceNow.

</td></tr><tr><td>

`type`

</td><td>

**File\_name**

</td><td>

Shows the text file content.

</td></tr><tr><td>

`nslookup`

</td><td>

**Host\_name**

</td><td>

DNS lookup

</td></tr><tr><td>

`arp`

</td><td>

**-a**

</td><td>

Shows the ARP table.

</td></tr><tr><td>

`netstat`

</td><td>

**-ano**

</td><td>

Shows the network connections.

</td></tr><tr><td>

`findstr`

</td><td>

Various options

</td><td>

Finds the string in the previous command output.

</td></tr><tr><td>

`dir`

</td><td>

**/q**

 **/s /b**

</td><td>

Lists files in the directories.

</td></tr><tr><td>

`paping`

</td><td>

**--nocolor -c 1 -p**

 **port\_num**

 **ip\_address**

</td><td>

Utility to run TCP ping against given host.

</td></tr><tr><td>

`ping`

</td><td>

**-n 1**

 **ip\_address/host**

</td><td>

Pings the host.

</td></tr><tr><td>

`tracert`

</td><td>

**Ip\_address**

</td><td>

Shows the layer 3 network route to the target host.

</td></tr></tbody>
</table>## Applications

|Command|Parameter|Description|
|-------|---------|-----------|
|`show partition`|Various options|Get the partition configured.|
|`sh-run all-partitions`|Various options|Get details like virtual-server, port, service group, and pool members information.|
|`show slb virtual-server all-partitions`|Various options|Get the status of the virtual server and hit count details.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|\(For Windows only\) Lists files and folders in the specified folder.|
|`msg_server`|**-V**|Gets the version.|
|`ping`|**-n 1**|\(For Windows only\) Verifies that the host is answering.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`netstat`|Various options|Gets open ports on|
|`ss`|Various options|Lists open ports.|
|`hostname`|**-**|Gets the hostname.|
|`dir`|Various options|Lists all files in the specified folder.|

<table id="table_z5m_x1y_n5"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`httpd`

</td><td>

**-V**

</td><td>

Gets the version.

</td></tr><tr><td>

`cut`

</td><td>

Various options

</td><td>

Splits the output line.

</td></tr><tr><td>

`opmnctl`

</td><td>

**status -fmt %cmp32%prt32%por40%pid**

 and

 **@farm status -noheaders -fsep "\|" -fmt %cmp%prt%clu%ins%por**

</td><td>

This command is used only for discovering the OC4J connectivity.Gets the status of the OPMN CTRL service.

</td></tr><tr><td>

`sort`

</td><td>

**-u**

</td><td>

This command is used only for discovering the Weblogic connectivity. Sorts the output.

</td></tr></tbody>
</table><table id="table_iln_xx2_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`httpd.exe`

</td><td>

**-V**

</td><td>

Gets the version.

</td></tr><tr><td>

`opmnctl`

</td><td>

**status -fmt %cmp32%prt32%por40%pid**

 and

 **@farm status -noheaders -fsep "\|" -fmt %cmp%prt%clu%ins%por**

</td><td>

This command is used only for discovering the OC4J connectivity.Gets the status of the OPMN CTRL service.

</td></tr></tbody>
</table><table id="table_zll_fwl_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`dir`

</td><td>

Various options

</td><td>

\(On Windows only\) Lists files and folders in the specified folder.

</td></tr><tr><td>

`findstr`

</td><td>

Various options

</td><td>

\(On Windows only\) Extracts strings from the output.

</td></tr><tr><td>

`find`

</td><td>

Various options

</td><td>

\(For Windows only\) Finds specific strings in files and folders.

</td></tr><tr><td>

`find`

</td><td>

**-name**

</td><td>

Creates the web services connections. Finds specific strings in files and folders.

</td></tr><tr><td>

`version.sh/version.bat`

</td><td>

**-**

</td><td>

Gets the Tomcat version.

</td></tr><tr><td>

`java -cp " + $install_directory + "/lib/catalina.jar org.apache.catalina.util.ServerInfo`

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

`find`

</td><td>

**-name**

</td><td>

This command is used only for creating the web services connections. Finds specific strings in files and folders.

</td></tr><tr><td>

`ss`

</td><td>

Various options

</td><td>

\(For Linux only\) Lists the open ports.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|\(On Windows only\) Lists files and folders in the specified folder.|
|`findstr`|Various options|\(On Windows only\) Extracts strings from the output.|
|`find`|Various options|\(For Windows only\) Finds specific strings in files and folders.|
|`version.sh/version.bat`|**-**|Gets the Tomcat version.|
|`netstat`|Various options|\(Windows only\) Lists the open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|\(On Windows only\) Lists files and folders in the specified folder.|
|`netstat`|Various options|\(On Windows only\) Lists open ports.|
|`grep`|Various options|\(On Windows only\) Extracts strings from the output.|

<table id="table_bpb_m3p_55"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`show`

</td><td>

**/gtm pool \[wide\_ip\_pool\_4\_cmd\[1\].pool\] members**

</td><td>

This command is used only to create connections to pool members.

Gets the pool members.

</td></tr><tr><td>

`list`

</td><td>

**/gtm server \[servers\_from\_cmd\[\].server\] addresses**

</td><td>

This command is used only to create connections to pool members.

Lists the alias server addresses.

</td></tr></tbody>
</table><table id="table_d42_2kf_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`b`

</td><td>

**rule \[rule name\] list**

and

**virtual address \[entry\_point.ip\_address\]**

</td><td>

This command is used only for creating connections from rules.Lists existing rules on BIGPipe.

</td></tr><tr><td>

`list`

</td><td>

**ltm rule \[rule name\]**

 and

 **data-group wts\_routing\_destination\_prod \| grep -A 1 \[ep\_uri\]**

</td><td>

This command is used only for creating connections from rules.Lists existing rules on TMSH.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`show cm traffic-group – get`|Various options|This command is used to get traffic and clustering information.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`findstr`|Various options|\(For Windows only\) Extracts strings from the output.|
|`netstat`|Various options|\(For Windows only\) Lists open ports.|

<table id="table_mbs_1y2_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`findstr`

</td><td>

Various options

</td><td>

\(For Windows only\) Extracts strings from the output.

</td></tr><tr><td>

`dir`

</td><td>

Various options

</td><td>

\(For Windows only\) Lists files and folders in the specified folder.

</td></tr><tr><td>

`find`

</td><td>

Various options

</td><td>

This command is used only to create connections to Control M Server.Finds file and folder paths.

</td></tr><tr><td>

`xargs`

</td><td>

**grep &lt;string&gt;**

</td><td>

This command is used only to create connections to IBM CTRL-M Server.Runs the command on all lists from the output.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`tnsping`|Various options|Retrieves information about Oracle connections.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`find`|Various options|Finds the base init configuration file path.|
|`locate`|Various options|Finds the base init configuration file path if the 'find' command fails.|
|`nodetool version`|Various options|Retrieves the Apache Cassandra version.|
|`nodetool describecluster`|Various options|Retrieves the cluster name.|
|`nodetool info`|Various options|Retrieves the data center and rack information|
|`nodetool ring`|Various options|Retrieves the workload running for Apache Cassandra.|
|`nodetool tablestats`|Various options|Retrieves list of keyspaces available on a cluster.|
|`dse`|**–v**|Retrieves the DataStax Cassandra version.|
|`dsetool ring`|Various options|Retrieves the workload running for DataStax Cassandra.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`show`|**context, running**|Shows the requested information.|
|`include`|**-**|Extracts strings from the output.|
|`echo`|**-**|Displays strings to the output.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`show`|**gslb-config domain-list**|Shows the domain list.|
|`show`|**gslb-config dns rule**|Shows the DNS rule output.|
|`show`|**gslb-config answer-group**|Show the VIP answer.|

<table id="table_mgh_bkf_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`powershell`

</td><td>

**Add-PSSnapin Citrix.Broker.Admin.V2; Get-BrokerApplication -Name \[entry\_point.name\]** \| **select Name**,**CommandLineExecutable****,CommandLineArguments**,**WorkingDirectory**,**ApplicationType**,**BrowserName** \| **Format-List**

and

**Add-PSSnapin Citrix.Broker.Admin.V2; Get-BrokerApplication -Name \[entry\_point.name\] \| select Name,CommandLineExecutable,CommandLineArguments,WorkingDirectory,ApplicationType,BrowserName \| Format-List**

And

**Add-PSSnapin Citrix.Broker.Admin.V2; Get-BrokerMachine -DesktopGroupName ‘ \[delivery\_groups\[1\].name\]**

</td><td>

Gets applications managed by this Delivery Controller.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`qfarm`| |Discovers epic icons.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`get_xenapp_apps.ps1`|**\[entry\_point.icon\_path\]**|Runs powershell commands that retrieve the Citrix icon info from the Citrix repository.|
|`powershell`|Various options|Runs powershell commands.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`cscript`|**//NoLogo**|Runs VB scripts without a popup box.|
|`GetAppsInFolder.wsf`|**\[entry\_point.icon\_path\]**|Runs vbscript commands that retrieve the Citrix icon info from the Citrix repository.|

<table id="table_wth_1y2_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`show`

</td><td>

**cs policy, cs action,cs Policy, lb vserver**

</td><td>

This command is used only for discovering outgoing connections.

Shows the requested information.

</td></tr><tr><td>

`grep`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr></tbody>
</table><table id="table_nwm_g1d_pdb"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`show`

</td><td>

**ns.conf**

</td><td>

This command is used only for discovering outgoing connections if SNMP or SSH credentials are not provided.

Shows the contents of the ns.conf file.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`findstr`|Various options|\(For Windows only\) Extracts strings from the output.|
|`dir`|Various options|\(For Windows only\) Lists files and folders in the specified folder.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`findstr`|Various options|Extracts strings from the output.|
|`find`|Various options|Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|\(On Windows only\) Lists files and folders in the specified folder.|
|`findstr`|Various options|\(On Windows only\) Extracts strings from the output.|
|`find`|Various options|\(For Windows only\) Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`findstr`|Various options|\(On Windows only\) Extracts strings from the output.|
|`tasklist`|Various options|Lists all running tasks.|
|`netsh`|**http show servicestate**|Shows a snapshot of the HTTP service.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`systemctl list-units --type service`|Various options|Show the service status.|
|`/bin/systemctl status "+service_name+".service`|Various options|Show the service status.|
|`service --status-all`|Various options|Show the service status.|
|`read /etc/services`|Various options|Allows access to the file.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`ls`|Various options|\(On Unix only\) Lists files and folders in the specified folder.|
|`tail`|Various options|\(On Unix only\) Displays the end of the output.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`tnsping`|Various options|Retrieves information about Oracle connections.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`netstat`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`netstat`|Various options|Lists open ports.|

<table id="table_kv4_zx2_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`dmqdocbroker`

</td><td>

**-s -c getdocbasemap**

 and

 **-t \[computer\_system.primaryHostname\] -s -c getdocbasemap**

 and

 **-s -c getservermap \[docbas\]**

 **-t \[computer\_system.primaryHostname\] -s -c getdocbasemap**

 \[docbase\]

</td><td>

Gets the docbase information.

</td></tr><tr><td>

`del`

</td><td>

Various options

</td><td>

Deletes the XML file containing the old binding information.

</td></tr><tr><td>

`BTSTask`

</td><td>

**ExportBindings /Destination:%TEMP%\\MyBindings.xml /Database:\[MgmtDbName\] /server:\[serverName\]**

</td><td>

This command is used only if there are not MSSQL credentials.Extracts the binding info and places it into the XML file.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`findstr`|Various options|\(For Windows only\) Extracts strings from the output.|
|`dir`|Various options|\(For Windows only\) Lists files and folders in the specified folder.|

<table id="table_kfv_1kf_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`findstr`

</td><td>

Various options

</td><td>

\(For Windows only\) This command is used only to create CICS connections.Extracts strings from the output.

</td></tr><tr><td>

`dir`

</td><td>

Various options

</td><td>

\(For Windows only\) This command is used only to create CICS connections. Lists files and folders in the specified folder.

</td></tr><tr><td>

`type`

</td><td>

**-**

</td><td>

\(For Windows only\) This command is used only to create CICS connections. Displays the file content in the output.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`source`|**\[installed\_dir\]db2profile**|Sets the DB2 variables.|
|`db2`|list database directory|Displays the DB2 installation parameters.|
|`grep`|Various options|Extracts strings from the output.|
|`head`|**-1**|Displays only the first line from the output.|
|`db2level`|**-**|Displays the DB2 version.|
|`cat`|**-**|Displays the file content in the output.|
|`xargs`|**-I \{\} echo list tablespace containers for \{\} ';'**|This command is used only to create storage connections. Runs the command on all lists from the output.|

<table id="table_x5d_bkf_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`db2cmd`

</td><td>

**/c /w /i**

</td><td>

Lists the DB2 directories.

</td></tr><tr><td>

`db2`

</td><td>

list database directory

</td><td>

Displays the DB2 installation parameters.

</td></tr><tr><td>

`find`

</td><td>

Various options

</td><td>

Finds specific strings in files, folders, or standard output.

</td></tr><tr><td>

`dir`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`db2level`

</td><td>

**-**

</td><td>

Displays the DB2 version.

</td></tr><tr><td>

`echo`

</td><td>

Various options

</td><td>

This command is used only for storage connectivity. Prints the strings in the output.

</td></tr><tr><td>

`findstr`

</td><td>

Various options

</td><td>

This command is used only for storage connectivity.Extracts strings from the output.

</td></tr><tr><td>

`for`

</td><td>

Various options

</td><td>

This command is used only for storage connectivity. Runs loops.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`netstat`|Various options|Gets the DB2 name.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`netstat`|Various options|Lists open ports.|
|`find`|Various options|Finds specific strings in files and folders.|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`findstr`|Various options|Extracts strings from the output.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`versionInfo.sh`|**-**|Gets the Websphere Application Server version.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`"oeconsol 'D OMVS,A=ALL' | grep "+$taskname`|**-**|Gets the Websphere Application Server task.|
|`netstat`|**-a \| grep "+$port+" \| awk '\{print $1\}'**|Gets the task name from the listening port.|
|`ps -ef -o user,pid,ppid,comm | awk '{print $1,$2,$3,$4}’`| |Gets attributes for processes.|
|`$install_dir+"/bin/versionInfo.sh | grep Version | tail -1"`| |Gets the version from script.|
|`$install_dir+"/properties/version/BASE.product"`| |Gets the version from version file \(failover\).|
|`"ls "+$conf_dir+"/*/*/applications/*/deployments/*/META-INF/application.xml | xargs grep \"<context-root>/"+$uri_search+"\""+" 1>/tmp/app.txt 2>/dev/null; cat /tmp/app.txt"`| |Gets the list of URI files.|
|`$ear_directory_name+"/*/*/*/wsdl/*.wsdl"`| |Reads the wsdl files under the discovered inclusion on the Ear directory.|

<table id="table_nym_3wl_45"><thead><tr><th>

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

**-name**

 **-type**

</td><td>

This command is used only for creating the Web Services connections. Finds files and folders for the specific name.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`findstr`|Various options|Extracts strings from the output.|
|`netstat`|Various options|Lists the open ports.|
|`find`|Various options|Finds specific strings in files and folders.|

<table id="table_crk_ptr_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`find`

</td><td>

**-name**

 **-type**

</td><td>

This command is used only for creating the Web Services connections. Finds files and folders for the specific name.

</td></tr><tr><td>

`mqsiprofile`

</td><td>

**-**

</td><td>

Sets the variables for WebSphere Message Broker.

</td></tr><tr><td>

`mqsireportbroker`

</td><td>

**\[broker name\]**

</td><td>

Gets the WebSphere Message Broker information.

</td></tr><tr><td>

`mqsibrowse`

</td><td>

**\[broker name\] -t BROKERRESOURCES**

</td><td>

Displays the Message Broker information resources.

</td></tr><tr><td>

`echo`

</td><td>

**$ODBCINI**

</td><td>

\(On Unix only\) This command is used only to create connections to IBM DB2. Prints strings in the output.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`mqsiprofile`|**-**|Sets the variables for WebSphere Message Broker.|
|`mqsireportbroker`|**\[broker name\]**|Gets the WebSphere Message Broker information.|
|`ps`|**-ef**|Gets the process information.|
|`mqsibrowse`|**\[broker name\] -t BROKERRESOURCES**|Displays the Message Broker information resources.|
|`db2`| |Displays DB2 installation parameters: database directory and node directory.|

<table id="table_g41_rtr_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`mqsiprofile`

</td><td>

**-**

</td><td>

Sets the variables for WebSphere Message Broker.

</td></tr><tr><td>

`mqsireportbroker`

</td><td>

**\[broker name\]**

</td><td>

Gets the WebSphere Message Broker information.

</td></tr><tr><td>

`mqsibrowse`

</td><td>

**\[broker name\] -t BROKERRESOURCES**

</td><td>

Displays the Message Broker information resources.

</td></tr><tr><td>

`find`

</td><td>

**-name**

 **-type**

</td><td>

This command is used only for creating the Web Services connections. Finds files and folders for the specific name.

</td></tr><tr><td>

`echo`

</td><td>

**$ODBCINI**

</td><td>

This command is used only to create connections to IBM DB2. Prints strings in the output.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`mqsiprofile`|**-**|SSets the variables for WebSphere Message Broker.|
|`mqsireportbroker`|**\[broker name\]**|Gets the WebSphere Message Broker information.|
|`ps`|**-ef**|Gets the process information.|
|`mqsibrowse`|**\[broker name\] -t BROKERRESOURCES**|Displays the Message Broker information resources.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dspmq`|**-**|Gets the queue manager status.|
|`dspmqver`|**-**|Gets the queue manager version.|
|`runmqsc`|**\[queue manager\]**|Gets the queue information.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`grep`|Various options|Extracts strings from the output.|
|`dspmq`|**-**|Gets the queue manager status.|
|`dspmqver`|**-**|Gets the queue manager version.|
|`runmqsc`|**\[queue manager\]**|Gets the queue information.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`netstat`|**-a \| grep "+$port**|Gets the IBM MQ name.|
|`df`|**-k \| grep MQ"**|Gets the file system.|
|`"echo "+$netstat_info[1].mq_name+" | cut -c1-4"`|**-**|Gets the queue manager name.|
|`"oeconsol '-"+$queue_manager+" display qmgr ALL' "`|**-**|Gets the MQ logical name information.|
|`"oeconsol '-"+$queue_manager+" display queue ("+$entry_point.queue_name+") ALL' | tr \"(\" \"#\" | tr \")\" \"\""`|**-**|Gets the MQ queue information together with the information on its connections.|
|`"oeconsol '-"+$queue_manager+" display queue ("+$name+")'"`|**-**|Gets the MQ queue information.|
|`"oeconsol '-"+$queue_manager+" display channel(*) CONNAME where(QMNAME EQ "+$remote_queue_mngr_name+")'"`|**-**|Gets the channel information.|
|`"oeconsol '-"+$queue_manager+" display qlocal(*) '"`| |Gets the local queue information.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dspmq`|**-**|Gets the queue manager status.|
|`dspmqver`|**-**|Gets the queue manager version.|
|`runmqsc`|**\[queue manager\]**|Gets the queue information.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dspmq`|**-**|Gets the queue manager status.|
|`dspmqver`|**-**|Gets the queue manager version.|
|`runmqsc`|**\[queue manager\]**|Gets the queue information.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|\(On Windows only\) Lists files and folders in the specified folder.|
|`findstr`|Various options|\(On Windows only\) Extracts strings from the output.|
|`find`|Various options|\(On Windows only\) Finds specific strings in files and folders.|
|`netstat`|Various options|\(On Windows only\) Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`find`|**-name**|Finds files and folders in the specified folder.|
|`xargs`|**grep &lt;string&gt;**|Finds strings in all files found in the output file.|
|`dir`|Various options|\(On Windows only\) Lists files and folders in the specified folder.|
|`findstr`|Various options|\(On Windows only\) Extracts strings from the output.|
|`find`|Various options|\(For Windows only\) Finds specific strings in files and folders.|
|`netstat`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`find`|**-name**|Finds files and folders in the specified folder.|
|`xargs`|**grep &lt;string&gt;**|Finds strings in the files found in the output file.|
|`grep`|Various options|Extracts strings from the output.|
|`dir`|Various options|\(On Windows only\) Lists files and folders in the specified folder.|
|`findstr`|Various options|\(On Windows only\) Extracts strings from the output.|
|`find`|Various options|\(For Windows only\) Finds specific strings in files and folders.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Various options|Lists open ports.|

<table id="table_ogv_zx2_45"><thead><tr><th>

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

`hostname`

</td><td>

**-**

</td><td>

Gets the hostname.

</td></tr><tr><td>

`dir`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`tasklist`

</td><td>

Various options

</td><td>

Lists all running tasks.

</td></tr><tr><td>

`del`

</td><td>

Various options

</td><td>

Deletes the XML file containing the old binding information.

</td></tr><tr><td>

`echo`

</td><td>

Various options

</td><td>

Prints strings in the output.

</td></tr><tr><td>

`powershell`

</td><td>

**Add-PSSnapin Microsoft.Exchange.Management.PowerShell.E2010; Get-ExchangeServer -status -Identity \[hostname\]\| export-clixml $env:TEMP\\exchange\_pwrshell\_output.xml**

 and

 **Add-PSSnapin Microsoft.Exchange.Management.PowerShell.Admin; Get-ExchangeServer -status -Identity \[hostname\]\| export-clixml $env:TEMP\\exchange\_pwrshell\_output.xml**

 and

 **Add-PSSnapin Microsoft.Exchange.Management.PowerShell.E2010; Get-ExchangeServer\| format-table -autosize -HideTableHeaders Name,Fqdn,IsMailboxServer**

 and

 **Add-PSSnapin Microsoft.Exchange.Management.PowerShell.Admin; Get-ExchangeServer \| format-table -autosize -HideTableHeaders Name,Fqdn,IsMailboxServer**

 and

 **Add-PSSnapin Microsoft.Exchange.Management.PowerShell.Admin; Get-MailboxServer \| format-list**

</td><td>

This command is used only if you do not use TCP connections.Gets the CAS status, server roles, and Exchange setup structure.

 **Important:** Do not use the dollar sign \($\) in credentials for Exchange CAS, because Service Mapping uses the dollar sign for pattern variables in the Powershell command.

</td></tr><tr><td>

`find`

</td><td>

Various options

</td><td>

This command is used only if PowerShell is not operational.Finds specific strings in the files and folders.

</td></tr><tr><td>

`findstr`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`netstat`|Various options|Lists open ports.|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`findstr`|Various options|Extracts strings from the output.|
|`find`|Various options|Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`echo`|Various options|Prints strings in the output.|

<table id="table_bll_zx2_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`echo`

</td><td>

Various options

</td><td>

Prints strings in the output.

</td></tr><tr><td>

`del`

</td><td>

Various options

</td><td>

Deletes the XML file containing the old binding information.

</td></tr><tr><td>

`BTSTask`

</td><td>

**ExportBindings /Destination:%TEMP%\\MyBindings.xml /Database:\[MgmtDbName\] /server:\[serverName\]**

</td><td>

This command is used only if there are not MSSQL credentials.Extracts the binding information and places it into the XML file.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`netstat`|Various options|Lists open ports.|
|`hostname`|**-**|Gets the hostname.|
|`tasklist`|Various options|Lists all running tasks.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`netstat`|Various options|Lists open ports.|
|`hostname`|**-**|Gets the hostname.|
|`tasklist`|Various options|Lists all running tasks.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`findstr`|Various options|Extracts strings from the output.|

<table id="table_ulr_xmk_45"><thead><tr><th>

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

`hostname`

</td><td>

**-**

</td><td>

Gets the hostname.

</td></tr><tr><td>

`dir`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`tasklist`

</td><td>

Various options

</td><td>

Lists all running tasks.

</td></tr><tr><td>

`echo`

</td><td>

Various options

</td><td>

Prints strings in the output.

</td></tr><tr><td>

`del`

</td><td>

Various options

</td><td>

Deletes the XML file containing the old binding information.

</td></tr><tr><td>

`powershell`

</td><td>

**Add-PSSnapin Microsoft.Exchange.Management.PowerShell.E2010; Get-ExchangeServer -status -Identity \[entry\_point.host\_name\]\| export-clixml $env:TEMP\\exchange\_pwrshell\_output.xml**

and

**"Add-PSSnapin Microsoft.Exchange.Management.PowerShell.Admin; Get-ExchangeServer -status -Identity \[entry\_point.host\_name\] \| export-clixml $env:TEMP\\exchange\_pwrshell\_output.xml**

</td><td>

This command is used only if you do not use TCP connections.Gives the CAS status, server roles, and Exchange setup structure.

 **Important:** Do not use the dollar sign \($\) in credentials for Exchange Hub Transport Server, because Service Mapping uses the dollar sign for pattern variables in the powershell command.

</td></tr><tr><td>

`findstr`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr><tr><td>

`find`

</td><td>

Various options

</td><td>

Finds specific strings in files and folders.

</td></tr></tbody>
</table><table id="table_wgz_xmk_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`appcmd.exe`

</td><td>

Various options

</td><td>

This command is used only for IIS version 7 and later.Retrieves information about the specified application name.

</td></tr></tbody>
</table><table id="table_erf_ymk_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`appcmd.exe`

</td><td>

Various options

</td><td>

This command is used only for IIS version 7 and later.Retrieves information about the specified application name.

</td></tr><tr><td>

`iisapp.vbs`

</td><td>

Various options

</td><td>

This command is used only for IIS version 6.Retrieves information about the specified application name.

</td></tr><tr><td>

`dir`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`findstr`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr><tr><td>

`find`

</td><td>

Various options

</td><td>

Finds specific strings in files and folders.

</td></tr><tr><td>

`netstat`

</td><td>

Various options

</td><td>

Lists open ports.

</td></tr></tbody>
</table><table id="table_hsd_51y_n5"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`ildasm.exe`

</td><td>

text that contains process exe path

</td><td>

This file is necessary for performing the put file operation on the ILDisassembler alias. This file disassembles strings from the command .exe file.

</td></tr><tr><td>

`.findstr`

</td><td>

Various options

</td><td>

Gets the strings from the output.

</td></tr><tr><td>

`dir`

</td><td>

Various options

</td><td>

Lists all files in the specified folder.

</td></tr><tr><td>

`connection_strings_browser.exe`

</td><td>

**\[encrypted\_configs\[\*\].Name\]**

</td><td>

This command is used only for creating database encrypted connections. This file is necessary for performing the put file operation on theConnectionStringsBrowser alias.

Decrypts the database connections.

</td></tr></tbody>
</table><table id="table_fpb_bnk_45"><thead><tr><th>

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

`hostname`

</td><td>

**-**

</td><td>

Gets the hostname.

</td></tr><tr><td>

`dir`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`tasklist`

</td><td>

Various options

</td><td>

Lists all running tasks.

</td></tr><tr><td>

`del`

</td><td>

Various options

</td><td>

Deletes the XML file containing old binding information.

</td></tr><tr><td>

`echo`

</td><td>

Various options

</td><td>

Prints strings in the output.

</td></tr><tr><td>

`powershell`

</td><td>

**Add-PSSnapin Microsoft.Exchange.Management.PowerShell.Admin; Get-ExchangeServer -status -Identity \[entry\_point.host\_name\]\| export-clixml $env:TEMP\\exchange\_pwrshell\_output.xml**

 and

 **Add-PSSnapin Microsoft.Exchange.Management.PowerShell.Admin; Get-ExchangeServer -status \| export-clixml $env:TEMP\\exchange\_pwrshell\_output.xml**

 and

**Add-PSSnapin Microsoft.Exchange.Management.PowerShell.E2010; Get-ExchangeServer -status -Identity \[entry\_point.host\_name\]\| export-clixml $env:TEMP\\exchange\_pwrshell\_output.xml**

 and

 **Add-PSSnapin Microsoft.Exchange.Management.PowerShell.Admin; Get-ClusteredMailBoxServerStatus \| format-table -Property OperationalMachines**

 and

 **Add-PSSnapin Microsoft.Exchange.Management.PowerShell.Admin; Get-ExchangeServer \| format-table -autosize -HideTableHeaders Name,Fqdn,IsHubTransportServer**

 and

**Add-PSSnapin Microsoft.Exchange.Management.PowerShell.E2010; Get-ExchangeServer \| format-table -autosize -HideTableHeaders Name,Fqdn,IsHubTransportServer**

 and

 **Add-PSSnapin Microsoft.Exchange.Management.PowerShell.Admin; Get-StorageGroup -server \[hostname\] \| select SystemFolderPath \| Export-Csv out.csv -notype;cat out.csv**

 and

 **Add-PSSnapin Microsoft.Exchange.Management.PowerShell.Admin; Get-StorageGroup \| select SystemFolderPath \| Export-Csv out.csv -notype;cat out.csv**

 and

 **Add-PSSnapin Microsoft.Exchange.Management.PowerShell.E2010; Get-MailboxDatabase \| select LogFolderPath \| format-table -autosize -hideTableHeaders; Get-MailboxDatabase \| select EdbFilePath\| format-table -autosize -hideTableHeaders;Get-MailboxDatabase \| select TemporaryDataFolderPath\| format-table -autosize -hideTableHeaders**

</td><td>

This command is used only if you do not use TCP connections.Gets the status, server roles, and the setup structure of Exchange Mailbox.

 **Important:** Do not use the dollar sign \($\) in credentials for Exchange Mailbox, because Service Mapping uses the dollar sign for pattern variables in the Powershell command.

</td></tr><tr><td>

`find`

</td><td>

Various options

</td><td>

This command is used only if PowerShell is not operational.Finds specific strings in the files and folders.

</td></tr><tr><td>

`findstr`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`hostname`|**-**|Gets the hostname.|

<table id="table_zxg_cnk_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`findstr`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr><tr><td>

`hostname`

</td><td>

**-**

</td><td>

Gets the hostname.

</td></tr><tr><td>

`findstr`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr><tr><td>

`sqlcmd`

</td><td>

**-Stcp:\[computer\_system.primaryManagementIP\],\[port\] -d \[entry\_point.database\] -U \[username\] -P '\[password\]' -y 0 -h-1 -Q select nvcname\#\#\#inboundtransporturl FROM adm\_ReceiveLocation rl, bts\_receiveport rp where rl.receiveportid=rp.nid**

 and

 **-Stcp:\[computer\_system.primaryManagementIP\],\[port\] -d \[entry\_point.database\] -U \[username\] -P '\[password\]' -y 0 -h-1 -Qselect nID,nvcName,nApplicationID from bts\_receiveport**

 and

 **-Stcp:\[computer\_system.primaryManagementIP\],\[port\] -d \[entry\_point.database\] -U \[username\] -P '\[password\]' -y 0 -h-1 -Qselect nID,nvcName,nApplicationID from bts\_sendport**

 and

 **-Stcp:\[computer\_system.primaryManagementIP\],\[port\] -d \[entry\_point.database\] -U \[username\] -P '\[password\]' -y 0 -h-1 -Qselect nOrcPortID,nReceivePortID,nSendPortid from bts\_orchestration\_port\_binding**

 and

 **-Stcp:\[computer\_system.primaryManagementIP\],\[port\] -d \[entry\_point.database\] -U \[username\] -P '\[password\]' -y 0 -h-1 -Qselect nID,nOrchestrationID from bts\_orchestration\_port**

 and

 **-Stcp:\[computer\_system.primaryManagementIP\],\[port\] -d \[entry\_point.database\] -U \[username\] -P '\[password\]' -y 0 -h-1 -Qselect nID,nvcFullName from bts\_orchestration**

 and

 **-Stcp:\[computer\_system.primaryManagementIP\],\[port\] -d \[entry\_point.database\] -U \[username\] -P '\[password\]' -y 0 -h-1 -Qselect ah.Name\#\#\#bo.nvcNamespace.bo.nvcName\#\#\#ase.Name from bts\_orchestration bo, adm\_Host ah,adm\_server ase,adm\_Server2HostMapping ash where bo.nAdminHostID = ah.ID and ase.ID = ash.ServerID and ah.ID = ash.HostID**

 and

 **-Stcp:\[computer\_system.primaryManagementIP\],\[port\] -d \[entry\_point.database\] -U \[username\] -P '\[password\]' -y 0 -h-1 -Qselect nID,nSendPortID,nvcAddress from bts\_sendport\_transport**

</td><td>

This command is used only to discover Microsoft BizTalk.Gets the BizTalk information from the database.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`findstr`|Various options|Extracts strings from the output.|
|`netstat`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`findstr`|Various options|Extracts strings from the output.|
|`netstat`|Various options|Lists open ports.|
|`sqlservr.exe`| |Gets the version of the database from the executable file.|

<table id="table_jm1_skp_12b"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`mongo`

</td><td>

--eval db.printShardingStatus\(\)

</td><td>

Retrieves the status of MondoDB that is used for load balancing.

</td></tr><tr><td>

`mongo`

</td><td>

--db.Name\(\)

</td><td>

Retrieves the name of the database connected to MongoDB server.

</td></tr></tbody>
</table><table id="table_xrd_2nk_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`findstr`

</td><td>

Various options

</td><td>

\(On Windows only\) Extracts strings from the output.

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

`ps`

</td><td>

**--pid=\[process.pid\] --no-headers -o " %U : %p : %a”**

</td><td>

Gets the userid parameter value.

</td></tr><tr><td>

`mysqld-nt/mysqld/mysqld.exe`

</td><td>

**-V**

</td><td>

Gets the version.

</td></tr><tr><td>

`mysql`

</td><td>

**--user=\[username\] --password=\[password\] --port=\[jdbc\_port\] --skip-column-names --silent --execute="SHOW ENGINE NDB STATUS;;”**

and

**--user=\[username\] --password=\[password\] --port=\[jdbc\_port\] --skip-column-names --silent --execute="SHOW SLAVE STATUS;;”**

and

**--user=\[username\] --password=\[password\] --port=\[jdbc\_port\] --skip-column-names --silent --execute="select host from information\_schema.processlist where command like '%%binlog%%';;”**

</td><td>

This command is used only to create cluster node connections, primary replications, and the secondary.Gets the deployment structure of the MySQL server.

</td></tr><tr><td>

`which`

</td><td>

**mysql**

</td><td>

This command is used only to create cluster node connections, primary replications, and the secondary.Gets the full path of MySQL cluster nodes.

</td></tr></tbody>
</table><table id="table_yrd_2nk_45"><thead><tr><th>

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

`ndb_mgmd`

</td><td>

**-V**

and

**-e show**

</td><td>

Gets the version and status of the MySQL Cluster MGM node.

</td></tr></tbody>
</table><table id="table_thl_2nk_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`nginx`

</td><td>

**-v**

</td><td>

Gets the version.

</td></tr><tr><td>

`egrep`

</td><td>

**-v -e ^\# -e "\\t\#"**

</td><td>

This command is used if necessary to create HTTP connections.Ignores special characters.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|\(On Windows only\) Lists files and folders in the specified folder.|
|`findstr`|Various options|\(On Windows only\) Extracts strings from the output.|
|`find`|Various options|\(For Windows only\) Finds specific strings in files and folders.|
|`export`|**-**|\(For Unix only\) Sets variables.|
|`echo`|Various options|Prints strings in the output.|
|`sqlplus`|Various options|Creates the connection to the Oracle instance.|
|`awk`|Various options|\(For Unix only\) Manipulates the output.|
|`netstat`|Various options|\(For Windows only\) Gets open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`export`|**-**|\(On Unix only\) Sets a variable.|
|`echo`|Various options|Prints strings in the output.|
|`sqlplus`|Various options|Creates connection to the Oracle instance.|
|`set`|**-**|\(On Windows only\) Sets a variable.|
|`netstat`|Various options|\(On Windows only\) Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`findstr`|Various options|\(For Windows only\) Extracts strings from the output.|
|`dir`|Various options|\(For Windows only\) Lists files and folders in the specified folder.|
|`netstat`|Various options|\(For Windows only\) Lists open ports.|
|`awk`|Various options|\(For Unix only\) Manipulates the output.|
|`find`|Various options|\(For Windows only\) Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`findstr`|Various options|Extracts strings from the output.|
|`find`|Various options|Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`findstr`|Various options|Extracts strings from the output.|
|`find`|Various options|Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`findstr`|Various options|Extracts strings from the output.|
|`find`|Various options|Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`findstr`|Various options|Extracts strings from the output.|
|`find`|Various options|Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`findstr`|Various options|Extracts strings from the output.|
|`find`|Various options|Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`findstr`|Various options|Extracts strings from the output.|
|`find`|Various options|Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`findstr`|Various options|Extracts strings from the output.|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`find`|Various options|Finds specified strings in the file and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`findstr`|Various options|Extracts strings from the output.|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`find`|Various options|Finds specified strings in the file and folders.|

<table id="table_cf5_2nk_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`export`

</td><td>

**-**

</td><td>

Sets the variable.

</td></tr><tr><td>

`sqlplus`

</td><td>

**-s \[username\]/\[password\]@\[entry\_point.instance\]**

</td><td>

This command is used only for getting the advanced queue information.Gets the Oracle version and information about advance queue.

</td></tr><tr><td>

`echo`

</td><td>

**-e set head off feed off pages 0 line 3000\\\\n\\"select NAME \|\| '\#\#' \|\| QUEUE\_TABLE \|\| '\#\#' \|\| QID \|\| '\#\#' \|\| QUEUE\_TYPE \|\| '\#\#' \|\| RETENTION from DBA\_QUEUES where OWNER = UPPER\(\[entry\_point.scheme\]\);**

 and

 **set head off feed off pages 0 line 3000\\\\n\\"select NAME \|\| '\#\#' \|\| QUEUE\_TABLE \|\| '\#\#' \|\| QID \|\| '\#\#' \|\| QUEUE\_TYPE \|\| '\#\#' \|\| RETENTION from DBA\_QUEUES where OWNER = UPPER\(\[entry\_point.scheme\]\);**

 and

 **select member as NEEBULA from v\\$logfile;**

 and

 **select value as NEEBULA from v\\$parameter where name='log\_archive\_dest'**

 and

 **select file\_name as NEEBULA from dba\_data\_files;**

 and

 **select DB\_LINK,HOST from DBA\_DB\_LINKS**

</td><td>

This command is used only for getting the advance queue information. Gets the information about advance queue, storage devices, and database links.

</td></tr><tr><td>

`lsnrctl`

</td><td>

**version**

And

**services**

</td><td>

This command is used only for discovering the real application cluster \(RAC\) version. Gets the RAC version.

</td></tr></tbody>
</table><table id="table_v3c_fnk_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`set`

</td><td>

**-**

</td><td>

Sets the variable.

</td></tr><tr><td>

`sqlplus`

</td><td>

**-s \[username\]/\[password\]@\[entry\_point.instance\]**

</td><td>

This command is used only for getting the advance queue information.Gets the Oracle version and information about advance queue.

</td></tr><tr><td>

`echo`

</td><td>

**-e set head off feed off pages 0 line 3000\\\\n\\"select NAME \|\| '\#\#' \|\| QUEUE\_TABLE \|\| '\#\#' \|\| QID \|\| '\#\#' \|\| QUEUE\_TYPE \|\| '\#\#' \|\| RETENTION from DBA\_QUEUES where OWNER = UPPER\(\[entry\_point.scheme\]\);**

 and

 **set head off feed off pages 0 line 3000\\\\n\\"select NAME \|\| '\#\#' \|\| QUEUE\_TABLE \|\| '\#\#' \|\| QID \|\| '\#\#' \|\| QUEUE\_TYPE \|\| '\#\#' \|\| RETENTION from DBA\_QUEUES where OWNER = UPPER\(\[entry\_point.scheme\]\);**

 and

 **select member as NEEBULA from v\\$logfile;**

 and

 **select value as NEEBULA from v\\$parameter where name='log\_archive\_dest'**

 and

 **select file\_name as NEEBULA from dba\_data\_files;**

 and

 **select DB\_LINK,HOST from DBA\_DB\_LINKS**

</td><td>

This command is used only for getting the advance queue information. Gets the information about advance queue, storage devices, and database links.

</td></tr><tr><td>

`lsnrctl`

</td><td>

**version**

 And

 **services**

</td><td>

This command is used only for discovering the real application cluster \(RAC\) version. Gets the RAC version.

</td></tr><tr><td>

`netstat`

</td><td>

Various options

</td><td>

Lists open ports.

</td></tr></tbody>
</table><table id="table_w3c_fnk_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`findstr`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr><tr><td>

`dir`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`find`

</td><td>

Various options

</td><td>

This command is used only to create the Web Services connections. Finds specified strings in the file and folders.

</td></tr><tr><td>

`netstat`

</td><td>

Various options

</td><td>

Lists open ports.

</td></tr></tbody>
</table><table id="table_bgq_fnk_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`lsnrctl`

</td><td>

**version**

 and

 **status**

</td><td>

Gets the version and status of the Oracle Net Listener.

</td></tr><tr><td>

`export`

</td><td>

**-**

</td><td>

Sets the variable.

</td></tr><tr><td>

`crsctl`

</td><td>

**status res -t**

 and

 **config service -d**

</td><td>

Gets the services status and configuration.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`psadmin`|Various options|Retrieves information from the PeopleSoft repository or server.|
|`tnsping`|Various options|Retrieves information about the database instance given to the tnsping command.|
|`sqlplus`|Various options|Connects to the database instance and runs the sql query.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`findstr`|Various options|Extracts strings from the output.|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`find`|Various options|Finds specified strings in the file and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`findstr`|Various options|Extracts strings from the output.|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`find`|Various options|Finds specified strings in the file and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`findstr`|Various options|Extracts strings from the output.|
|`find`|Various options|Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`findstr`|Various options|Extracts strings from the output.|
|`find`|Various options|Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|Lists files and folders in the specified folder.|
|`findstr`|Various options|Extracts strings from the output.|
|`find`|Various options|Finds specific strings in files and folders.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|\(On Windows only\) Lists files and folders in the specified folder.|
|`findstr`|Various options|\(On Windows only\) Extracts strings from the output.|
|`find`|Various options|\(For Windows only\) Finds specific strings in files and folders.|
|`versionInfo.sh`|**-**|Gets the Websphere Application Server version.|

<table id="table_mnv_5jp_55"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`findstr`

</td><td>

Various

</td><td>

\(For Windows only\) Extracts strings from the output

</td></tr><tr><td>

`dir`

</td><td>

Various

</td><td>

\(For Windows only\) Lists all existing files in the given folder.

</td></tr><tr><td>

`find`

</td><td>

Various

</td><td>

\(For Windows only\) Finds specific strings in files and folders.

</td></tr><tr><td>

`find`

</td><td>

**-name**

</td><td>

This command is used only to create web service connections.

Finds files and folders for specific name.

</td></tr><tr><td>

`tmadmin`

</td><td>

**-v**

</td><td>

Gets the Tuxedo version.

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

</td></tr></tbody>
</table><table id="table_mr5_jnp_55"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`findstr`

</td><td>

Various

</td><td>

\(For Windows only\) Extracts strings from the output

</td></tr><tr><td>

`dir`

</td><td>

Various

</td><td>

\(For Windows only\) Lists all existing files in the given folder.

</td></tr><tr><td>

`find`

</td><td>

Various

</td><td>

\(For Windows only\) Finds specific strings in files and folders.

</td></tr><tr><td>

`find`

</td><td>

**-name**

</td><td>

This command is used only to create web service connections.

Finds files and folders for specific name.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`postgres`|**-v**|Gets the version.|
|`findstr`|Various options|\(For Windows only\) Extracts strings from the output.|
|`dir`|Various options|\(For Windows only\) Lists files and folders in the specified folder.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`ps`|**-ef**|Displays the currently running process.|
|`grep`|Various options|Searches plain-text data sets for lines that match the regular expression.|
|`grep`|**-v &lt;string&gt;**|Searches plain-text data sets for lines that do not match the regular expression.|
|`ps`|**-ef \| grep corosync \| grep -v grep'**|Checks if the corosync process is running on the server. If the process is running, the Red Hat Cluster is running on this server.|
|`ifconfig`|**-**|Displays the current network configuration information.|
|`ip a`|**-**|Displays the current network configuration information.|
|`awk`|Various options|Manipulates the output.|
|`hostname`|**-s**|Displays the Fully Qualified Domain Name \(FQDN\).|
|`hostname`|**-f**|Displays the short host name.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`findstr`|Various options|\(For Windows only\) Extracts strings from the output.|
|`type`|**-**| |
|`tnsping`|**instance**|This command is used to create connections to Oracle.|

<table id="table_nzj_1wl_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`findstr`

</td><td>

Various options

</td><td>

\(For Windows only\) Extracts strings from the output.

</td></tr><tr><td>

`dir`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`tnsping`

</td><td>

**instance**

</td><td>

This command is used to create connections to Oracle. Gets the version.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|\(For Windows only\) Lists files and folders in the specified folder.|
|`disp + work`|**-V**|Gets the version.|
|`ping`|**-n 1**|\(For Windows only\) Verifies that the host is answering.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Lists open ports.|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|\(For Windows only\) Lists files and folders in the specified folder.|
|`disp + work`|**-V**|Gets the version.|
|`ping`|**-c 1**|\(For Unix only\) Verifies that the host is answering.|
|`ping`|**-n 1**|\(For Windows only\) Verifies that the host is answering.|
|`netstat`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|\(For Windows only\) Lists files and folders in the specified folder.|
|`disp + work`|**-V**|Gets the version.|
|`ping`|**-n 1**|\(For Windows only\) Verifies that the host is answering.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Lists open ports.|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`hdbsql`|**-v**|Gets the version.|

<table id="table_jtx_csn_tzb"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`hdbsql`

</td><td>

Various options

</td><td>

-   Gets schemas info
-   Gets time zone
-   Gets disk size

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|\(For Windows only\) Lists files and folders in the specified folder.|
|`jlaunch`|**-V**|Gets the version.|
|`ping`|**-n 1**|\(For Windows only\) Verifies that the host is answering.|
|`netstat`|Various options|Lists the open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dir`|Various options|\(For Windows only\) Lists files and folders in the specified folder.|
|`msg_server`|**-V**|Gets the version.|
|`ping`|**-n 1**|\(For Windows only\) Verifies that the host is answering.|
|`netstat`|Various options|Lists the open ports.|
|`ss`|Lists open ports.|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`MsMdSrv.exe`|**-n**|Gets the instance name.|
|`netstat`|Various options|Lists the open ports.|

<table id="table_zb3_dwl_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`MsMdSrv.exe`

</td><td>

**-n**

</td><td>

Gets the instance name.

</td></tr><tr><td>

`dir`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`findstr`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr><tr><td>

`find`

</td><td>

Various options

</td><td>

Finds specified strings in the file and folders.

</td></tr><tr><td>

`sqlcmd`

</td><td>

**-Stcp:\[computer\_system.primaryManagementIP\],\[port\] -y 0 -h-1 -E -Qselect convert\(varchar\(max\), convert\(varbinary\(max\),packagedata\)\)from msdb.dbo.sysssispackages where name = '\[name\]' -o \[tmp\_dir\]/\[name\].xml**

 and

 **-Stcp:\[computer\_system.primaryManagementIP\],\[port\] -y 0 -h-1 -E -Qselect convert\(varchar\(max\), job\_id\)\#\#\#\[command\]@@@ from msdb.dbo.sysjobsteps**

 and

 **-Stcp:\[computer\_system.primaryManagementIP\],\[port\] -y 0 -h-1 -E -Qselect \[name\]\#\#\#convert\(varchar\(max\), job\_id\) from msdb.dbo.sysjobs**

</td><td>

This command is used only for discovering jobs.

</td></tr></tbody>
</table><table id="table_ac3_dwl_45"><thead><tr><th>

Command

</th><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`dir`

</td><td>

Various options

</td><td>

Lists files and folders in the specified folder.

</td></tr><tr><td>

`findstr`

</td><td>

Various options

</td><td>

Extracts strings from the output.

</td></tr><tr><td>

`find`

</td><td>

Various options

</td><td>

Finds specified strings in the file and folders.

</td></tr><tr><td>

`sqlcmd`

</td><td>

**-Stcp:\[computer\_system.primaryManagementIP\],\[port\] -h-1 -E -QSELECT \[name\]\#\#\#DB FROM msdb.dbo.sysssispackages**

 and

 **-Stcp:\[computer\_system.managementIP\],\[port\] -h-1 -E -QSELECT \[name\]\#\#\#DB FROM msdb.dbo.sysssispackages**

 and

 **-Stcp:\[computer\_system.primaryManagementIP\],\[port\] -h-1 -E -QSELECT \[name\]\#\#\#JOB FROM msdb.dbo.sysjobs**

 and

 **-Stcp:\[computer\_system.managementIP\],\[port\] -h-1 -E -Q SELECT \[name\]\#\#\#JOB FROM msdb.dbo.sysjobs**

</td><td>

This command is used only if you need to discover jobs.

</td></tr></tbody>
</table>|Command|Parameter|Description|
|-------|---------|-----------|
|`slapd-dirserv`|**-D \[instance\] -v**|Gets the version.|
|`netstat`|Various options|Lists the open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`configutil`|**-**|Gets the JES configuration.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`dataserverv`|**-v**|Gets the version.|
|`dir`|Various options|\(For Windows only\) Lists files and folders in the specified folder.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`findstr`|Various options|Extracts strings from the output.|
|`netstat`|Various options|Lists open ports.|
|`ping`|**-n 1\[ip\]**|Verifies that the SQL server is running.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`hostname`|**-**|Gets the hostname.|
|`"IFS=$'\n';for i in `find " + $tra_home + " -type f | grep -v /tmp | egrep \".process$|.substvar$\"`; do result=`grep \"" + $entry_point.queue + "\" $i`; echo $i###$result@@@; done| grep -v \"###@@@\""`|**-**|Scans the label file and brings the actual values.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`TibcoFilesParser.ksh`|**-**|\(For Unix only\) This file is necessary for performing the put file operation. It replaces all tags in Tibco configuration files and puts them under the /tmp folder.|
|`hostname`|**-**|Gets the hostname.|
|`cd`|**-**|\(On Unix only\) Changes directory.|
|`chmod`|**-**|\(On Unix only\) Changes file permissions.|
|`for`|Various options|\(On Unix only\) Runs loops.|
|`echo`|Various options|\(On Unix only\) Prints strings in the output.|
|`if`|Various options|\(On Unix only\) Starts a condition.|
|`wc`|**-l**|\(On Unix only\) Counts the output lines.|
|`dir`|Various options|\(On Windows only\) Lists files and folders in the specified folder.|
|`findstr`|Various options|\(On Windows only\) Extracts strings from the output.|
|`netstat`|Various options|Lists open ports.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`hostname`|**-**|Gets the hostname.|
|`cd`|**-**|\(On Unix only\) Changes directory.|
|`chmod`|**-**|\(On Unix only\) Changes file permissions.|
|`for`|Various options|\(On Unix only\) Runs loops.|
|`echo`|Various options|\(On Unix only\) Prints strings in the output.|
|`if`|Various options|\(On Unix only\) Starts a condition.|
|`wc`|**-l**|\(On Unix only\) Counts the output lines.|
|`dir`|Various options|\(On Windows only\) Lists files and folders in the specified folder.|
|`findstr`|Various options|\(On Windows only\) Extracts strings from the output.|
|`netstat`|Various options|Lists open ports.|
|`ss`|Lists open ports.|Lists open ports.|
|`cut`|Various options|\(On Unix only\) Splits the output line.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`rm`|**-f /tmp/ems.cmd**|Prepares the EMS script.|
|`tibemsadmin`|**-server tcp://+\[computer\_system.primaryManagementIP\]:\[port\] -user \[username\] -password \[password\] -script \[script\]**|Connects to the EMS administrator and gets the list of EMS Queue consumers.|
|`echo`|Various options|Prints strings in the output.|

|Command|Parameter|Description|
|-------|---------|-----------|
|`rm`|**-f /tmp/ems.cmd**|Prepares the EMS script.|
|`tibemsadmin`|**-server tcp://+\[computer\_system.primaryManagementIP\]:\[port\] -user \[username\] -password \[password\] -script \[script\]**|Connects to the EMS administrator and gets the list of EMS Queue consumers.|
|`echo`|Various options|\(On Windows only\) Prints strings in the output.|

**Parent Topic:**[Prerequisites for performing top-down discovery using Service Mapping](prerequisites-service-mapping.md)

**Related topics**  


[Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md)


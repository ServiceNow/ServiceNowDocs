---
title: MID Server properties used by Service Mapping
description: Service Mapping uses the MID Server parameters during discovery and mapping. Do not change default values for these parameters unless you are troubleshooting the discovery process.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 13
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# MID Server properties used by Service Mapping

Service Mapping uses the MID Server parameters during discovery and mapping. Do not change default values for these parameters unless you are troubleshooting the discovery process.

## General properties

<table id="table_ejf_pd4_w4b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mid.file\_tracking.file\_path\_forbidden\_strings

</td><td>

Comma-separated list of strings to search for in tracked file paths. Once any string in this list is found in a tracked file path, the file is removed from further processing. -   **Default value**: job finished with status ERROR
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>## SSH-related properties

<table id="table_vgb_tcx_s4b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mid.sa.ssh.path

</td><td>

A location at the target system where the MID Server checks for commands to execute.

-   **Default value**: /usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.truncate\_last\_line\_regex

</td><td>

A regular expression of line that the MID Server removes from the end of the SSH command response.

-   **Default value**: Command.\*performed by.\*
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.remove\_first\_line\_regex

</td><td>

A regular expression of line that the MID Server removes from the start of every SSH command response.

-   **Default value**: \[empty string\]
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.privileged\_command\_message

</td><td>

A prompt the MID Server sends with commands with sudo-level privileges. For example, a sudo-level command is sent with “Password:”.

-   **Default value**: \[empty string\]
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.restricted\_shell\_regex

</td><td>

A regular expression text included on opening message of a restricted shell. Using a restricted shell, the SSH provider does not run some commands during the session initialization.-   **Default value**: restricted shell
-   **Type**:
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.terminal\_cols

</td><td>

The number of columns in the terminal windows opened with the SSH session.-   **Default value**: 300
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.terminal\_rows

</td><td>

The number of rows in the terminal windows opened with the SSH session. -   **Default value**: 800
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.time\_between\_change\_shell\_and\_prompt

</td><td>

The time to wait between changing a shell during initialization and the time the shell prompt appears \(in milliseconds\).-   **Default value**: 1000
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.connect\_timeout

</td><td>

The SSH initial connection timeout \(in milliseconds\).-   **Default value**: 2000
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.max\_chars\_single\_response

</td><td>

The maximum number of characters allowed in a single SSH command response.-   **Default value**: 10000000
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.break\_session\_chars

</td><td>

The ASCII value of character used to break a session.-   **Default value**: 7
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.no\_change\_shell\_regex

</td><td>

The regular expression of text within command response after sending ‘su’ in order to change to superuser. If the regular expression matches, the MID Server does not change the shell.

-   **Default value**: pfsh
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.permission\_denied\_regex

</td><td>

The regular expression of command responses which the MID Server recognizes as an access problem and generates an appropriate message.

-   **Default value**: permission denied
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.more\_line\_command\_regex

</td><td>

When the SSH response exceeds the terminal size, the system sends ‘more’ line which matches the regular expression. When the MID Server recognizes the ‘more’ line, it sends the space character. This is relevant for proprietary systems sending a non-standard ‘more’ prompt.-   **Default value**: \[empty\]
-   **Type**:
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.become\_superuser\_command

</td><td>

An SSH command for turning into a superuser.-   **Default value**: su
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.prompt\_changing\_command\_regex

</td><td>

SSH commands that change the shell prompt. When the command the MID Server sends matches the regular expression, the MID Server knows to expect a change in the server prompt.-   **Default value**: changeto\\\\s+\[^\\\\s\]+
-   **Type**:
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.ignore\_errors\_on\_commands\_regex

</td><td>

A regular expression for the command on which the MID Server ignores permission errors.-   **Default value**: stat.\*\|istat.\*\|perl.\*
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.prompt\_last\_char\_regex

</td><td>

A regular expression of the last character in the default prompt of the server.-   **Default value**: \[$\#&gt;\\\\\]\\\\:\]
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.timeout

</td><td>

The SSH command timeout \(in milliseconds\).-   **Default value**: 60000
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.port

</td><td>

The SSH port number.To add more than one port, separate port numbers with a comma. For example, 22,33,44.

 -   **Default value**: 22
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.connect.retry

</td><td>

The SSH connection retry count.-   **Default value**: 1
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.additional\_setup

</td><td>

The command the MID Server sends after it creates the SSH session.

-   **Default value**: \[empty\]
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.expect\_after\_su

</td><td>

A regular expression of the last character in the prompt after sendind ‘su’.-   **Default value**: \[:$\#&gt;\\\\\]\]
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.privileged\_command\_last\_char

</td><td>

A character indicating the last expected character in a command result String. Once this character is found in the result, the MID Server does not wait for additional output.-   **Default value**: \[empty\]
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.prompt

</td><td>

A string representing the non-standard SSH prompt. The MID Server uses this string when parsing results of SSH CLI commands.

-   **Default value**: SERVNOW&gt;
-   **Type**:
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.proprietary\_system\_trial\_count

</td><td>

Number of additional waiting periods on proprietary non-UNIX/Linux systems. The MID Server waits for a response after the initial waiting period of 5 seconds. After the initial 5 seconds, the MID Server waits for the response the number of times as defined by this parameter. The additional waiting time starts from 1 second and increases by 1 sec for every iteration.

-   **Default value**: 10
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.restart\_after\_unstopped\_threads

</td><td>

The number of allowed unstopped threads before the MID Server is restarted, when it attempts to close the SSH session.

-   **Default value**: 50
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.stty\_command

</td><td>

The stty command for configuring appropriate settings. The MID Server runs this command when initializing the SSH terminal.

-   **Default value**: \[empty\]
-   **Type**:
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.inocrrect\_password\_regex

</td><td>

The expected string which the SSH terminal returns when the MID Server uses an incorrect password during the login process.

-   **Default value**: Sorry, try again\|incorrect password attempt
-   **Type**:
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.max\_unstopped\_threads

</td><td>

Same as the mid.sa.ssh.restart\_after\_unstopped\_threads parameter.-   **Default value**: 50
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.ssh.idle\_after\_sudo

</td><td>

The period of time \(in milliseconds\) that the MID Server waits after sending a sudo command and expects to have no activity on the line.

-   **Default value**: 3000
-   **Type**:integer
-   **Location:**This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>## WMI-related properties

**Important:** WMI Collector is deprecated in New York patch 10 and later. See the [KB0791835 WMI Collector deprecation details](https://hi.service-now.com/kb_view.do?sysparm_article=KB0791835)for more information.

<table id="table_ah4_hyc_t4b"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mid.servicewatch.wmi.host

</td><td>

The Host/IP of the server running the ServiceNow WMI collector.

-   **Default value**: localhost
-   **Type**: string
-   **Location:** This property is available under specific MID Server parameters as described in [Add a MID Server parameter](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.servicewatch.wmi.port

</td><td>

The port on which the ServiceNow WMI collector service listens to requests from the MID server.-   **Default value**: 8585
-   **Type**: integer
-   **Location:** This property is available under specific MID Server parameters as described in [Add a MID Server parameter](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.wmi.timeout

</td><td>

The timeout on command execution in milliseconds. This property controls also the Powershell commands.-   **Default value**: 60000
-   **Type**: integer
-   **Location:** This property is available under specific MID Server parameters as described in [Add a MID Server parameter](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.wmi.max\_bytes\_in\_response

</td><td>

The maximum number of characters allowed in a response.-   **Default value**: 20971520
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.servicewatch.wmi.get\_file\_on\_shared\_drive\_from\_collector

</td><td>

The MID Server attempts to access the requested file on a shared drive directly from the MID Server.

-   **Default value**: true
-   **Type**: true/false
-   **Location:** This property is available under specific MID Server parameters as described in [Add a MID Server parameter](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.wmi.access\_denied\_regex

</td><td>

The regular expression of error messages returned by server that the MID Server considers as an access problem and triggers trying other credentials.-   **Default value**: Access is denied\|Access denied\|service installation failed\|User credentials cannot be used for local connections\|System error 1312\|generic failure\|Insufficient privilege\|user rights\|HRESULT: 0x800706BA
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.wmi.send\_retry\_count

</td><td>

The number of attempts to commiunicate with the ServiceNow WMI Collector service on each requests.-   **Default value**: 1
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.servicewatch.wmi.mui

</td><td>

The MID Server supports MUI \(Multilingual UI\) configuration.

-   **Default value**: false
-   **Type**: true/false
-   **Location:** This property is available under specific MID Server parameters as described in [Add a MID Server parameter](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.powershell\_api.winrm.remote\_port

</td><td>

Set the port used by WinRM to connect to remote hosts.-   **Default value**: 5985
-   **Type**: integer
-   **Location:** This property is available under specific MID Server parameters as described in [Add a MID Server parameter](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.windows.management\_protocol

</td><td>

The management protocol the MID Server uses to connect to Windows servers. Allowed values are WMI and WinRM.-   **Default value**: WMI
-   **Type**: string
-   **Location:** This property is available under specific MID Server parameters as described in [Add a MID Server parameter](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.servicewatch.wmi.protocol

</td><td>

Communication protocol between the MID Server and the WMI collector. Allowed values: http/https.

-   **Default value**: http
-   **Type**: string
-   **Location:** This property is available under specific MID Server parameters as described in [Add a MID Server parameter](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.use\_powershell

</td><td>

Allows using PowerShell for executing commands on Windows servers.-   **Default value**: false
-   **Type**: true/false
-   **Location:** This property is available under specific MID Server parameters as described in [Add a MID Server parameter](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.prefer\_powershell

</td><td>

Makes PowerShell the preferred method of executing commands on Windows servers.

**Note:** If you set this parameter to true, you must also set the mid.sa.use\_powershell parameter to true.

 -   **Default value**: false
-   **Type**: true/false
-   **Location:** **MID Server** &gt; **Properties**

</td></tr><tr><td>

mid.win.baseboard.or.bios.insertion

</td><td>

Makes the **Windows OS - Servers** pattern discover the BIOS Serial Number instead of the Baseboard Serial Number.

 -   **Possible values**: false - to populate the BaseBoard number; true - to populate the BIOS serial number.
-   **Type**: true/false
-   **Default value**: false
-   **Location:** **MID Server** &gt; **Properties**

</td></tr></tbody>
</table>## SNMP-related properties

<table id="table_alp_xpd_t4b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

mid.snmp.request.timeout

</td><td>

The time \(in milliseconds\) the MID Server waits for a response for each OID request.-   **Default value**: 1500
-   **Type**: Integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.snmp.port

</td><td>

The SNMP port.-   **Default value**: 161
-   **Type**: Integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.snmp.retry

</td><td>

The SNMP retry count.-   **Default value**: 1
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.snmp.table\_size\_limit

</td><td>

Maximum table size to bring in the SNMP table requests.-   **Default value**: 20000
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.snmp.table\_walk\_limit

</td><td>

Maximum requests in the SNMP walk session.-   **Default value**: 10000
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.snmp.get\_table\_timeout\_sec

</td><td>

Maximum time \(in seconds\) allowed for load of a whole SNMP table.-   **Default value**: 600
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.snmp.walk\_timeout\_sec

</td><td>

Maximum time \(in seconds\) allowed for the SNMP walk session.-   **Default value**: 600
-   **Type**: integer
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.snmp.discover\_engine

</td><td>

Discovery authoritative engine ID on SNMP V3 sessions.-   **Default value**: true
-   **Type**: true/false
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.snmp.snmp\_v2\_disabled

</td><td>

Disable usage of SNMP version 2-   **Default value**: false
-   **Type**: true/false
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

mid.sa.snmp.failed\_status\_oid

</td><td>

OID indicating the Failed status. If an SNMP result starts with this OID, the MID Server considers it a failure.

-   **Default value**: 1.3.6.1.6.3.15.1.1.3
-   **Type**: string
-   **Location:** This property is not available in the base system. You can add the property as described in [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Service Mapping reference](service-mapping-reference.md)


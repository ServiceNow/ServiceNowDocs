---
title: SSHCommand parameters
description: Several parameters are available for the SSHCommand probe.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [SSHCommand probe, List of Discovery probes, Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# SSHCommand parameters

Several parameters are available for the SSHCommand probe.

For instructions on configuring probe parameters, see [Set probe parameters](../task/t_SetProbeParameters.md).

<table id="table_kdv_bcm_vp"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

allow\_unsupported\_shells

</td><td>

Allows a probe designer to attempt to run a command on a device that does not have a supported shell. With no shell, the following is true:-   No path information can be provided.
-   No scripts can function, because there is no ability to handle script parameters.
-   The text that is specified in the **ECC queue name** field of the probe form is the raw command that is run on the device.

 For example, you may design a probe to display the version of a Cisco switch running NX-OS. The command that the switch understands is `show version`. To accomplish this, put the `show version` command in the **ECC queue name** field, and add the parameter name `allow_unsupported_shells` with a value of **true**.

 This parameter is only effective for `sncssh`. It is not supported with j2ssh. Currently supported shells are sh, bash, ksh, csh, and tcsh.

 -   Type: string, true or false
-   Default value: false

</td></tr><tr><td>

source

</td><td>

\[Required\] Specifies the initial host to connect to.-   Type: string \(URL\)
-   Default value: None

</td></tr><tr><td>

port

</td><td>

Specifies the target port to connect to.-   Type: integer \(port\)
-   Default value: 22

</td></tr><tr><td>

debug

</td><td>

Specifies whether to write SSH debug information to the log file. The parameter usage depends on whether the ServiceNow SSH client is enabled.When the ServiceNow SSH client is enabled, this parameter functions as follows:

-   Type: string
-   Default value: false

The following string values are valid for the ServiceNow SSH client:

    -   true: Enables SSH debug information in the log file.
    -   false: Disables SSH debug information in the log file.
    -   &lt;IP Addresses&gt;: Specifies which IP ranges to enable SSH debug information in the log file. You can enter IP addresses in the following formats:
        -   An IP range defined by a slash and the number of bits in the subnetwork. For example, the string 10.10.10.0/24 scans 24 bits of IP addresses from 10.10.10.0 to 10.10.10.254.
        -   An IP range defined by a dash. For example, the string 10.10.11.0-10.10.11.165 scans the IP addresses from 10.10.11.0 to 10.10.11.165.
        -   A comma-separated list of specific IP addresses. For example the string 10.10.11.200,10.10.11.235 scans the IP addresses 10.10.11.200 and 10.10.11.235.
    -   deferred: Specifies to log SSH debug information in memory unless an error or warning occurs. If an error or warning occurs, the platform publishes the debug information to the log file. This ensures that only the part of the log file pertaining to the error or warning is recorded. If no error or warning is detected, the platform deletes the unused log data from memory when the session closes. Each session stores up to 1000 log messages. If the session exceeds 1000 log messages, the deferred log discards the oldest log message to make room for the newest log message.

 When the ServiceNow SSH client is disabled, this parameter enables or disables SSH debug information in the log file:

-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

debug\_ssh

</td><td>

Specifies whether the legacy SSH client writes debug information into the `agent/logs/agent.log` log file. **Note:** This log file can grow quickly and should be disabled when not needed.

 The ServiceNow SSH client does not use this parameter.

-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

timeout

</td><td>

Sets the socket connection timeout for the legacy SSH client.The ServiceNow SSH client does not use this parameter.

-   Type: integer \(milliseconds\)
-   Default value: 60,000

</td></tr><tr><td>

path\_override

</td><td>

Specifies how to change the default paths set before executing a command. Type one or more override paths delimited by a colon \(:\). The default path is /usr/sbin: /usr/bin: /bin: /sbin.The ServiceNow SSH client accepts the following prefixes in front of the path\_overide value:

-   append: Appends the override path to the end of the host’s path. This is the default behavior.
-   replace: Replaces the host path with the path\_overide value.
-   prepend: Appends the override path to the front of the host path.

 -   Type: string \(a colon-separated list of directories\)
-   Default value: None

</td></tr><tr><td>

keyboard\_interactive

</td><td>

Determines whether to enforce keyboard\_interactive SSH login mode.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

must\_sudo

</td><td>

Determines whether SSH commands run through sudo.**Note:** must\_sudo probe parameter affects all patterns. On Unix or Linux hosts, pattern execution can run many different commands, some should not have sudo appended.

 -   Type: true \| false
-   Default value: false

</td></tr><tr><td>

run\_in\_terminal

</td><td>

Determines whether SSH commands run in an SSH terminal.-   Type: true \| false
-   Default value:
    -   ServiceNow SSH client: false
    -   Legacy SSH client: true

</td></tr><tr><td>

set\_path

</td><td>

Determines whether the probe is allowed to alter the session's PATH variable or not. By default, during session setup, the PATH variable is set to `/usr/sbin:/usr/bin:/bin:/sbin`.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

rm\_override

</td><td>

Overrides the default remove command `(/bin/rm -f)` with the provided value.-   Type: string
-   Default value: none

</td></tr><tr><td>

use\_snc\_ssh

</td><td>

Enables the ServiceNow SSH client. The ServiceNow SSH client is active by default on new instances. Enabling the ServiceNow SSH client disables the legacy SSH client.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

command\_timeout\_ms

</td><td>

Number of milliseconds an SSH command is allowed to run before timing out \(default is configurable per MID server\).The legacy SSH client does not use this parameter.

-   Type: integer
-   Default value: value of the mid.ssh.command\_timeout\_ms MID Server parameter.

</td></tr><tr><td>

channel\_timeout\_ms

</td><td>

Specifies the amount of time, in milliseconds, that a MID Server waits for activity during processing of an SSH command. If the MID Server does not detect activity in the specified timeout window, this parameter kills the command. -   Type: integer \(milliseconds\)
-   Default value: 300000 \(5 minutes\)

</td></tr><tr><td>

preserve\_sudo\_environment

</td><td>

Specifies whether to use sudo to preserve the environment for SSH. This parameter is only effective if the sudo environment on the host being probed supports the `-E` switch.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

credentials\_debug

</td><td>

Displays a &lt;credentials\_debug&gt; section in the ECC queue, which can help you troubleshoot credentials. If you set this property to true, credential troubleshooting information is output to the ECC queue, even if the credentials succeed. See [Credentials Troubleshooting](https://www.servicenow.com/docs/access?context=r_CredentialTroubleshooting&version=australia&pubname=australia-platform-security&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[SSHCommand probe](../concept/c_SSHCommandProbe.md)


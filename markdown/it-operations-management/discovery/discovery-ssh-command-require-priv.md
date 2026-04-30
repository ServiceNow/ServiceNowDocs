---
title: SSH commands requiring a privileged user during probe-based discovery
description: These tables display the SSH commands run by Discovery probes during horizontal discovery. These SSH commands require elevated privileges to run.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [SSH commands, SSH probe commands, probe commands, elevated privileges]
breadcrumb: [SSHCommand probe, List of Discovery probes, Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# SSH commands requiring a privileged user during probe-based discovery

These tables display the SSH commands run by Discovery probes during horizontal discovery. These SSH commands require elevated privileges to run.

## Operating system commands requiring elevated rights

These examples assume that the user name is **Disco**. Substitute the actual user name and verify that the paths for the commands match the paths on the system.

**Note:** Sudo commands don’t work with private key credentials, because there’s no password to supply to the sudo command. A solution is to add the NOPASSWD option to the sudo configuration. For example, you might enter: `disco ALL=(root) NOPASSWD:/usr/sbin/dmidecode,/usr/sbin/lsof,/sbin/ifconfig`.

For information on commands that don’t require elevated rights, see [SSH commands not requiring a privileged user during probe-based discovery](discovery-ssh-probe-commands.md).

For information on commands used by Service Mapping during the top-down discovery, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md) and [Service Mapping commands not requiring a privileged user](../../service-mapping/reference/r_NonSudoCommands.md).

## SSH key not validated

When the MID Server connects to a system, the MID Server doesn’t perform host key validation against that system and so treats it as untrusted. If an attacker performs a man-in-the-middle attack and redirects the traffic to a malicious SSH service, the attacker can intercept or modify any data sent over the connection.

Therefore, limit any sensitive information exchanged between the MID Server and the target SSH server. Only use keys or certificates for SSH authentication, and avoid sending system credentials. Configure NOPASSWD in the sudoers file for the required privileged commands.

<table id="table_fsp_m5r_52c"><thead><tr><th>

Command

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

`adb`

</td><td>

Gathers CPU speed and memory.**/etc/sudoers line example**: `Disco ALL=(root) /usr/bin/adb`

</td></tr></tbody>
</table><table id="table_t32_t5r_52c"><thead><tr><th>

Command

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

`dmidecode`

</td><td>

Gathers several pieces of information about the hardware, including the serial number embedded within the motherboard.**/etc/sudoers line example**: `Disco ALL=(root) /sbin/dmidecode`

</td></tr><tr><td>

`fdisk`

</td><td>

Gathers the disks and size information on the system.**/etc/sudoers line example**: `Disco ALL=(root) /usr/bin/fdisk -l`

</td></tr><tr><td>

`multipath`

</td><td>

Gathers device mappings for MultiPath Input Output \(MPIO\).**/etc/sudoers line example**: `Disco ALL=(root) /usr/bin/multipath -ll`

</td></tr></tbody>
</table><table id="table_fjp_z5r_52c"><thead><tr><th>

Command

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

`dmsetup`

</td><td>

Examines a low-level volume. **/etc/sudoers line example**

 -   `Disco ALL=(root) /usr/bin/dmsetup table *`
-   `Disco ALL=(root) /usr/bin/dmsetup ls`

</td></tr></tbody>
</table><table id="table_sqb_fvr_52c"><thead><tr><th>

Command

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

`lsof`

</td><td>

Determines the relationship between processes and the connections being made to the system.**/etc/sudoers line example**: `Disco ALL=(root) /sbin/lsof`

</td></tr><tr><td>

`oratab`

</td><td>

Grants read access to the oratab file for locating the Oracle Home and pfile.

</td></tr><tr><td>

`netstat`

</td><td>

Determines the relationship between processes and the connections being made to the system.**/etc/sudoers line example**: `Disco ALL=(root) /bin/netstat`

</td></tr><tr><td>

`ss`

</td><td>

Determines the relationship between processes and the connections being made to the system.**/etc/sudoers line example**: `Disco ALL=(root) /sbin/ss`

</td></tr></tbody>
</table><table id="table_kzq_jvr_52c"><thead><tr><th>

Command

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

`iscsiadm`

</td><td>

Gets iSCSI qualified names \(IQNs\).**/etc/sudoers line example**: `${sudo:iscsiadm list target -S}`

</td></tr><tr><td>

`fcinfo`

</td><td>

Gets World Wide Port Names \(WWPNs\) for ports.**/etc/sudoers line example**: `${sudo:fcinfo remote-port -sl -p $port}`

</td></tr><tr><td>

`prtvtoc`

</td><td>

Reports information about disk partitions.**/etc/sudoers line example**: `Disco ALL=(root) /usr/bin/prtvtoc`

</td></tr><tr><td>

`/usr/bin/ps`

</td><td>

Lists running process. As an alternative to running with root access, add a proc\_owner role.sola.**/etc/sudoers line example**: `Disco ALL=(root) /usr/bin/ps`

</td></tr><tr><td>

`/usr/ucb/ps`

</td><td>

Lists running process. As an alternative to running with root access, add a proc\_owner role. The use of the `/usr/ucb/ps` command is deprecated as of Solaris 11. Because Discovery requires the use of this command for all Solaris versions, you must install the ucb utility manually on Solaris 11 systems. For instructions, see [KB0564262](https://support.servicenow.com/kb_view.do?sysparm_article=KB0564262).

 **/etc/sudoers line example**: `Disco ALL=(root) /usr/ucb/ps`

</td></tr><tr><td>

`pgrep`

</td><td>

Gets list of process IDs \(PIDs\) with socket information.**/etc/sudoers line example**: `Disco ALL=(root) /usr/bin/pgrep`

</td></tr><tr><td>

`pfiles`

</td><td>

For each PID, gets and processes the output for S\_IFSOCK.**/etc/sudoers line example**: `Disco ALL=(root) /usr/bin/pfiles`

</td></tr></tbody>
</table>**Parent Topic:**[SSHCommand probe](../concept/c_SSHCommandProbe.md)

**Related topics**  


[Discovery commands for probes and patterns](../concept/discovery-command-probe-pattern.md)


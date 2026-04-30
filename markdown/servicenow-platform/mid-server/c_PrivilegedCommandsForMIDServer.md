---
title: MID Server privileged commands
description: To discover certain information on a host server, the MID Server must run SSH commands with higher privileges. The platform provides default privileged commands for the MID Server to use and the ability to add additional commands to the system.Configure J2SSH and ServiceNow SSH to prevent long running commands using sudo from failing when the MID Server disconnects.Add a new privileged command to the Privileged Command \[privileged\_command\] table that is available to your MID Servers.You can configure the MID Server to use specific commands in a defined order.You can create a special configuration for the pbrun privileged command that allows it to run as a profile.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server privileged commands

To discover certain information on a host server, the MID Server must run SSH commands with higher privileges. The platform provides default privileged commands for the MID Server to use and the ability to add additional commands to the system.

<table id="table_y14_tv4_nhb"><tbody><tr><td>

![Links to each of the MID Server sections](../image/MIDRefIconBar.png)

</td></tr></tbody>
</table>An example of information that requires elevated privileges is information about storage disks on a host server, retrieved with the `fdisk -l` command. If your system cannot use sudo commands, you must configure the hosts in your network to use one of the other privileged commands. You can configure different privileged commands for different hosts. However, Discovery supports only one privileged command per host.

**Important:** You can edit supported privileged commands, but do not delete them.

For a list of possible SSH commands requiring root privileges, see [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

<table id="table_zgn_3wb_dt"><thead><tr><th>

Command

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sudo

</td><td>

-   Host must support the `sudo -S -p <password>` command and return the correct list of allowed SSH commands.
-   Credentials provided for Discovery must be able to run the command `sudo -S -p <password> <commands>`.
-   Discovery calls `sudo -l` to determine whether `sudo` is available on the host and which commands the current user can run with elevated privileges.

</td></tr><tr><td>

pbrun

</td><td>

-   Host must support the `pbrun -v` command and return the correct version of PowerBroker.
-   Credentials provided for Discovery must be able to run `pbrun <commands>`.
-   Discovery does not support any other **pbrun -** options, such as a password prompt.
-   The instance must be able to reach the target host via SSH.

</td></tr><tr><td>

pfexec

</td><td>

-   Host must support the `pfexec id -a` command and return the correct ID.
-   Credentials provided for Discovery must be able to run `pfexec <commands>`.
-   Discovery does not support any other **pfexec -** options, such as a password prompt.

</td></tr><tr><td>

dzdo

</td><td>

-   Host must support the `command –v dzdo` command and return the path to dzdo in standard output.
-   Credentials provided for Discovery must be able to run dzdo &lt;commands&gt;.
-   Discovery does not support any other `dzdo –` options, but Discovery supports password authentication for dzdo.

</td></tr></tbody>
</table>**Parent Topic:**[MID Server reference](mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements](../reference/r_MIDServerSystemRequirements.md)

[MID Server upgrades](c_UpgradeAndTestMIDServer.md)

[Resolving MID Server issues](../reference/r_MIDServerTroubleshooting.md)

[MID Server dashboard](c_MIDServerDashboard.md)

[MID Server properties](../reference/r_MIDServerProperties.md#)

[MID Server parameters](../reference/mid-server-parameters.md#)

[MID Server Configuration Parameter settings and priority](../reference/mid-config-param-priority.md)

[MID Server File Cleaner](mid_file_cleaner.md)

[MID Server protected records and reserved characters](../reference/mid-server-reserved-characters.md)

[MIDSystem methods](../reference/r_MIDSystemMethods.md)

[Manually start, stop, and restart a MID Server](../task/t_InstallMIDServerAsWinService.md)

[MID Server heartbeat](../reference/r_MIDServerHeartbeat.md)

[Set the MID Server JVM memory size](../task/t_MIDServerOptionalConfiguration.md)

[Pause the MID Server](../task/t_PauseTheMIDServer.md#)

## Long-running commands with sudo

Configure J2SSH and ServiceNow SSH to prevent long running commands using sudo from failing when the MID Server disconnects.

ServiceNow SSH allows probes to run sudo against individual commands or an entire, long-running script. This is also supported for the **pbrun** and **pfexec** privileged commands.

### Sudo for individual commands

You can run sudo against individual commands within a probe, but only if all the following sudoer configurations are performed on the target:

-   The `!requiretty` option is required.
-   Allow individual commands to be run by the user in the provided credential with `NOPASSWD` configured.
-   The target specifies an individual sudo call in the command or referenced scripts. For example, set sudo as `"sudo fdisk -I"` or `"${sudo:fdisk -I}"` rather than `"must_sudo"` for the entire script.

**Note:** Running sudo against individual commands with ServiceNow SSH produces detailed and useful entries in the sudo logs on the target computer.

### Running sudo on an entire script

If any of the required sudoer configuration requirements for individual commands is not in place, Discovery applies sudo to the initial and complete probes, and does not execute sudo remotely inside the command. This condition can be forced by setting **must\_sudo** on the probe and eliminating any sudo commands within the probe.

This approach prevents long running commands from failing when the probe disconnects, but cannot specify individual commands in the sudoers configuration.

### Logging

The logs from ServiceNow SSH sudo activity run against an entire script show cryptic entries, such as `/tmp/.run.aef13123fe124123`, which prevent administrators from controlling permissible commands and knowing the exact command that was run. Sudo run against individual commands produces more detailed log entries, such as `/sbin/fdisk –l`.

## Add a new privileged command for use by the MID Server

Add a new privileged command to the Privileged Command \[privileged\_command\] table that is available to your MID Servers.

### Before you begin

Role required: admin

### About this task

**Important:** Do not delete any of the supported commands.

### Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Privileged Command** and click **New**.

2.  Complete these fields:

    -   **Command**: The name of the privileged command.
    -   **Password Prompt**: The password prompt displayed to the user for this privileged command, or a regular expression that matches this password prompt. If this field is empty, no password is required for this privileged command, and no prompt is displayed. SUDO commands do not require a password prompt.
3.  Click **Submit**.


## Configure the MID Server to use specific privileged commands

You can configure the MID Server to use specific commands in a defined order.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to the list of MID Servers using one of the following paths:

    -   **MID Server** &gt; **Servers**
    -   **Discovery** &gt; **MID Servers**
    -   **Orchestration** &gt; **MID Servers**
2.  Select the MID Server you want to configure.

3.  Click the menu icon in the header bar and select **View** &gt; **Advanced** from the context menu.

    ![Selecting the Advanced view](../image/MIDServerAdvancedView.png "Selecting the Advanced view")

4.  In the **Privileged Command** related list, click **Edit**.

5.  Select the command you want this MID Server to use and click **Save**.

    The default order of privileged commands is 100, but you can change the order as necessary. The privileged command with the smallest order number is tried first.

    ![List of privileged commands to use for a MID Server](../image/MIDSelectPrivilegedCommand.png "List of privileged commands to use for a MID Server")


## Create a pbrun profile privileged command

You can create a special configuration for the **pbrun** privileged command that allows it to run as a profile.

### Before you begin

Role required: discovery\_admin, admin

### About this task

Of all the privileged commands, only the **pbrun** command can be configured to run as a profile, and only one of these special **pbrun** configurations can function on a MID Server.

**Important:** Edit the existing **pbrun** record for this purpose. The system ignores any additional commands you create for **pbrun**.

### Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Privileged Command**.

2.  Select **pbrun** from the list.

3.  In the Privileged Command record, edit the value in the **Command** field to use the format **pbrun -u &lt;profile&gt;**.

    For example, you can set **pbrun -u admin** as a command to run with an admin profile.

4.  Click **Update**.


### What to do next

Return to [Configuring MID Servers](c_MIDServerConfiguration.md).


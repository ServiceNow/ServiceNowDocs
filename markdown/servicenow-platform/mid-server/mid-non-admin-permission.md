---
title: File permission enforcement for Windows MID Servers
description: To improve security, Windows MID Servers enforce Windows file permission restrictions. The enforcement limits access to the MID Server files to a restricted allow list of users and groups.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# File permission enforcement for Windows MID Servers

To improve security, Windows MID Servers enforce Windows file permission restrictions. The enforcement limits access to the MID Server files to a restricted allow list of users and groups.

<table id="table_p53_ms4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>File permission enforcement for Windows MID Servers goes into effect on the MID Server on start up in Orlando. By default the agent folder is locked to four user accounts and groups: the local admin group, the system account, creator owner, and the user account the Windows MID Server is using. The list of permitted user accounts is managed by a allow list, which is controlled by the MID Server parameter **mid.windows\_host.file\_permissions.allow\_list**. This parameter takes a string of comma separated group names, user names, and security identifiers \(SID\). Group and user names must follow SAM account naming requirements. Domain accounts must be specified by using the SID.

## Roll back file permission changes

Changes to the file permissions are recorded, and the last used settings are saved in the `/etc` folder as a backup. The file is `fileperm.aclsave`. Open a command prompt and run the command `icacls <agent_folder> /restore <agent_folder>/etc/fileperm.aclsave` where &lt;agent\_folder&gt; is name of your agent folder.

## Run a MID Server as a non-admin

To run a MID Server as a non-admin user, it must first be installed using an admin account. Then add the non-admin user to allow list and restart the MID Server. Once the new enforcement rules run, the MID Server can be switched to the non-admin service account. See [Run a Windows MID Server as a non-admin after manual installation](mid-server-install-prereqs.md#) for more information on setting up non-admin Windows MID Servers, or [Run Linux MID Servers as non-root users](../task/t_InstallAMIDServerOnLinux.md#) for Linux MID Servers.


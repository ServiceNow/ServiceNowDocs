---
title: VMware credentials
description: The VMware credentials type manages access to vCenter credentials.
locale: en-US
release: xanadu
product: Connections and Credentials
classification: connections-and-credentials
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create and test your credentials, Getting started with credentials, Connections and Credentials, Access Management]
---

# VMware credentials

The VMware credentials type manages access to vCenter credentials.

Applications that access VMware cloud resources need access to VMware credentials. For example, the VMware credential type enables Discovery to explore VMware's vCenter running on a Windows machine to discover ESX machines, virtual machines, and resource pools. The VMware Discovery and automation API \(vCenter API\) now provides the globally unique serial number for computer CIs. CIM credentials aren’t needed to enable access to each VMware host.

**Note:** Windows credentials aren’t necessary for vCenter Discovery, when valid VMware credentials are used.

**Important:** Do not use **VMware** Type credentials for Orchestration activities that perform work on the individual virtual machines cloned by vCenter \(for example, restarting a Linux VM\). For these activities, the credential **Type** depends on the operating system of the virtual machine \(either **SSH** or **Windows**\).

<table id="table_yks_3g2_3z"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique and descriptive name for the VMware credentials.

</td></tr><tr><td>

Active

</td><td>

Enable or disable these credentials for use.

</td></tr><tr><td>

User name

</td><td>

Enter the user name that you use for your VMware account. Avoid leading or trailing spaces in user names. A warning appears if the platform detects leading or trailing spaces in the user name. The VMware credentials must have the read-only role in vCenter.

</td></tr><tr><td>

Password

</td><td>

Enter the password for the VMware account.

</td></tr><tr><td>

Applies to

</td><td>

Select one or more MID Servers from the list of available MID Servers. The credentials configured in this record are available to the MID Servers in this list. This field is available only when you select **Specific MID servers** from the **Applies to** field.

</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr></tbody>
</table>
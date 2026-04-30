---
title: Discovery for VMware Cloud
description: Applications that access VMware cloud resources need access to VMware credentials.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery for VMware Cloud

Applications that access VMware cloud resources need access to VMware credentials.

For example, the VMware credential type enables Discovery to explore VMware's vCenter running on a Windows machine to discover ESX machines, virtual machines, and resource pools. The VMware Discovery and automation API \(vCenter API\) now provides the globally unique serial number for computer CIs. CIM credentials aren’t needed to enable access to each VMware host.

**Note:** Windows credentials aren’t necessary for vCenter Discovery, when valid VMware credentials are used.

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
</table>**Related topics**  


[Configure the VMware Events service to auto-update the CMDB](../../it-operations-management/task/vmware-events-service-cloud-mgt.md)

[Create a VMware Discovery schedule in Discovery Admin Workspace](../task/create-vmware-schedule-DAW.md)


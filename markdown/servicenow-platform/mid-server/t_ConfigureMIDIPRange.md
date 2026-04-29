---
title: Configure an IP address range for the MID Server
description: You can manually configure an IP address range for the MID Server to explore.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [MID Server selection, Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Configure an IP address range for the MID Server

You can manually configure an IP address range for the MID Server to explore.

## Before you begin

Role required: agent\_admin or admin

<table id="table_ifn_4s4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>## About this task

Applications, such as Discovery and Orchestration, can specify an IP range or the specific IP address of a target. When the application looks for a MID Server to use during auto-selection, it chooses a MID Server whose IP range includes the application's range or specific IP address. Applications also use other criteria, such as the MID Server's supported application or capability. See [MID Server selection](../concept/c_MIDServerSelector.md) for more information.

**Note:** This is a manual configuration procedure. To learn how the system can assign IP address ranges to selected MID Servers automatically, see [Using MID Server IP range auto-assignment](../concept/mid-servers-auto-assignment.md#).

These applications use IP ranges as follows:

-   **Orchestration**: Use the IP address of the target machine \(together with the capability\) to select the correct MID Server for Orchestration activities. See the procedure in this topic to configure the IP address.
-   **Service Mapping**: Select the MID Server whose IP address range matches the IP in the discovery request. See [MID Server configuration for Service Mapping](https://www.servicenow.com/docs/access?context=configure-mid-service-mapping&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) for more information.
-   **Discovery**: Can select an IP address range using the same criteria as Service Mapping. Discovery can also use a [quick IP range](https://www.servicenow.com/docs/access?context=discovery-ip-address-configuration&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) that you specify in the Discovery schedule.

**Tip:** You can also use the **ALL** IP range, which allows the MID Server to be used with any range of IP addresses that an application specifies. This only allows the MID Server to access IP ranges, it does not mean that the MID Server can actually reach all of the IP ranges. To function with an application, the MID server must have access to the IP ranges that the application needs.

Valid IP address ranges can be as follows:

An IP address in dotted decimal or hexadecimal format. The hexadecimal format can be explicitly prefixed with 0x, this is not mandatory. Here are examples:

-   10.11.144.155
-   0x0A0B909B
-   0A0B909B

An IP address range in dotted decimal or hexadecimal format. Here are examples:

-   10.11.144.150-10.11.144.160
-   0x0A0B9096-0x0A0B90A0
-   10.11.144.150-0x0A0B90A0

An IP network address with the net mask specified after a slash \(/\) in regular notation \(0-32 inclusive\) or in IP address notation. Here are examples:

-   10.11.144.0/24 10.11.144.0/255.255.255.0
-   10.11.144.0/0xFFFFFF00
-   0x0A0B9000/24
-   0x0A0B9000/0xFFFFFF00

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **IP Ranges**.

2.  Click **New**.

3.  Complete the form, using the fields in the table.

    ![IP address ranges](../image/IPRangeForm.png "IP address ranges")

<table id="table_flk_pk1_mw"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a descriptive name.

</td></tr><tr><td>

Application

</td><td>

Application scope for this IP range. The default is **Global**.

</td></tr><tr><td>

Type

</td><td>

Select the type of range: -   **Include**: Include the specified IP range.
-   **Exclude**: Exclude the IP address range.

**Note:** If a MID Server is configured for **ALL** applications, any IP addresses configured for exclusion are ignored by the system. If your goal is to configure default MID Servers for separate applications in your system, see [Configure a default MID Server for each application](t_SpecifyMIDServerApplications.md#).

</td></tr><tr><td>

Range

</td><td>

Enter the range in a valid format.

</td></tr><tr><td colspan="2">

**Related list**

</td></tr><tr><td>

MID Servers

</td><td>

The MID Servers that can use this IP address range.

</td></tr></tbody>
</table>4.  Click **Save**.

    **Important:** IP ranges assigned manually prior to using auto-assignment in the [Discovery Quick Start](https://www.servicenow.com/docs/access?context=discovery-quick-start&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) are affected as follows:

    -   Individual IP ranges are retained and appended to the ranges assigned automatically by the system for the designated MID Server.
    -   If the MID Server was configured with the **ALL** ranges selection, the auto-assignment feature overwrites that designation with the ranges it finds.

## What to do next

Open the **ALL** IP range record and configure the MID Servers that you want to use with any set of IP addresses.

**Parent Topic:**[MID Server selection](../concept/c_MIDServerSelector.md)


---
title: Map an IP address to a DNS name
description: Associate the IP address to a DNS name to ensure the appropriate MID Server is selected. The IP Address range configuration determines which MID Server is selected. If the MID Server manages resources within defined IP ranges, all host servers must have their DNS names mapped to an IP address.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Map an IP address to a DNS name

Associate the IP address to a DNS name to ensure the appropriate MID Server is selected. The IP Address range configuration determines which MID Server is selected. If the MID Server manages resources within defined IP ranges, all host servers must have their DNS names mapped to an IP address.

## Before you begin

Role required: admin

<table id="table_wd3_ss4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>The association of an IP address to a DNS name ensures that the appropriate MID Sever is selected based on the IP Address range configuration. If this is not done, Orchestration reverts to the default MID Server.

If Discovery cannot discover the server and resolve the DNS name to an IP address, you must create the mapping manually.

**Important:** The platform does not map **localhost** to 127.0.0.1 automatically. You must create that mapping using this procedure.

## Procedure

1.  Enter **cmdb\_ci\_dns\_name.list** in the navigation filter.

    A list of DNS names appears.

2.  Check the list for your host server.

    If the server does not appear in the list, continue with this procedure.

3.  Click **New**.

4.  Enter the fully-qualified domain name \(FQDN\) of the host server in the **Name** field.

5.  Right-click in the form header and select **Save** from the context menu.

6.  In the **IP Address** related list, click **New**.

7.  In the **IP Address** field, enter the IP address of your host server.

8.  In the **Nic** field, select **eth0** or your preferred network interface controller.

9.  Leave the **Netmask** field blank.

10. Click **Submit**.


**Parent Topic:**[Configuring MID Servers](../concept/c_MIDServerConfiguration.md)


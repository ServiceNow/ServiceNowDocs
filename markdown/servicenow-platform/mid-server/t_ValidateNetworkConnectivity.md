---
title: Test MID Server connectivity
description: Confirm that the MID Server host is able to communicate with the instance. Resolve any issues with the network connectivity such as conflicts with firewalls, access control lists, and routing errors. Successful communication is necessary for automatic upgrades.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Installing the MID Server, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Test MID Server connectivity

Confirm that the MID Server host is able to communicate with the instance. Resolve any issues with the network connectivity such as conflicts with firewalls, access control lists, and routing errors. Successful communication is necessary for automatic upgrades.

## Before you begin

Role required: admin

<table id="table_jjm_fs4_nhb"><tbody><tr><td>

![Set up indicator for installation phase](../image/ProgressBarInstall.png)

</td></tr></tbody>
</table>## About this task

The computer that hosts the MID Server must be able to access one of these URLs to upgrade automatically:

-   HTTPS: `https://install.service-now.com on the default HTTPS port (443)`
-   HTTP: `http://install.service-now.com on the default HTTPS port (80)`

## Procedure

1.  Use PING to test connectivity with the host on the network \(ping&lt;host IP&gt;\).

2.  If no ping response is returned, use TRACEROUTE to see where traffic might be stopped \(traceroute&lt;host&gt;\).

3.  Use TELNET to connect to any of the TCP ports \(telnet&lt;host&gt; &lt;port&gt;\).

4.  Use an SNMP scanning tool to determine if a potential network device is responsive.

5.  Resolve the most likely issues around network connectivity:

    -   Routing: Confirm that the MID Server host has network access to the IP ranges you are attempting to discover.
    -   Firewalls: Confirm access to the physical firewalls that protect a large environment such as the Data Center. Confirm access to any logical firewalls that protect an individual computer. MID Server communications are initiated inside the firewall and therefore do not require any special firewall rules or VPNs.
    -   Access Control Lists \(ACL\): Confirm that ACLs contain the IP addresses based list on SNMP network devices that allows communication to a particular target.
    -   Resolve all issues with your network teams to better understand your topology. Deploy additional MID Servers if necessary to help keep your network secure. Configure access from your existing MID Server host to networking components.
6.  Verify that the MID Server service is running on the host:

    -   Windows: In the Windows Services console, locate the **ServiceNow \[MID Server name\]** and confirm that each MID Server has the **Started Status** value.
    -   Linux: Ensure that the `agent0.log.0.lck` appears in the `/servicenow/ MID Server name]/agent` folder.
7.  After each MID Server restart, open the `agent0.log.0` and address all error messages.

8.  From the ServiceNow instance, navigate to **MID Server** &gt; **Servers**.

9.  Review and verify that all MID Servers that are connected to the instance are listed.

10. Verify that the **Status** is **Up** for the MID Servers.


## What to do next

This concludes the installation of a single MID Server. If necessary, continue to [deploy multiple MID Servers from a single host](t_InstallMultplMIDSvrOnASingleSys.md#) in your network. Otherwise, begin [configuring your MID Server](../concept/c_MIDServerConfiguration.md).


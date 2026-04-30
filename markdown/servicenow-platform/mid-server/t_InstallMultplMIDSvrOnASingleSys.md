---
title: Install multiple MID Servers on a single system
description: Install multiple MID Servers on the same host computer. Multiple MID Servers can support each other with load balancing, as well as use domain separation. The number of MID Servers required is determined by factors like network policies, security restraints, and the reliability of the host computer.Depending upon how you use the MID Server \(for an external integration, Discovery, Service Mapping, or Orchestration\) and the load placed on it, you might find it necessary to deploy multiple MID Servers in your network.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Installing the MID Server, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Install multiple MID Servers on a single system

Install multiple MID Servers on the same host computer. Multiple MID Servers can support each other with load balancing, as well as use domain separation. The number of MID Servers required is determined by factors like network policies, security restraints, and the reliability of the host computer.

## Before you begin

Role required: admin, mid\_server

<table id="table_eyr_gs4_nhb"><tbody><tr><td>

![Set up indicator for installation phase](../image/ProgressBarInstall.png)

</td></tr></tbody>
</table>## About this task

You can install multiple MID Servers on a Linux or Windows host or on a virtual machine. Installing multiple MID Servers may involve other setup steps depending on your network configuration.

**Important:** Only one MID Server service can be a daemon on a Linux host. This is a limitation of the Tanuki wrapper service.

## Procedure

1.  Log in to the host system or virtual machine where you want to install multiple MID Servers.

2.  Create a directory for each MID Server on the top level of the drive.

    Make sure you create a unique and descriptive name for each MID Server, such as MIDServer\_SMS\_Int or MIDServer\_Disc1.

3.  Extract the downloaded MID Server archive file into each MID Server directory.

    When the extract completes, there should be a directory path similar to the following for each MID Server: `ServiceNow<MID Server name>\agent`.

4.  For each MID Server, run the installer appropriate to the host's operating system.

    |Operating System|Installer path|
    |----------------|--------------|
    |Windows|`/agent/start.bat`|
    |Linux|`/agent/installer.sh`|

5.  Use the installer to enter the following information.

    -   URL to your instance
    -   User credentials to run the MID Server
    -   Proxy server connection details
    -   MID server name
    -   MID server service wrapper name and display name \(Windows systems only\)
    **Note:** The MID Server user must have the mid\_server role.

6.  From the installer, click **Start MID Server**.

    ![Installer screen](../image/MIDServerInstallerStartMIDServer.png)

    The local host starts the MID Server.

7.  Click **Mid Servers List Page**.

    The installer opens the MID Server list from your instance.

8.  Select the MID Server name from the list.

    **Note:** It may take a few seconds for the MID Server time to establish a connection with your instance.

    The system displays the MID Server record.

9.  From **Related Links**, click **Validate**.

    The MID Server **Validated** changes to **Yes**.


## What to do next

All MID Server installation procedures are complete. Proceed to [configure your MID Server](../concept/c_MIDServerConfiguration.md).

## Multiple MID Server deployments

Depending upon how you use the MID Server \(for an external integration, Discovery, Service Mapping, or Orchestration\) and the load placed on it, you might find it necessary to deploy multiple MID Servers in your network.

Factors determining the number of MID Servers your network will require to support external applications that integrate with ServiceNow include the following:

-   The security constraints in your network.
-   Your network policies.
-   The amount of traffic between ServiceNow and the integrations.
-   The reliability of the MID Server machines.

### Network policies and security

Security policies in your network \(firewalls between network segments, for example\) might make direct communication impossible between your instance and an integration's data source \(JDBC, LDAP, etc.\). To retrieve data for the instance, you can install a MID Server that has access to both the data source and the instance.

These network policies can determine if you need to install multiple MID Servers in your environment:

-   **Access control lists \(ACL\)**: If your security policy controls access to network devices \(e.g. switches and routers\) with an ACL, it might be necessary to install one or more MID Servers on a machine in the network that is already on the ACL.
-   **DMZ**: Your network policy might require you to install one or more MID Servers in your DMZ to probe the devices there. This is common in networks that tightly regulate the ports that are opened on the inside firewall.
-   **Probe types**: If you are conducting probes of different operating systems, your network policy might require a separate MID Server for each type of probe \(e.g., one MID server for Windows WMI probes and another for SSH probes on UNIX\).

### Load balancing

Deploy multiple MID Servers where capacity is an issue, as when Discovery has to gather information about thousands of configuration items quickly. In a high volume environment, it might be necessary to deploy multiple MID Servers as load balancers for certain transactions. For example, JDBC data transfers can tie up the resources of a MID Server, making it unable to respond to other requests. The following operations between an integration might require separate MID Servers in a busy network:

-   File exports
-   Running scripts
-   JDBC data sources
-   Reading files

### High availability model

Avoid installing MID Servers for critical integrations on a machine that might experience any type of planned outage or an outage caused by overloaded processes. If necessary for reliability, consider deploying these types of MID Servers to dedicated machines for high reliability

**Note:** Do not integrate with an external application on a MID Server provisioned for ServiceNow Discovery or Orchestration.

### Wide area network \(WAN\)

When determining where to deploy MID Servers in a WAN, consider the bandwidth available between your local area networks. In most cases, install a MID Server on each LAN to probe devices locally, rather than deploying MID Servers that must probe devices across slow WAN connections. An alternative to this type of deployment is to install MID Servers that probe other LANs via VPN connections that take advantage of fast Internet connections. If the bandwidth of your WAN connections is comparable to that of your Internet connection, then there is no performance impact in running MID Server probes across WAN connections.

### Domain separation

In deployments where domain separation is enabled and domains are configured to form a hierarchy, place the MID Servers at the lowest domain level.

![Deploying MID Servers with domain separation](../image/MIDServerDomainDeployment.png "Deploying MID Servers with domain separation")


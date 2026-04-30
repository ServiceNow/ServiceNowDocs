---
title: Prepare network connections for MID Servers
description: Before you install the MID Server, perform the necessary prerequisites that it needs to connect to elements inside and outside your network. This includes network privileges and security considerations.Prepare the network for MID Servers to connect with the instance and access the download site. The network must be prepared before installing or configuring the MID Server. If computers or devices have additional security measures, that security may interfere with MID Servers on those systems.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 11
breadcrumb: [Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Prepare network connections for MID Servers

Before you install the MID Server, perform the necessary prerequisites that it needs to connect to elements inside and outside your network. This includes network privileges and security considerations.

## Security considerations

Sometimes computers or devices have additional security measures configured, and these measures may interfere with the MID Server's ability to run commands or queries on those systems.

For example, a Linux server might be configured to allow only certain IP address to connect to it via SSH. Similarly, a network router might be configured to allow only certain IP address to query SNMP on it. To allow access in such cases, use one of the following methods:

-   Update the configuration of those computers or devices to allow the desired MID Server to run commands or query them. For example, a network router may be configured to only allow the network management systems to query SNMP on it. In that case, add the MID Server as though it were another network management system.
-   Install a MID Server on a computer that already has access to the computers or network devices with such restrictions. For example, to use Discovery within a DMZ \(where communication from outside the DMZ will be severely restricted\), install a MID Server on a computer that is already in the DMZ.

## Credential spray

The MID Server uses its host’s Windows Server Message Block \(SMB\) client and configuration to connect to other Windows machines. If Windows is configured to use legacy protocols, the connection is vulnerable to man-in-the-middle attacks that can result in weak password disclosure and remote code execution.

Use the following host configuration to limit the impact of an attacker with a man-in-the-middle vantage point:

-   Ensure that SMB Signing is configured to be **Required** on the client MID Server to limit potential attacks on the integrity.

-   Ensure that SMB Signing is required by all SMB servers within the environment.

-   Use strong passwords to limit offline dictionary attacks if the host machine must support legacy authentication protocols such as NetNTLM.

-   Use a unique account for each relevant host to limit the impact of compromised credentials on the end systems.


## External connectivity requirements

These requirements are specifically for the use of MID Servers with the ServiceNow® Discovery and Orchestration products.

The MID Server communicates securely on port 443 to the instance and requires no inbound connections. In some cases, it might be necessary to allow this communication through the firewall if the MID Server fails to register on the instance. To determine if the application or a network security restriction is to blame for connection failure, attempt to telnet to the instance on port 443 from the server that is hosting the MID Server application. If this connection fails, then the problem could be a web proxy \(since 443 is an https connection\) or a Firewall rule preventing external TCP connections from that host. Contact network security personnel for the proxy information to add to the config.xml file, or request that the firewall be configured to allow access using one of the following syntaxes:

-   `<source IP> to <any>`
-   `<source IP> to <ServiceNow> any established`
-   `<source IP> to <instance\_name.service-now.com> 443`

**Important:** The MID Server host computer must have access to the ServiceNow download site at `install.service-now.com` to upgrade automatically. If you have a self-hosted ServiceNow environment that blocks access to the download site, you must import the MID Server installer package into your MID Server hosts manually. For instructions, see [KB0760123](https://support.servicenow.com/kb_view.do?sysparm_article=KB0760123) in the Self-Hosted knowledge base.

## Internal connectivity requirements

These methods are used for discovering various devices on a network and are specifically for the use of MID Servers with the Discovery and Orchestration products.

-   **SSH**: For UNIX-like machines, Discovery and Orchestration use SSH protocol, version 2 to access target machines. SSH is a network protocol that allows data to be exchanged using a secure channel between two networked devices. SSH communicates on port 22 within an encrypted datastream and requires a login to access the targets using two available methods of authentication: a user name and password combination and a user name and shared private key. Specify SSH authentication information and type in the **Credentials** module. If multiple credentials are entered, the platform tries one after the other until a successful connection is established or all are ultimately denied. To provide for application relationships a limited number of SUDO commands must be available to be run. Additional details to these requirements can be found in UNIX/Linux [commands requiring root privileges](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) for Discovery and Orchestration.
-   **WMI**: For Windows machines, Discovery uses the Windows Management Instrumentation \(WMI\) interface to query devices. Due to security restrictions for WMI, the MID Server application executing the WMI queries must run as a domain user with local \(target\) administrator privileges. When Discovery detects activity on port 135, it launches a WMI query. The response from the Windows device is sent over a Distributed Component Object Model \(DCOM\) port configured for WMI on Windows machines. This can be any [port](http://support.microsoft.com/kb/832017). Ensure that the MID Server application host machine has access to the targets on all ports due to the unique nature of the WMI requirements.
-   **Windows PowerShell**: [PowerShell](http://support.microsoft.com/kb/968929) is built on the Windows .NET Framework and is designed to control and automate the administration of Windows machines and applications. Orchestration uses PowerShell to run Workflow activities on Windows machines. PowerShell must be installed on any MID Server that executes these activities. MID Servers using PowerShell must be installed on a supported Windows operating system. ServiceNow supports PowerShell 3.0 to 5.1. Orchestration activities for PowerShell require a credentials **Type** of Windows.
-   **SNMP - Network**: For network devices, Discovery uses an SNMP scan to get device specific MIBs and OIDs. SNMP is a common protocol used on most routers, switches, printers, load balancers and various other network enabled devices. Use a community string \(password\) for authentication when scanning a device via SNMP. Many devices have a default community string of **public** which Discovery uses by default when querying a target. Define additional community strings in the [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) form which are tried in succession, along with **public**, until a successful query returns. In addition to the credentials, the platform also requires the ability to make SNMP requests on port 161 from the MID Server to the target. If Access Control Lists \(ACLs\) are in place to control the IP addresses that can make these queries, ensure that the IP address of the MID Server is in the ACL. Discovery supports SNMP versions 1, 2c, and 3.
-   **WBEM:** Web-Based Enterprise Management \(WBEM\) defines a particular implementation of the Common Information Model \(CIM\), including protocols for discovering and accessing each CIM implementation. WBEM requires either of two ports, 5989 or 5988 and uses the HTTP transport protocol. WBEM supports SSL encryption and uses CIM user name/password credentials. Discovery launches a WBEM port probe to detect activity on the target ports and to append gathered data to a classification probe that explores CIM Servers.

**Parent Topic:**[Configuring MID Server](configure-mid-server.md)

**Related topics**  


[Installing the MID Server](mid-server-installation.md)

[Configuring MID Servers](c_MIDServerConfiguration.md)

## Configure MID Server network connectivity

Prepare the network for MID Servers to connect with the instance and access the download site. The network must be prepared before installing or configuring the MID Server. If computers or devices have additional security measures, that security may interfere with MID Servers on those systems.

### Before you begin

Role required: admin

<table id="table_xsh_kvf_wgb"><tbody><tr><td>

![Setup indicator for connection prerequisites
                                            phase](../image/ProgressBarConnect.png)

</td></tr></tbody>
</table>Make sure that the host machine meets the requirements specified in the [MID Server system requirements](../reference/r_MIDServerSystemRequirements.md).

### About this task

The MID Server host computer must have access to the ServiceNow download site at `install.service-now.com` to upgrade automatically. If you have a self-hosted ServiceNow environment that blocks access to the download site, you must import the MID Server installer package into your MID Server hosts manually. For instructions, see [KB0760123](https://support.servicenow.com/kb_view.do?sysparm_article=KB0760123) in the Self-Hosted knowledge base.

Firewalls and proxy configurations may block calls to the OCSP Entrust and DigiCert servers, which prevents the MID Server from working. You may need to change your firewall permissions so that the OCSP traffic goes through. For more information and resolutions, see the HI Knowledge Base article [\[KB1216223\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1216223).

The host machine must have these network privileges:

-   Firewall access: Configure any firewalls between the MID Server and the target devices to allow a connection. If your network uses a DMZ, and if your network security protocols limit port access from within the network to the DMZ, you might have to deploy a MID Server to a machine within the DMZ to probe the devices there.
-   Network access: Configure target devices to allow the MID Server probe to connect. If network security prevents you from configuring new machines that can connect to the targets, install the MID Server on an existing machine with connection privileges.
-   Network account: Install the MID Server with the proper account, either local or domain administrator.

Additionally, for the MID Server to access your ServiceNow instance, satisfy these prerequisites:

-   Network access to the ServiceNow instance: Configure the network that the MID Server uses to allow traffic over TCP port 443.
-   A MID user: Create a ServiceNow user record for the MID Server to use. This user record must have the mid\_server and import\_admin roles.

**Note:** Verify that the baseline public page **InstanceInfo** is active for the MID Server to connect to the instance.

### Procedure

1.  Configure the network to allow MID Server network connectivity to the ServiceNow instance over TCP port 443.

2.  Configure basic authentication for SOAP communications with the ServiceNow instance.

3.  Navigate to **System Web Services** &gt; **Scripted Web Services** &gt; **Scripted SOAP Services**.

4.  Confirm that the following web services are active:

    -   GetMIDInfo
    -   InstanceInfo
    -   MIDAssignedPackages
    -   MIDFieldForFileProvider
    -   MIDFileSyncSnapshot
    -   MIDServerCheck
    -   MIDServerFileProvider
5.  Type **sys\_public.list** in the navigation search field and press **Enter**.

    The Public Pages record list appears.

6.  Verify that the **InstanceInfo** public page is active, to allow the MID Server to validate its version.

7.  Ensure that the MID Server host computer can access the download site at `install.service-now.com`.


### What to do next

After the network is prepared, proceed to [Installing the MID Server](mid-server-installation.md).


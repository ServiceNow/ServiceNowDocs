---
title: Credential-less Discovery with Nmap
description: If the instance fails to identify a configuration item \(CI\) because of authentication failure, Discovery or Service Mapping can run selected Network Mapper \(Nmap\) commands with a MID Server to collect some basic information about the CI without using credentials.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Advanced Discovery configuration, Discovery, ITOM Visibility, IT Operations Management]
---

# Credential-less Discovery with Nmap

If the instance fails to identify a configuration item \(CI\) because of authentication failure, Discovery or Service Mapping can run selected Network Mapper \(Nmap\) commands with a MID Server to collect some basic information about the CI without using credentials.

A MID Server administrator can [install Nmap](https://www.servicenow.com/docs/access?context=install-nmap-on-mid-server&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) on individual MID Servers running on a Windows host. Those MID Servers can then discover some basic information about CIs in your network when normal authentication fails.

**Important:** Self-hosted customers whose network security does not permit downloads from `install.service-now.com` must install and configure Nmap manually on their system. Refer to [Install Nmap on a self-hosted system](https://www.servicenow.com/docs/access?context=install-nmap-on-mid-server&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for instructions.

Credential-less Discovery can create or modify host and application CIs when credentials are missing or misconfigured. If a credential-based Discovery is performed successfully after Nmap creates a CI, the system reconciles the information gathered from each type of discovery.

## What Nmap can discover

The Nmap commands executed during credential-less Discovery can:

-   Perform reverse DNS name resolution to identify the host from the IPv4 address.
-   Return the MAC address of the host if that host is on the same subnet as the host executing the Nmap command.
-   Detect applications installed on a target host.
-   Detect the operating system of a target host and the OS version.

**Note:**

Credential-less Discovery classifies routers and switches as hardware. It does not create or update CIs specifically for them.

Credential-less Discovery should only be used on known subnets where credentials are not viable and should not be used long term.

## Nmap credential-less Discovery scans in cloud computing platforms

It is often against the terms of service to run Nmap scans to or from any resource within a cloud computing service such as Amazon Web Service, Microsoft Azure, IBM Cloud, or Google Cloud Platform. For example, the Amazon Web Service \(AWS\) environment is tightly regulated and requires the permission of AWS through the [AWS Vulnerability/Penetration Testing Request](https://aws.amazon.com/security/penetration-testing/) form. Unauthorized tests against AWS services or AWS-owned resources are prohibited. For this reason, credential-less Discovery within a cloud computing service environment is not appropriate, and if a violation of their policy occurs, could result in expulsion from the service. Please contact your platform service provider for information on limitations or permission requirements for running Nmap.

## Components installed with Nmap

The Discovery - IP Based \[com.snc.discovery.ip\_based\] plugin that provides the Nmap functionality is activated automatically when either Discovery or Service Mapping is active. These Nmap components are provided by the Discovery - IP Based plugin:

<table id="table_m1z_f2w_sbb"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

System property

</td><td>

The **mid.discovery.credentialless.enable** property enables or disables Nmap for all MID Servers on which Nmap is installed that are connected to the instance. This property is installed with the Discovery plugin and is enabled by default. It is configurable by a system administrator.

</td></tr><tr><td>

MID Server properties

</td><td>

These properties, from the MID Server Property \[ecc\_agent\_property\] table, are not intended to be configured:-   **mid.nmap.version**: Version of Nmap that is installed on MID Servers in your environment. This field is visible on the MID Server \[ecc\_agent\] form after Nmap is installed.
-   **nmap.safe.scripts**: Defines the list of Nmap scripts that are classified as safe for use during execution of Nmap’s Application Version Detection phase \(-sV command option\).
-   **nmap.npcap.version**: The version of Npcap that is installed with Nmap. The Nmap installer can only perform upgrades of existing Npcap installations it encounters.

</td></tr><tr><td>

Fields

</td><td>

-   **Credentialless Discovery Port \[cl\_port\]**: Optional field on the Application \[cmdb\_ci\_appl\] table that displays the number of a port scanned by credential-less Discovery. This port number is used to determine whether an application returned by Nmap has a matching CI in the CMDB or if a new CI must be created.
-   **Discovery source \[discovery\_source\]**: Optional field in the Configuration Item \[cmdb\_ci\] table to which the **CredentiallessDiscovery** choice is added. This option shows that credential-less Discovery was used to create a CI.

</td></tr><tr><td>

Nmap MID Server capability

</td><td>

The **Nmap** [MID Server capabilities](https://www.servicenow.com/docs/access?context=t_ConfigureCapabilities&version=xanadu&pubname=xanadu-servicenow-platform&section=r_MIDServerCapabilities&ft:locale=en-US) is added to the MID Server when Nmap is installed and removed automatically when Nmap in uninstalled. Only MID Servers with this capability can perform credential-less Discovery. A system administrator cannot add or remove this capability manually. Self-hosted customers who have the maint role can modify or delete the Nmap capability, but should not do so.Service Mapping doesn’t check for the presence of the **Nmap** capability and selects the MID Server based on the IP address only. To ensure that Service Mapping doesn’t select a MID Server without the **Nmap** capability, install Nmap on all MID Servers assigned to the IP address ranges for which you want credential-less Discovery to be available. If Service Mapping selects a MID Server for credential-less Discovery that doesn’t have Nmap capabilities, this error message appears in the map, at the site of the CI being discovered: `Nmap is not installed on MID Server. Verify all MIDs configured to handle selected IP Address have Nmap Capability. Nmap root directory path does not exist: <path>`

 **Note:** The **ALL** MID Server capability does not include the **Nmap** capability.

</td></tr><tr><td>

Npcap

</td><td>

[Npcap](https://nmap.org/npcap/) is Nmap's packet capture library for Windows. Npcap allows Nmap to perform port scans quickly and to identify the family of the operating system running on the target. Only one copy of Npcap is installed per MID Server host.Because Npcap can be used by other applications, uninstalling Nmap does not automatically uninstall Npcap. You must uninstall Npcap manually, after determining that no other dependencies exist.

</td></tr><tr><td>

Patterns

</td><td>

-   **Credentialless Discovery Network Device**: Scans a host IP address using an Nmap command to identify the host. This pattern launches the **Credentialless Discovery Network Device – PreLaunch** script to retrieve the list of ports to explore from the IP Service \[cmdb\_ip\_service\] table. Do not modify this script.
-   **Credentialless Discovery Application**: Scans a port at an IP address using an Nmap command to identify the application service actively listening on that port. Service Mapping launches this pattern when all credential-based port classification steps fail. Discovery creates a CI in the Application \[cmdb\_ci\_appl\] table if the port is open and it can identify the service by name and product. If the service does not respond to any of the scan attempts, Nmap consults its nmap-services registry and guesses at which service is most likely running on that port. If Nmap has to guess what application is running on a scanned port, the Credentialless Discovery Application pattern does not create an application CI or update an existing CI.

</td></tr><tr><td>

MID Server script includes

</td><td>

-   **SetCredentialLessDeviceClassName**: Determines which host CI to create or update after the successful execution of the Nmap command. Do not modify this script.
-   **CredentialLessApplicationClassNameMapper**: Maps the service product, service name, and extra service information supplied by Nmap for the scanned port to a supported application table in the instance. System administrators can modify this script.
-   **SetCredentialLessApplicationClassName**: Ensures that theCredentialLessApplicationClassNameMapper script is invoked only once. Do not modify this script.

</td></tr><tr><td>

System script include

</td><td>

The CredentiallessDiscoveryAjax script include runs on the instance and handles the installation and uninstallation of Nmap on Windows MID Servers, executed from UI actions on the form. Do not modify this script.

</td></tr></tbody>
</table>-   **[Credential-less host Discovery](../reference/credential-less-host-discovery.md)**  
Credential-less host discovery occurs when a scanned host is found to be alive, but not active, or when all configured credential-based classification probes have failed.
-   **[Credential-less Application Discovery](../reference/credential-less-app-discovery.md)**  
Credential-less Application Discovery attempts to identify an application service actively listening on a specific port at a given IP address.
-   **[Nmap commands and data collected with credential-less Discovery](../reference/data-collected-nmap.md)**  
Nmap executes in phases when collecting data and runs a controlled set of safe commands with two patterns for exploring applications and devices.

**Parent Topic:**[Advanced Discovery configuration](c_DiscoveryExtendedCapabilities.md)


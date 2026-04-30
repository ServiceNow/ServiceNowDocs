---
title: Credential-less host Discovery
description: Credential-less host discovery occurs when a scanned host is found to be alive, but not active, or when all configured credential-based classification probes have failed.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Credential-less Discovery with Nmap, Advanced Discovery configuration, Discovery, ITOM Visibility, IT Operations Management]
---

# Credential-less host Discovery

Credential-less host discovery occurs when a scanned host is found to be alive, but not active, or when all configured credential-based classification probes have failed.

## How the host Discovery pattern is launched

If the Shazzam probe scans a host that is alive but not active, and if credential-based classification probes fail, horizontal Discovery launches the Credentialless Discovery Network Device pattern to gather host information. If the host being scanned does not have a CI defined, Service Mapping launches the HorizontalDiscoveryProbe probe, which in turn launches the Credentialless Discovery Network Device pattern. This pattern attempts to create a new CI if one does not already exist for the scanned host or to update an existing CI in the Hardware \[cmdb\_ci\_hardware\] table.

**Important:** To allow the Credentialless Discovery Network Device pattern to launch, ensure that the **mid.discovery.credentialless.enable** system property is set to **true**. To disable, ensure this property is set to **false**.

<table id="table_lbt_4ng_5bb"><tbody><tr><td>

The system creates these entries in the ECC queue during execution of the HorizontalDiscoveryProbe. ![ECC Queue entries created during execution of the HorizontalDiscoveryProbe](../image/ECCQueueCredential-lessDisco.png "Credential-less Discovery")

</td></tr></tbody>
</table><table id="table_als_h4g_5bb"><tbody><tr><td>

These log messages are published during execution of the HorizontalDiscoveryProbe.![Log messages during execution of the HorizontalDiscoveryProbe](../image/Credential-lessHostIdentifier.png "Credential-less host identifier")

</td></tr></tbody>
</table>## The Nmap command

The Nmap command executed on the MID Server determines if the host is up. Using the IP address and a list of ports passed to Nmap by the pattern, Nmap performs reverse DNS name resolution to identify the host name associated with the IP address. If multiple host names are configured, the first name returned by Nmap is used. If no host name is configured, then the IP address of the remote host is used to create the host CI. The Npcap packet capture library, included with the Nmap installation, identifies the host operating system family. If the scanned host is located on the same subnet as the Windows MID Server host that executes Nmap, the remote host's MAC address is returned.

**Note:** The list of ports that Nmap is configured to scan during credential-less host Discovery is stored in the IP Service \[cmdb\_ip\_service\] table, which is editable. By default, all ports are available for scanning. To block the use of any port for an Nmap scan, set the value in the **Credentialless Discovery \[cl\_discovery\]** column to **false**.

![Configurable list of ports for credential-less Discovery](../image/Credential-lessPortList.png "Credential-less port list")

## Creating or updating host CIs

After successful execution of the Credentialless Discovery Network Device pattern, the SetCredentialLessDeviceClassName MID Server script runs to identify the operating system family of the discovered host. The system class of the host CI is based on the operating system family that is returned by Nmap. If the OS family matches one of the six supported server operating systems, then the system uses a server class derived from the Hardware \[cmdb\_ci\_hardware\] base class, such as Linux Server \[cmdb\_ci\_linux\_server\]. If no match is found, the system uses the base class.

**Note:** When the issue with the credentials is resolved and Discovery runs again, the instance uses the serial number, host name, and system class provided by credential-based discovery to update the host CI that was created by credential-less Discovery.

|OS family|CI table|
|---------|--------|
|AIX|cmdb\_ci\_aix\_server|
|HP-UX|cmdb\_ci\_hpux\_server|
|Linux|cmdb\_ci\_linux\_server|
|Solaris|cmdb\_ci\_solaris\_server|
|OS X or iOS|cmdb\_ci\_osx\_server|
|Windows|cmdb\_ci\_win\_server|
|Undefined|cmdb\_ci\_hardware|

## Hardware identification

The Discovery - IP Based \[com.snc.discovery.ip\_based\] plugin adds an identifier to the Hardware Rule for the Hardware \[cmdb\_ci\_hardware\] base table that matches on the host CI **name** for Nmap scans. The Hardware Rule is used by both credential-based and credential-less Discovery.

![Hardware rule identifier for Credential-less Discovery](../image/Credential-lessHardwareRule.png "Credential-less hardware rule")

**Parent Topic:**[Credential-less Discovery with Nmap](../concept/nmap-credential-less-discovery.md)


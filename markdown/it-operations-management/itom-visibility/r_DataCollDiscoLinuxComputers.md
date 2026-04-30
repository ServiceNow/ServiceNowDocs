---
title: Linux discovery
description: Discovery and Service Mapping applications use probes and patterns to discover and map information about Linux computers and servers. The information is populated in the CMDB. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-31"
reading_time_minutes: 8
keywords: [Patterns, Discovery, Linux]
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Linux discovery

Discovery and Service Mapping applications use probes and patterns to discover and map information about Linux computers and servers. The information is populated in the CMDB. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Supportability details

The Linux server pattern can discover only English-based Linux.

-   **Supported Linux operating systems**

    For IPv4 discovery:

    -   Red Hat
    -   Oracle
    -   Fedora
    -   Debian
    -   SUSE
    -   CentOS
    -   Ubuntu
    For IPv6 discovery:

    -   CentOS 7
    -   Ubuntu 20
    The following operating systems or devices haven’t been verified for IPv6 discovery:

    -   Red Hat cluster
    -   Oracle Clusterware
    -   Linux Pacemaker cluster
    -   Network storage

## Classifier, probes, and pattern

<table id="table_nww_wmf_nbb"><thead><tr><th>

Classifier

</th><th>

Probes

</th><th>

Pattern

</th></tr></thead><tbody><tr><td>

Linux\(Unix classification\)

</td><td>

-   Horizontal discovery probe: Launches patterns
-   Linux - Installed Software^
-   Unix - ADM^
-   Linux - Identity\*
-   Linux - CPU\*
-   Linux - Distribution\*
-   Linux - Find FQDN\*
-   Linux - Memory\*
-   Linux - Memory Modules\*
-   Linux - Network ARP Tables\*
-   Linux - Storage\*
-   Linux - Amazon EC2\*
-   Unix - OS Uptime\*
-   UNIX - OS Filesystems\*
-   UNIX - Find FQDN\*
-   Unix - ADM Enhanced\*

</td><td>

Linux Server

</td></tr></tbody>
</table>\*These probes aren't active on the classifier, as Discovery uses patterns by default for these discoveries.

^These probes remain active by default, even when Discovery uses pattern discovery.

To use patterns, verify that the correct pattern is specified in the horizontal pattern probe on the classifier. See [Add the Horizontal Pattern probe to a classifier](../concept/c-UsingPatternsForHorizontalDiscovery.md#) for instructions.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Requirements for Linux discovery

Before running a discovery, you must verify that all the required configurations are complete.

-   **Verify the plugins installation and activation**
    -   [Plugins or applications installed with ITOM Visibility](../../it-operations-management/reference/plugin-app-itom-visibility.md)
    -   [Install Discovery and Service Mapping Patterns](../../service-mapping/task/install-discovery-service-mapping-patterns.md)
    -   [Install Visibility Content](../../service-mapping/task/install-itom-visibility-global-content.md)
-   **Verify the required credentials configuration**

    Configure the credentials by the required SSH permissions. Discovering sensitive Linux data may require a user with appropriate sudo privileges to run the sudo commands. To configure the required sudo privileges, modify the `/etc/sudoers` file to include the commands that Discovery needs. For `/etc/sudoers` line examples for each command, see [SSH commands requiring a privileged user during probe-based discovery](discovery-ssh-command-require-priv.md).

    For more information about the commands that require a user with elevated rights, refer to the following documents.

    -   [Commands that require root privileges for Discovery, Orchestration, and Integration Hub](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).
    -   For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

    -   [MID Server privileged commands](https://www.servicenow.com/docs/access?context=c_PrivilegedCommandsForMIDServer&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)
    -   [View Patterns commands through the Discovery Patterns module](../task/view-command-pattern-discovery.md)
    -   [Validate commands used in pattern-based discovery](../../it-operations-management/task/validate-discovery-commands.md)
    SSH private key credentials are preferable over SSH password credentials for security reasons.

-   **Verify the MID Server configuration**

    For detailed information, see:

    -   [Test MID Server connectivity](https://www.servicenow.com/docs/access?context=t_ValidateNetworkConnectivity&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)
    -   [MID Server properties](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)
-   **Verify the configuration of the discovery schedule**

    For information on creating a discovery schedule, see [Schedule a horizontal discovery](../task/t_CreateADiscoverySchedule.md#).

    Defining IP ranges ensures that only the specified network adapters and their primary IP addresses are used during Linux discovery. You can configure **Quick Ranges** by entering comma-separated IPv4 address ranges or single IPv6 address.

    Alternatively, you can use the **network\_adapter\_exclusion\_list** property to limit Linux discovery to specific network adapters and their primary IP addresses. For more information, see [Omit network adapter secondary IP addresses in Linux discovery](../../service-mapping/task/omit-adapter-secondary-ip-linux.md).

-   **\(Optional\) Populate Virtual Machine Object field in Hardware \[cmdb\_ci\_hardware\] table**

    Starting with Discovery and Service Mapping Patterns version 1.30.2, you can improve query performance by populating the Virtual Machine Object field in the Hardware \[cmdb\_ci\_hardware\] table. For more information, see [Improved query performance with direct field population in CI tables](../../service-mapping/concept/query-service-account-ldc-fields.md).


## Data collected

The Linux classifier triggers probes that perform the discovery. Several probes are launched during the discovery. See the classifier for a list of the trigger probes.

**Note:** See the knowledge article [KB0687582](https://support.servicenow.com/kb_view.do?sysparm_article=KB0687582) for information on model\_id and manufacturer.

|Label|Table Name|Field Name|Source|
|-----|----------|----------|------|
|Operating System|cmdb\_ci\_linux\_server|os|uname -a|
|OS Version|cmdb\_ci\_computer|os\_version|uname -a or cat /etc/\*release|
|Short description|cmdb\_ci\_linux\_server|short\_description|uname -a|
|Name|cmdb\_ci\_linux\_server|name|DNS, NBT|
|Hostname|cmdb\_ci\_linux\_server|host\_name|DNS, NBT|
|DNS domain|cmdb\_ci\_linux\_server|dns\_domain|DNS|
|Start date|cmdb\_ci\_linux\_server|start\_date|uptime|
|Manufacturer|cmdb\_ci\_computer|manufacturer|dmidecode|
|Serial number|cmdb\_ci\_computer|serial\_number|dmidecode|
|CPU type|cmdb\_ci\_linux\_server|cpu\_type|/proc/cpuinfo|
|CPU speed \(MHz\)|cmdb\_ci\_linux\_server|cpu\_speed|/proc/cpuinfo|
|CPU count|cmdb\_ci\_linux\_server|cpu\_count|/proc/cpuinfo|
|CPU core count|cmdb\_ci\_computer|cpu\_core\_count|/proc/cpuinfo|
|CPU core thread|cmdb\_ci\_computer|cpu\_core\_thread|/proc/cpuinfo|
|CPU manufacturer|cmdb\_ci\_linux\_server|cpu\_manufacturer|/proc/cpuinfo|
|Model number|cmdb\_ci\_computer|model\_number|dmidecode|
|Model ID|cmdb\_ci\_computer|model\_id|dmidecode|
|RAM \(MB\)|cmdb\_ci\_linux\_server|ram|meminfo|
|Disk space \(GB\)\*|cmdb\_ci\_linux\_server|disk\_space|/proc/ide, /proc/scsi, /var/log/dmesg|
|Type|cmdb\_ci\_disk|type|/proc/ide, /proc/scsi, /var/log/dmesg|
|Model ID|cmdb\_ci\_disk|model\_id|/proc/ide, /proc/scsi, /var/log/dmesg|
|Disk space \(GB\)|cmdb\_ci\_disk|disk\_space|/proc/ide, /proc/scsi, /var/log/dmesg|
|Name|cmdb\_ci\_disk|name|/proc/ide, /proc/scsi, /var/log/dmesg|
|Name|cmdb\_ci\_file\_system|name|df|
|Capacity \(MB\)|cmdb\_ci\_file\_system|capacity|df|
|Free Space Bytes \(MB\)|cmdb\_ci\_file\_system|free\_space\_bytes|df|
|Mount point|cmdb\_ci\_file\_system|mount\_point|df|
|Name|cmdb\_running\_process|name|ps|
|Command|cmdb\_running\_process|command|ps|
|Type|cmdb\_running\_process|type|ps|
|PID|cmdb\_running\_process|pid|ps|
|Parameters|cmdb\_running\_process|parameters|ps|
|Name|cmdb\_ci\_network\_adapter|name|ifconfig or ip address show|
|IP address|cmdb\_ci\_network\_adapter|ip\_address|ifconfig or ip address show|
|MAC address|cmdb\_ci\_network\_adapter|mac\_address|ifconfig or ip address show|
|Netmask|cmdb\_ci\_network\_adapter|netmask|ifconfig or ip address show|
|Default gateway|cmdb\_ci\_hardware|default\_gateway|route|

\* The value in the **disk\_space** field is an aggregation of the total capacity \(to include used space\) for all non-removable disks, including both directly attached and SAN storage.

**Note:** Make sure to define unique serial numbers for the RAMs on the Linux server.

Discovery also identifies and classifies information about Linux KVM. Discovery identifies Linux kernel-based virtual machines \(KVM\) when the process classifier detects libvirtd running on a Linux server. The classification triggers the creation of a cmdb\_ci\_kvm record and launches the SSH Command probes to explore the Linux server with virsh, lbvert utility, and virtual machine configuration data.

Discovery creates a \[cmdb\_ci\_kvm\_instance\] record for each virtual machine on the server, and then matches the \[cmdb\_ci\_kvm\_instance\] record to a corresponding \[cmdb\_ci\_computer\] record using the MAC addresses of installed network adapters.

|Table name|Extends|Description|Source|
|----------|-------|-----------|------|
|cmdb\_ci\_kvm|cmdb\_ci\_vm|A hypervisor that manages kernel-based virtual machines \(KVMs\)|Process classifier detects libvirtd running on Linux servers|
|cmdb\_ci\_kvm\_vm\_instance|cmdb\_ci\_vm\_instance|A virtual machine instance on this hypervisor|virsh list-all and dumpxml command|
|cmdb\_ci\_kvm\_object|cmdb\_ci\_vm\_object|An object connected to a virtual machine instance|&lt;network&gt;, &lt;storage pool&gt;, and &lt;storage volume&gt; elements from the dumpxml command|
|cmdb\_kvm\_device|Not applicable|A device connected to a virtual machine instance|&lt;devices&gt; element from the dumpxml command|

|Label|Table name|Field name|Source|
|-----|----------|----------|------|
|Linux Host|cmdb\_ci\_kvm|linux\_host|Reference to the cmdb\_ci\_linux\_server that is running this virtual machine|
|Details|cmdb\_ci\_kvm|details\_xml|dumpxml|
|Object ID|cmdb\_ci\_kvm\_vm\_instance|object\_id|virsh dumpxml|
|State|cmdb\_ci\_kvm\_vm\_instance|state|virsh list-all|
|CPUs|cmdb\_ci\_kvm\_vm\_instance|cpus|virsh dumpxml|
|Memory|cmdb\_ci\_kvm\_vm\_instance|memory|virsh dumpxml|
|Disks|cmdb\_ci\_kvm\_vm\_instance|disks|virsh dumpxml|
|Disks size|cmdb\_ci\_kvm\_vm\_instance|disks\_size|virsh domblkinfo|
|Network adapters|cmdb\_ci\_kvm\_vm\_instance|nics|virsh dumpxml|
|Name|cmdb\_ci\_kvm\_vm\_instance|name|virsh dumpxml|
|Short description|cmdb\_ci\_kvm\_vm\_instance|short\_description|virsh desc|
|Details|cmdb\_ci\_kvm\_object|details\_xml|XML element from dumpxml|
|KVM instance|cmdb\_kvm\_device|kvm\_instance|Reference to cmdb\_ci\_kvm\_instance|
|Device|cmdb\_kvm\_device|device|disk, controller, interface, and so on|
|Type|cmdb\_kvm\_device|type|depends on the device|
|Details|cmdb\_kvm\_device|details\_xml|XML element from dumpxml|

|Relationship|Parent table|Child table|
|------------|------------|-----------|
|Registered On::Has Registered|KVM \[cmdb\_ci\_kvm\]|KVM Virtual Machine instance \[cmdb\_ci\_kvm\_vm\_instance\]|
|Provided By::Provides|KVM \[cmdb\_ci\_kvm\]|Network \[cmdb\_ci\_kvm\_network\]|
|Defines resource for::Gets resources from|KVM \[cmdb\_ci\_kvm\]|Storage Pool \[cmdb\_ci\_kvm\_storage\_pool\]|
|Connected By::Connects|KVM Virtual Machine instance \[cmdb\_ci\_kvm\_vm\_instance\]|Network \[cmdb\_ci\_kvm\_network\]|
|Instantiated By::Instantiates|KVM Virtual Machine instance \[cmdb\_ci\_kvm\_vm\_instance\]|Computer \[cmdb\_ci\_computer\]|
|Virtualized By::Virtualizes|Computer \[cmdb\_ci\_computer\]|KVM \[cmdb\_ci\_kvm\]|
|Provides storage for::Stored on|Storage Pool \[cmdb\_ci\_kvm\_storage\_pool\]|KVM Virtual Machine instance \[cmdb\_ci\_kvm\_vm\_instance\]|

**Related topics**  


[Linux discovery fails with "Cannot connect, status is SSH\_CONNECTION\_FAILURE. Could not agree on signature algorithm Client \(KB1425502\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1425502)

[Linux discovery fails in Unix Classification with the error - Name of unclassified CI is 'servername' \(KB0860486\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0860486)

[Linux discovery error "rbash: PATH: readonly variable Exit status: 1" \(KB0866860\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0866860)


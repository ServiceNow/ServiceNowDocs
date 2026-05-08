---
title: z/OS discovery
description: Discovery and Service Mapping Patterns finds computers running the z/OS operating system using the IBM zOS Server pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# z/OS discovery

Discovery and Service Mapping Patterns finds computers running the z/OS operating system using the IBM zOS Server pattern. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

The IBM zOS Server pattern performs infrastructure-level discovery for z/OS servers. To discover applications on z/OS, use application patterns, such as DB2 on Linux, WMQ On Unix, or Websphere On Unix. For more information, see [IBM z/OS Discovery requirements and expectations \[KB0623031\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0623031) article in the Now Support Knowledge Base.

## Prerequisites

-   **Verify that the UNIX System Services \(USS\) is running on port 22**

    Verify that the USS service is running on port 22 on z/OS.

-   **Verify the required commands on the host machine**

    Verify that you can run the following commands on the host machine:

    -   `uname`
    -   `hostname`
    -   `sysvar SYSNAME`
    -   `netstat`
    -   `df`
    -   `ls`
    -   `cat`
    -   `grep`
    -   `ps`
    -   `cut`
-   **Verify required permissions**

    Verify that you have the following permissions:

    -   Write permission to `/tmp`
    -   Read access to all user processes
    -   Ability to run REXX scripts
-   **Create SSH credentials**

    For more information, see SSH credentials.


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the IBM zOS Server pattern. The pattern discovers USS-mounted file systems.

<table id="table_u33_nv5_qhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Hostname of the z/OS system.

</td></tr><tr><td>

OS Version \[os\_version\]

</td><td>

z/OS operating system version. For example: V2R5 or 3.1.

</td></tr><tr><td>

Operating System \[os\]

</td><td>

Operating system type. The value is set to **IBM\_ZOS**.

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

Hardware manufacturer. The value is set to **IBM**.

</td></tr><tr><td>

Serial number \[serial\_number\]

</td><td>

Hardware chassis serial number.

</td></tr><tr><td>

Model ID \[model\_id\]

</td><td>

Hardware model display name based on model code lookup. For example: z14, z15, or zEnterprise 196.If the model code isn’t in the lookup table, this field remains empty.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

Management IP address used for discovery connection.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|IP Address \[ip\_address\]|IPv4 or IPv6 address.|
|Netmask \[netmask\]|Network mask for the IP address. The value is set to **0.0.0.0**.|
|MAC Address \[mac\_address\]|Hardware MAC address. If unavailable, the value is set to **NOT\_FOUND**.|
|Nic \[nic\]|References the Network Adapter \[cmdb\_ci\_network\_adapter\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Network interface name. If unavailable, the value is set to **VIP**.|
|IP Address \[ip\_address\]|IPv4 or IPv6 address assigned to this network adapter.|
|Netmask \[netmask\]|Network mask for the adapter. The value is set to **0.0.0.0**.|
|MAC Address \[mac\_address\]|Hardware MAC address for the network adapter. If unavailable, the value is set to **NOT\_FOUND**.|
|Configuration Item \[cmdb\_ci\]|References the IBM zOS server \[cmdb\_ci\_ibm\_zos\_server\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the USS file system set to the mount point path. For example: `/`, `/tmp`, or `/u`.|
|Volume ID \[volume\_id\]|Volume identifier, set to the mount point path.|
|Mount point \[mount\_point\]|Directory path where the file system is mounted in the USS hierarchy.|
|File system \[file\_system\]|USS dataset name of the zFS file system. For example: `OMVS.ROOT.ZFS` or `OMVS.TMP.ZFS`.|
|Size bytes \[size\_bytes\]|Total capacity of the file system in kilobytes \(KB\), as retrieved by the `df -Pkv` command.|
|Free space bytes \[free\_space\_bytes\]|Available free space in the file system in KB, as retrieved by the `df -Pkv` command.|
|Computer \[computer\]|References the IBM zOS server \[cmdb\_ci\_ibm\_zos\_server\] table.|

## CI relationships

|CI|Relationship|CI|
|---|------------|---|
|IBM zOS server \[cmdb\_ci\_ibm\_zos\_server\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|IBM zOS server \[cmdb\_ci\_ibm\_zos\_server\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|IBM zOS server \[cmdb\_ci\_ibm\_zos\_server\]|Contains::Contained by|File System \[cmdb\_ci\_file\_system\]|
|IP Address \[cmdb\_ci\_ip\_address\]|References|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|References|IBM zOS server \[cmdb\_ci\_ibm\_zos\_server\]|
|Serial Number \[cmdb\_serial\_number\]|References|IBM zOS server \[cmdb\_ci\_ibm\_zos\_server\]|
|File System \[cmdb\_ci\_file\_system\]|References|IBM zOS server \[cmdb\_ci\_ibm\_zos\_server\]|

**Parent Topic:**[Operating systems discovery](c_Computers.md)

**Related topics**  


[IBM Db2 on Linux database discovery](../../service-mapping/reference/ibm-db2-linux-discovery.md)

[IBM MQ discovery](../reference/r-IBMWebsphereMQ.md)

[IBM WebSphere Application Server discovery using patterns](../../service-mapping/reference/ibm-websphere-server-pattern.md)


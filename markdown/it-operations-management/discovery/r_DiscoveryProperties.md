---
title: Discovery properties
description: Discovery properties allow you to control several aspects of the horizontal discovery process.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 28
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery properties

Discovery properties allow you to control several aspects of the horizontal discovery process.

For information about the Discovery properties that Agent Client Collector uses, see [Using push-based Discovery and horizontal IP-based Discovery together](../../agent-client-collector/concept/using-enhanced-discovery-and-agent-less-discovery-together.md).

Edit the following Discovery properties by navigating to **Discovery Definition** &gt; **Properties**.

**IP properties**

<table id="table_r25_f2l_hhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.discovery.exclude\_ip\_sync\_classes

</td><td>

Defines CI classes whose IP addresses shouldn’t be substituted if the address returned by Discovery doesn’t match one of the devices' NICs. Use a comma-separated list to define multiple classes. By default, the system uses the management IP of a load balancer returned by Discovery in the CI record, rather than substituting it for the IP address of one of the load balancer's NICs.-   Type: string
-   Default value: cmdb\_ci\_lb

</td></tr><tr><td>

glide.discovery.enforce\_unique\_ips

</td><td>

Enforce unique IP addresses: Ignores the IP address after Discovery encounters subsequent devices that use the same IP address. Each time a computer, printer, or network gear with a valid IP address is discovered, any other devices with the same IP address have their IP address field cleared. If inactive, stores the IP address for each device.

 -   Type: true \| false
-   Default value false

</td></tr></tbody>
</table>**Network properties**

<table id="table_cgw_s2l_hhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.discovery.bgp\_router\_disable

</td><td>

BGP router exploration disable: Disables running the SNMP – Routing probe or pattern when discovering a router running the BGP protocol. Normally such exploration IS inactive because of the huge size of BGP routing tables, and because generally such routers are only operating at the edge of large networks where further network discovery would be irrelevant. This value could be set to false if your organization only uses BGP routers as edge routers between relatively small networks \(such as between buildings on a single campus\).

 If you must populate the \[discovery\_device\_neighbors\] table during horizontal layer 2 discovery of the bgp-enabled devices, set the **BGP router exploration disable** property to **No**. Notice that enabling this property can cause performance issues including out-of-memory issues on the MID Server.

 -   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.debug.network\_discovery

</td><td>

Network discovery debugging: Enables extensive logging of all Network Discovery activities on the instance.

 -   Type: true \| false
-   Default value: true
-   Learn More: [Discovery monitoring and issue resolution](../concept/c_DiscoveryTroubleshooting.md)

</td></tr><tr><td>

glide.discovery.discoverable.network.max.netmask.bits

</td><td>

Maximum netmask size for discoverable networks \(bits\): The maximum number of bits in a regular netmask for networks that are discovered by Network Discovery. A regular netmask is a netmask that can be expressed in binary as a string of ones followed by a string of zeroes. For example, 255.255.255.0 is regular and 255.255.255.64 is irregular. Regular networks are commonly expressed like: 10.0.0.0/24, which means a network address of 10.0.0.0 with a netmask of 255.255.255.0. Larger bit numbers mean networks with smaller numbers of addresses in them. For example, the network 10.128.0.128/30 has four addresses in it: one network address \(10.128.0.128\), one broadcast address \(10.128.0.131\), and two usable addresses \(10.128.0.129 and 10.128.0.130\). Small networks are commonly configured in network gear to provide loopback addresses or networks used strictly by point-to-point connections. Since these sorts of networks generally don't need to be discovered by Network Discovery, it would be useful to filter them out. By setting this property to a value of 1 through 32, you can limit the sizes of regular networks that are discovered. Setting it to any other value causes all networks to be discovered. Irregular networks are always discovered. The default value is 28, which means that regular networks with 8 or fewer addresses cannot be discovered.

 -   Type: integer
-   Default value: 28

</td></tr><tr><td>

glide.discovery.network\_owner\_method

</td><td>

Network router selection method: This property controls the method used to decide \(during Network Discovery\) which router should be selected as the router to be associated with a given IP Network. The possible values are:

 -   First Router: The first router that discovers the network is associated
-   Last Router: The last router that discovers the network is associated
-   Most Networks: The router with the most attached networks is associated
-   Least Networks: The router with the least attached networks is associated

 -   Type: choice list
-   Default value: Most Networks
-   Additional options: First Router, Last Router, Least Networks

</td></tr><tr><td>

glide.discovery.physical\_interface\_types

</td><td>

Physical interface types: A comma-separated list of interface types that are considered physical for the purposes of network discovery. If a router \(or device capable of routing\) has an interface of this type, the networks connected to that interface are considered locally connected to that device. The default interface types include Ethernet, 802.11, and Token Ring types. Interface type numbers are defined in the SNMP MIB-2, specifically in OID 1.3.6.1.2.1.2.2.1.3.-   Type: string
-   Default value: 6,117,9,71,209

</td></tr><tr><td>

glide.discovery.switch\_interface\_types

</td><td>

Switch interface types: A comma-separated list of interface types that are considered. Interface type numbers are defined in the SNMP MIB-2, specifically in OID 1.3.6.1.2.1.2.2.1.3. Devices with any interface types that do NOT appear in this list are classified as routers, when they have routing. A complete list of the interface type numbers may be found on the [IANA web site](http://www.iana.org/assignments/smi-numbers), in the section "ifType definitions".-   Type: string
-   Default value: 7,8,9,26,53,62,69,71,78,115,117,209

</td></tr></tbody>
</table>**Other Discovery properties**

<table id="disco-properties"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.use\_external\_credentials

</td><td>

Allows the use of external storage of credentials.-   Type: true \| false
-   Default value: true

</td></tr><tr><td id="increase-scale-factor-max">

com.glide.processing.framework.max\_thread\_utilization\_percentage

</td><td>

Enables you to modify the scale factor for the **discovery.sensor** and **discovery.cloud.sensor** queues. Increasing the value allows you to increases the scale factor, which subsequently increases the number of worker threads per app node.-   Type: integer
-   Default value: 30
-   Max value: 75

**Note:** This behavior only applies when **discovery.use.event.processing** is set to **true**.

</td></tr><tr><td>

com.glide.queue.discovery.cloud.sensors.processing\_jobs.priority

</td><td>

Manages the background job's worker priority for Cloud-based Discovery jobs when using Event Framework. Increasing the value decreases the priority. -   Type: integer
-   Default value: 100

**Note:** This behavior only applies when **discovery.use.event.processing** is set to **true**.

</td></tr><tr><td>

com.glide.queue.discovery.sensors.processing\_jobs.priority

</td><td>

Manages the background job's worker priority for IP-based Discovery jobs when using Event Framework. Increasing the value decreases the priority. -   Type: integer
-   Default value: 100

**Note:** This behavior only applies when **discovery.use.event.processing** is set to **true**.

</td></tr><tr><td>

discovery.event.pin.jobs

</td><td>

Enables event processors to execute on specific nodes. When set to **true**, jobs are assigned to nodes to distribute the work evenly. If set to **false**, jobs are randomly assigned, which may increase discovery throughput.-   Type: true \| false
-   Default value: false

**Note:** This behavior only applies when **discovery.use.event.processing** is set to **true**.

</td></tr><tr><td>

discovery.event.separate.cloud.events

</td><td>

Reduces processing time by separating the **discovery.sensor** and **discovery.cloud.sensor** event queues for cloud and IP-based discoveries. When this property is set to **false**, event processing will only use the **discovery.sensor** queue.-   Type: true \| false
-   Default value: true

**Note:** This behavior only applies when **discovery.use.event.processing** is set to **true**.

</td></tr><tr><td>

discovery.use.event.processing

</td><td>

Enables Discovery to use the Event Framework when processing jobs.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

glide.discovery.active\_processes\_filter

</td><td>

Active Processes Filter: Optimization for application dependency mapping. Filters the active processes returned by Discovery to only those that have a match in the Process Classification table.

 -   Type: true \| false
-   Default value: false

</td></tr><tr><td>

glide.discovery.adme.aggregation\_interval

</td><td>

ADME - Aggregation interval \(sec\): How often to aggregate instantaneous data into chunks in seconds. It must be a minimum of 60 seconds and it must be a multiple of ADME Sampling interval.-   Type: integer
-   Default value: 3600

</td></tr><tr><td>

glide.discovery.adme.base\_dir\_unix

</td><td>

ADME - Unix Base Dir: An existing directory on the target UNIX machines to be used as a workspace. Must be an absolute path to the directory.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

mid.powershell.target\_base\_dir

</td><td>

Powershell - Target Base Dir: A network share on the target Windows machines to be used as a workspace.-   Type: string
-   Default value: admin$\\temp

</td></tr><tr><td>

glide.discovery.adme.max\_total\_samples

</td><td>

ADME - Max total samples: The limit of samples being taken by the script. The script will stop running after this number of samples are taken.-   Type: integer
-   Default value: 100

</td></tr><tr><td>

glide.discovery.adme.rolling\_window\_size

</td><td>

ADME - Rolling window size: How many recently aggregated chunks to keep. An aggregated chunk consists of ADME Aggregation interval divided by ADME Sampling interval samples. Only the newest chunks are kept.-   Type: integer
-   Default value: 24

</td></tr><tr><td>

glide.discovery.adme.sampling\_interval

</td><td>

ADME - Sampling interval \(sec\): How often to sample process and connection data in seconds. Must be a minimum of 5 seconds.-   Type: integer
-   Default value: 120

</td></tr><tr><td>

glide.discovery.adm.update.applications

</td><td>

Controls if application CIs should be updated based on running process status.

 When Discovery rediscovers the server and notices that a previously running process is no longer active on cmdb\_running\_process record, Absent is set to **true**. In addition, on related application CI, install\_status is updated from installed to absent. On subsequent scans, if the running process is back online on the related application CI, install\_status is reverted to installed.

**Note:** This behavior will only work for application CIs that are discovered using patterns.

 -   Type: true \| false
-   Default value: true \(for zbooted or new activations\)

</td></tr><tr><td>

glide.discovery.allow\_loopback\_adapters

</td><td>

Loopback adapter filter: Allows network loopback adapters on SNMP devices to be discovered instead of being filtered out during Discovery. When this property is set to **true**, network loopback addresses are discovered and added to the CMDB.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

glide.discovery.application\_mapping

</td><td>

Application mapping: Enables the application mapping portion of Discovery

 **Important:** Disabling this property disables the creation of relationships between applications but doesn’t disable the ADM probes and sensors, nor does it prevent process classification.

 -   Type: true \| false
-   Default value: true
-   Learn More: [Application Dependency Mapping \(ADM\) for Discovery](r_ApplicationDependencyMapping.md#)

</td></tr><tr><td>

glide.discovery.certs.cert\_admin\_user\_id

</td><td>

Certificate Inventory and Management: Holds the user ID of the user who will be referenced in the certificate task and incident, created via Scheduled Job.

 -   Type: string \(40 characters maximum\)
-   Default value: Certificate Administrator

</td></tr><tr><td>

glide.discovery.certs.days\_before\_expiration\_to\_create\_renewal\_task

</td><td>

Certificate Inventory and Management: Number of days before certificate expiration that a renewal task should be created.

 -   Type: integer
-   Default value: 60

</td></tr><tr><td>

glide.discovery.certs.enable\_incident\_creation\_for\_expired\_certificates

</td><td>

Certificate Inventory and Management: Enables the Scheduled Job to create the incidents for expired certificates, for example, certificates whose validity is past current system date or time. By default, this property is enabled.

 -   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.certs.enable\_renewal\_task\_creation\_for\_discovered\_certificates

</td><td>

Certificate Inventory and Management: Enables renewal task creation for all discovered certificates. By default, this property is enabled.

 -   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.certs.slack\_channel\_id

</td><td>

Certificate Inventory and Management: Indicates the Slack channel ID where certificate notifications are sent.

 -   Type: string
-   Default value: empty

</td></tr><tr><td>

glide.discovery.count.use\_optimized\_counter

</td><td>

Executes optimized code for updating discovery\_status.started and discovery\_status.completed counts. If set to **true**, business rules on discovery\_status won't execute when "started" or "completed" is changed. There are two exceptions:

1.  When a request to increment starting counts gets triggered and discovery\_status.state value is still in 'Starting'.
2.  When discovery\_status.completed changes to the same value as discovery\_status.started.

-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.debug.ci\_identification

</td><td>

CI identification debugging: If set to **true**, enables debug logging \(into the CI Identification Log\) for CI Identification.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

glide.discovery.discover\_aws\_ec2\_host\_metadata

</td><td>

When doing IP-based discovery against a given host, also run probes that retrieve AWS EC2 metadata.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.discover\_azure\_host\_metadata

</td><td>

When doing IP-based discovery against a given host, also run probes that retrieve Azure metadata.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.discover\_software

</td><td>

Discover software packages: Enable the discovery of software packages.-   Type: true \| false
-   Default value: true
-   Learn More: [General software package discovery](r_DataCollDiscoGenSWPkg.md)

</td></tr><tr id="acc-discovery-property1"><td>

glide.discovery.domain.name.nbt

</td><td>

Set OS domain name by NBT or WMI. If set to **true**, Windows domain name is set by NBT. Otherwise it’s set by WMI.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.enable\_adme

</td><td>

ADME: Enable enhanced ADM probe. If set to **true**, the ADM Enhanced probe is triggered and only fall back to the ADM probe as needed.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

glide.discovery.enable\_file\_tracking

</td><td>

Enable configuration file tracking as part of the Pattern based Horizontal Discovery. If set to **true**, the system enables you to specify paths of configuration files for applications that are discovered by patterns. You can track and compare tracked configuration files.

 -   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.enable\_mac\_address\_verification

</td><td>

Enables MAC address verification to determine if a device has changed its IP address during a discovery. If set to **true**, Discovery passes the MAC address of a device being discovered to the MID Server so that probes can determine if the IP address has changed while Discovery is running. If the device has changed IP addresses, then Discovery stops processing that IP address and updates the Discovery log with a warning message. Discovery doesn’t stop processing other IP addresses.

 -   Type: true \| false
-   Default value: false

 Open the System Properties \[sys\_properties\] table to find this property.

</td></tr><tr><td>

glide.discovery.enable.software\_filter

</td><td>

Windows software filter: Enable Windows software filtering for Discovery.

 -   Type: true \| false
-   Default value: true

</td></tr><tr id="acc-discovery-property2"><td>

glide.discovery.enable.software\_simplify

</td><td>

Enables cleanup for software’s name and version. If set to **true**, it removes any appended version or commonly found phrases from the name and removes leading 0s in the version. If set to **false**, raw data is persisted in the table. Use with the **glide.discovery.enable.software\_simplify\_sccm** property to avoid software data discrepancy between Discovery and SCCM.-   Type: true \| false
-   Default value: true

 **Note:** Once the property is set to **false**, to disable the cleanup, duplicate records are generated for a given software. Name and Version are the primary identifiers.

</td></tr><tr><td>

glide.discovery.enable.software\_simplify\_sccm

</td><td>

Enables cleanup for SCCM software. If set to **true**, Discovery changes the Name of the software to be the same as SCCM. If set to **false**, Discovery doesn’t clean up the Name. Use with the **glide.discovery.enable.software\_simplify** property to avoid software data discrepancy between Discovery and SCCM.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

glide.discovery.file\_tracking.max\_file\_size

</td><td>

File Tracking: The maximum file size for tracked configuration file content. -   Type: integer
-   Default value: 500000

</td></tr><tr><td>

glide.discovery.file\_tracking.max\_files\_per\_ci

</td><td>

File Tracking: The maximum number of tracked configuration files per CI.-   Type: integer
-   Default value: 50

</td></tr><tr><td>

glide.discovery.file\_tracking.change\_limit\_count

</td><td>

File Tracking: Number of changes allowed on a tracked configuration file in the defined time window.-   Type: integer
-   Default value: 4

</td></tr><tr><td>

glide.discovery.file\_tracking.change\_limit\_days

</td><td>

File Tracking: Time window \(in days\) that limits the number of changes on a tracked configuration file.-   Type: integer
-   Default value: 7

</td></tr><tr><td>

glide.discovery.fqdn.regex

</td><td>

DNS Host Name And Domain Name Regex: The default parsing of FQDN \(Fully Qualified Domain Name\) is to pick the first name separated by dots as the host name and the rest of the names as the domain name. For example, "machine1.testlab.service-now.com" has host name of "machine1" and domain name of "testlab.service-now.com". The property allows regex with two capturing groups with the first group representing the host name and the second group the domain name.-   Type: string
-   Default value: ^\(\[^.\]+\)\\.\(\(?:\[^.\]+\\.\)+\[^.\]+\)$

</td></tr><tr><td>

glide.discovery.hostname.always\_update

</td><td>

Always update host name. If set to **true**, discovery always updates the host name with the most recently discovered value contingent upon the source being trusted. Note that this may result in hand-entered values being overwritten. This property is only applicable for Probe-based Discovery.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.hostname.case

</td><td>

Host name case. If **Lower case** is selected, always translate the host name into lower case. If **Upper case** is selected, always translate the host name to upper case. If **No change** is selected, leave the host name intact. This primarily affects host names discovered with NETBIOS, though some non-standard DNS systems may also return some or all of the name in upper case.-   Type: choice list
-   Default value: Lower case
-   Additional options: Upper case, No change

</td></tr><tr><td>

glide.discovery.hostname.dns\_nbt\_trusted

</td><td>

DNS or NetBIOS is trusted host name source: If set to **true**, trust the device name discovered via DNS or NetBIOS. If checked, CI's host name found via DNS or NBT is used.**Note:** For Linux, AIX, and Solaris patterns, do not use the DNS name as the host name.

-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.hostname.include\_domain

</td><td>

Includes domain name in host name: If set to **true**, include the domain name as part of the host name. For example, "bosco.service-now.com" instead of "bosco".**Note:** For AIX and Solaris patterns, do not use the DNS name as the host name.

-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

glide.discovery.hostname.snmp\_trusted

</td><td>

SNMP is trusted host name source: If set to **true**, trust the device name discovered via SNMP. If checked, any device name found via SNMP is used instead of the name found by a reverse DNS lookup. -   Type: true \| false
-   Default value: false \(For new Discovery customers starting in Yokohama, default value is true.\)

</td></tr><tr><td>

glide.discovery.hostname.ssh\_trusted

</td><td>

SSH is trusted host name source: If set to **true**, trust the device name discovered via SSH. If checked, any device name found via SSH is used instead of the name found by a reverse DNS lookup.**Note:** For Linux, AIX, and Solaris patterns, do not use the DNS name as the host name.

-   Type: true \| false
-   Default value: false \(For new Discovery customers starting in Yokohama, default value is true.\)

</td></tr><tr><td>

glide.discovery.hostname.wmi\_trusted

</td><td>

WMI is trusted host name source: If set to **true**, trust the device name discovered via WMI. If checked, any device name found via WMI is used instead of the name found by a reverse DNS lookup.-   Type: true \| false
-   Default value: false \(For new Discovery customers starting in Yokohama, default value is true.\)

</td></tr><tr><td>

glide.discovery.ip\_based.active

</td><td>

This allows scans on all IP Address of the same device in the same Discovery schedule to go through full cycle. This is set to **true** for probe-to-pattern migrated instances, Discovery doesn’t attempt extra IP Address detection.-   Type: true \| false
-   Default value: true \(For probe-to-pattern migrated instances.\)

</td></tr><tr><td>

glide.discovery.ip\_service\_affinity

</td><td>

IP service affinity: If set to **true**, IP service affinity is enabled. IP service affinity allows Discovery to remember the last port of the IP address that was discovered.

 **Note:** You must enable ip\_service\_affinity records if you’re using multiple SSH ports.

 -   Type: true \| false
-   Default value: false \(For new Discovery customers starting in Yokohama, default value is true.\)
-   Learn More: [Check IP service affinity for Discovery and Orchestration](../../credentials/task/t_CheckIPServiceAffinity.md)

</td></tr><tr><td>

glide.discovery.L3\_mapping

</td><td>

Map servers and network devices to routers and layer-3 switches If the "L3 mapping" property is enabled, it maps servers and network gears to its associated routers and layer-3 switches.-   Type: true \| false
-   Default value: true
-   Learn More: [Network discovery](../concept/c_NetworkDiscovery.md#)

</td></tr><tr><td>

glide.discovery.log\_message\_length

</td><td>

Limits the maximum message length that is displayed in Discovery Log table. A value of 0 or any negative number disables this limit.

 -   Type: integer
-   Default value: 200
-   Learn More: [Logs for horizontal discovery](r_DiscoveryLog.md#)

</td></tr><tr><td>

glide.discovery.mark\_esx\_servers\_as\_absent

</td><td>

If this property is set to true, the ESX Servers are marked as absent instead of retired if the ESX server isn’t found in the payload.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

glide.discovery.max\_concurrent\_invocations\_per\_schedule

</td><td>

Maximum concurrent invocations per schedule: Prevents an unbounded number of invocations from inundating the system when a schedule takes longer than the time between invocations. The value is an integer defining the maximum number of automated invocations of the same schedule that may proceed at one time. If the limit has been reached subsequent scheduled invocations are canceled. The default value is 3. A value of 0 or any negative number disables this restriction. -   Type: integer
-   Default value: 3

**Note:** This property does not apply to schedules that have a 'Run after' configuration set to 'Even if canceled'.

</td></tr><tr><td>

glide.discovery.network\_discovery.functionality

</td><td>

Networks discovery functionality: The Functionality used to discover networks. Usually this should be **SNMP only**.-   Type: string
-   Default value: SNMP only

</td></tr><tr><td>

glide.discovery.perf.metrics.enable\_collection

</td><td>

Whether to collect Discovery performance metrics.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.perf.metrics.rollup\_by\_build

</td><td>

Whether to aggregate individual Discovery performance metrics into a roll-up table that groups by discovery build.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.perf.metrics.rollup\_by\_status

</td><td>

Whether to aggregate individual Discovery performance metrics into a roll-up table that groups by discovery status.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.perf.metrics.rollup\_by\_target

</td><td>

Whether to aggregate individual Discovery performance metrics into a roll-up table that groups by target IP address.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.populate\_software\_instance\_table

</td><td>

If set to **true**, Discovery populates these tables for software discovery: `cmdb_software_instance` and `cmdb_sam_sw_install`

-   Type: true \| false
-   Default value: false

 Use this property only if you were using Software Asset Management with Discovery in pre-Jakarta releases and want to keep populating the `cmdb_software_instance` table.

 Open the System Properties \[sys\_properties\] table to find this property.

</td></tr><tr><td>

glide.discovery.roundingInterval.cpu

</td><td>

CPU speed rounding: Enter the number to round the CPU speed to. The units are in MHz.-   Type: integer
-   Default value: 1

</td></tr><tr><td>

glide.discovery.roundingInterval.ram

</td><td>

Memory rounding: Enter the number to round the computer RAM to. The units are in MB.-   Type: integer
-   Default value: 1

</td></tr><tr><td>

 

</td><td>

 

</td></tr><tr><td>

glide.discovery.save\_pattern\_log

</td><td>

Controls whether pattern logs are saved during discovery execution. This property helps enhance performance by reducing database interactions.-   Type: string
-   Default value: true

If set to **false**, the system saves the pattern log only when it is important to display information \(for example, when a failure occurs\). This further improves performance by minimizing unnecessary saves.

**Note:** Regardless of the property value, pattern logs are always saved if the pattern status is failure.

</td></tr><tr><td>

glide.discovery.schedule.autogenerate.debug

</td><td>

Enables detailed logging for troubleshooting. If set to **true**, the job’s detailed logging output will appear in the System Log \[sys\_log\] table with the source DiscoveryIPAMIntegration.-   Type: true \| false
-   Default value: false
-   Learn more: [IPAM Discovery integration](../concept/ipv6-ipam-disco-integration.md)

</td></tr><tr><td>

glide.discovery.schedule.autogenerate.group

</td><td>

Groups auto-generated IPAM Discovery schedules by a specific tag or attribute. For example, entering "location" as the value would group the schedules by their associated locations.-   Type: string
-   Default value: empty
-   Learn more: [IPAM Discovery integration](../concept/ipv6-ipam-disco-integration.md)

</td></tr><tr><td>

glide.discovery.schedule\_ipv4\_limit

</td><td>

Defines the maximum number of IPv4 addresses that can be included in a single auto-generated IPv4 Discovery schedule.-   Type: integer
-   Default value: 65,536
-   Learn more: [IPAM Discovery integration](../concept/ipv6-ipam-disco-integration.md)

</td></tr><tr><td>

glide.discovery.schedule\_ipv6\_limit

</td><td>

Defines the maximum number of IP6 addresses that can be included in a single auto-generated IPv6 Discovery schedule.-   Type: integer
-   Default value: 20000
-   Learn more: [IPAM Discovery integration](../concept/ipv6-ipam-disco-integration.md)

**Note:** On instances below ZP3 and YP9, the maximum number of IPv6 addresses per schedule must not exceed 5,000, which is also the default value in Yokohama and earlier releases.

</td></tr><tr><td>

glide.discovery.schedule\_monitoring.dry\_run

</td><td>

Determines whether the job will run in "dry run" mode. If set to **true**, the job will only log the decision in the Discovery Log but won't change the status's state, otherwise the job will change the state of the status if needed.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

glide.discovery.schedule\_monitoring.schedule\_types\_to\_monitor

</td><td>

Determines the type of statuses to track. The value can be found on the "Discover" attribute on the schedule.-   Type: string
-   Default value: CIs

</td></tr><tr><td>

glide.discovery.schedule\_monitoring.stale\_check\_seconds

</td><td>

Determines the number in seconds in which a status is considered stale. A stale status is a status that was not updated for the last X seconds.-   Type: integer
-   Default value: 1200 \(20mins\). If nothing is configured, the default is 2x the interval of the job.

</td></tr><tr><td>

glide.discovery.sensors.fire\_ssh\_probe

</td><td>

In case the VIPs \(Load Balancer Virtual Services\) didn’t return as part of the SNMP Probe payload, fire the SSH Probe. Select this option to use the SSH port on the load balancer, rather than just using SNMP.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.sensors.netapp\_native\_7mode

</td><td>

For 7-Mode NetApp storage servers, use native discovery instead of SMI-S.

</td></tr><tr><td>

glide.discovery.sensors.netapp\_native\_cluster\_mode

</td><td>

For Cluster Mode NetApp storage servers, use native discovery instead of SMI-S.

</td></tr><tr><td>

glide.discovery.sensors.save\_attachments

</td><td>

Save ECC queue attachments: The normal behavior for discovery sensors is to delete attachments to ECC queue entries upon successful sensor processing. Setting this property to true overrides this behavior, and forces attachments to be preserved. This would normally only be useful for debugging purposes.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.shazzam\_ranges\_json

</td><td>

Use JSON for IP ranges in Shazzam: If set to **true**, discovery encodes Shazzam's IP ranges as JSON, dramatically reducing the payload size.-   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.software\_filter\_keys

</td><td>

Windows software filters: If Windows software filtering is enabled, when the name of a discovered software contains any of the comma-separated values, it’s filtered out.-   Type: string
-   Default value: Language Pack, Hotfix Security Update

</td></tr><tr><td>

glide.discovery.software\_sccm\_managed

</td><td>

Windows software is SCCM managed: If set to **true**, Discovery won’t populate software for computer CIs also managed by SCCM.

 -   Type: true \| false
-   Default value: false
-   Learn More: [Discovery and SCCM together](../concept/c_DiscoveryAndSCCMTogether.md#)

</td></tr><tr><td>

glide.discovery.use\_cmdb\_identifiers

</td><td>

CMDB Identifiers: If set to **true**, identification and reconciliation will be handled by the CMDB API instead of through the old Discovery implementation.

 -   Type: true \| false
-   Default value: true

</td></tr><tr><td>

glide.discovery.use\_probe\_results\_cache

</td><td>

Use probe results cache: If set to **true**, the cache is checked to see if the results of the probe must be processed by a sensor. It only needs to be processed if the results have changed from the last discovery run.-   Type: true \| false
-   Default value: false
-   Learn More: [Create or modify a probe](../task/modify-a-probe.md)

**Note:** In previous releases, this property was **true** by default. The value in this property isn’t changed during an upgrade to Kingston.

</td></tr><tr><td>

glide.discovery.virtual\_interface\_types

</td><td>

Virtual interface types: List of interface types \(comma-separated\) that can be considered "virtual" for the purposes of network discovery. In other words, if a router \(or device capable of routing\) has an interface of this type, the networks connected to that interface are considered virtually connected to that device. The default interface types include the propVirtual type. Interface type numbers are defined in the SNMP MIB-2, specifically in OID 1.3.6.1.2.1.2.2.1.3.-   Type: integer
-   Default value: 53

</td></tr><tr><td>

glide.discovery.warn\_minor\_version

</td><td>

Warn on Minor Version Mismatch: If set to **true**, warnings are logged when minor\_version mismatches are detected during Discovery sensor processing.

 -   Type: true \| false
-   Default value: false

</td></tr><tr><td>

glide.ecc\_agent.validated.override

</td><td>

An override for the ecc\_agent validated field: If set to true, ecc\_agent records will always be treated as valid.-   Type: true \| false
-   Default value: false

 Navigate to **System Properties** &gt; **All Properties** to find this property.

</td></tr><tr><td>

glide.eccprobe.awsrestprobe.max\_retries

</td><td>

Set the maximum number of times the AWS request will be retried if a rate limit exceeded error occurs. Maximum value is 10. Note that retries use exponential backoff \(2^x\). Setting negative values is equivalent to setting the maximum value.-   Type: integer
-   Default value: 4

</td></tr><tr><td>

glide.eccprobe.awsrestprobe.max\_wait

</td><td>

Set the maximum total amount of time \(seconds\) the AWS request attempts to retry. Maximum value: 2046 seconds. Setting negative values is equivalent to setting the maximum value.-   Type: integer
-   Default value: 30

</td></tr><tr><td>

glide.eccprobe.max\_queued\_probes\_per\_run

</td><td>

Set the maximum number of probes a node can pick up during a run.-   Type: integer
-   Default value: 20

</td></tr><tr><td>

glide.eccprobe.node\_agent\_id

</td><td>

ECC queue entries with "mid.server.$\{VALUE\}" will be picked up and processed by the nodes. This must be unique and not the same as any MID server name.-   Type: string
-   Default value: NODE\_AGENT

</td></tr><tr><td>

sn\_disco\_firewall.default.rule.task.policy.owner.group

</td><td>

Firewall Audits and Reporting: Indicates the name of the assignment group that owns or is assigned to firewall rule tasks

-   Type: string \(40 characters maximum\)
-   Default value: Task Owner Group Name

</td></tr><tr><td>

sn\_disco\_firewall.default.rule.task.approval.group

</td><td>

Firewall Audits and Reporting: Indicates the name of the approval group that is used to approve the firewall rule tasks.

 -   Type: string \(40 characters maximum\)
-   Default value: Approval Group Name

</td></tr><tr><td>

sn\_disco\_certmgmt.enable\_csr\_generation

</td><td>

Enables automatic CSR generation on the Certificate Inventory and Management **Request New Certificate** and **Request New Ceriticate \(Automated\)** forms. This feature is disabled by default for security.-   Type: true \| false
-   Default value: false

</td></tr><tr><td>

sn\_disco\_certmgmt.private\_key\_size

</td><td>

Changes the private key size when using automatic CSR generation on the Certificate Inventory and Management **Request New Certificate** and **Request New Ceriticate \(Automated\)** forms. This property accepts values: 512 \| 1024 \| 2048 \| 4096.-   Type: integer
-   Default value: 2048

</td></tr><tr><td>

sn\_disco\_workspace.discovery\_schedule\_anomaly\_detection\_disabled

</td><td>

Discovery Admin Workspace: Disables the anomaly detection feature. When set to **true**, the system doesn't detect anomalies in Discovery schedules.-   Type: true \| false
-   Default value: false

**Warning:** Turning off this feature significantly impacts the Discovery experience across multiple pages, charts, and tables.

</td></tr><tr><td>

sn\_disco\_workspace.discovery\_schedule\_anomaly\_detection\_method

</td><td>

Discovery Admin Workspace: Determines the approach used for anomaly detection in Discovery schedules. The machine learning \(ML\)-based approach uses historical scan data and AI algorithms to detect anomalies and outliers. The Stats-based approach uses historical scan data and statistical standard deviation metrics to detect anomalies and outliers.-   Type: choice list
-   Default value: ML-based

</td></tr><tr><td>

sn\_disco\_workspace.discovery\_schedule\_anomaly\_discover\_type

</td><td>

Discovery Admin Workspace: Determines the type of Discovery schedules for which anomaly detection is enabled, IP-based \(CIs\) and/or Cloud Discovery \(Cloud Resources\). To disable anomaly detection for a specific type of discovery, exclude it from the value. For example, remove "Cloud Resources" from the string if you only want to detect anomalies for IP-based Discovery schedules.-   Type: string
-   Default value: CIs, Cloud Resources

</td></tr><tr><td>

sn\_disco\_workspace.discovery\_schedule\_anomaly\_ml\_model\_sensitivity

</td><td>

Discovery Admin Workspace: Adjusts the sensitivity for ML-based Discovery schedule anomaly detection. Changing the sensitivity can impact detection accuracy. Lower sensitivity results in more anomalies reported, which could increase false positives. Higher sensitivity results in fewer anomalies reported, which could increase false negatives.-   Type: choice list
-   Default value: low

</td></tr><tr><td>

sn\_disco\_workspace.discovery\_schedule\_cis\_discovered\_anomaly\_threshold

</td><td>

Discovery Admin Workspace: Sets the threshold percentage for detecting anomalies in the number of configuration items \(CIs\) discovered during a Discovery schedule execution. A Discovery status is marked as anomalous if the CI count decreases from the average by more than this threshold.-   Type: integer
-   Default value: 20

</td></tr><tr><td>

sn\_disco\_workspace.discovery\_schedule\_error\_anomaly\_threshold

</td><td>

Discovery Admin Workspace: Sets the threshold percentage for detecting anomalies in Discovery schedule error counts. A Discovery status is marked as anomalous if the total error count deviates from the average error count by more than this threshold.-   Type: integer
-   Default value: 20

</td></tr><tr><td>

sn\_disco\_workspace.discovery\_schedule\_runtime\_anomaly\_threshold

</td><td>

Discovery Admin Workspace: Sets the threshold percentage for detecting anomalies in Discovery schedule execution time. A Discovery status is marked anomalous if the run time deviates from the average run time of the schedule by more than this threshold.-   Type: integer
-   Default value: 20

</td></tr><tr><td>

sn\_disco\_workspace.discovery\_stats\_time\_scale

</td><td>

Discovery Admin Workspace: Allows you to see the health of your Discovery schedules over your preferred time span. Options include: 7, 14, and 30 days. Selecting a different value updates indicators and charts to measure over this time period.

 -   Type: choice list
-   Default value: 7

</td></tr><tr><td>

sn\_disco\_workspace.visibility\_diagnostic\_utility.enabled

</td><td>

Discovery Admin Workspace: Enables a Virtual Agent to retrieve diagnostic information for troubleshooting issues with Discovery. Setting this property to **true** displays a Virtual Agent on the **Diagnostics** page.-   Type: true \| false
-   Default value: false

</td></tr></tbody>
</table>**Parent Topic:**[Configuring Discovery](../concept/c_DiscoveryConfiguration.md)


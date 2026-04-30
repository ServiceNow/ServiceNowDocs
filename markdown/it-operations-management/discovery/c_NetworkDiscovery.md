---
title: Network discovery
description: Network Discovery discovers the internal IP networks and subnets within your organization.Configure network Discovery from a Discovery schedule.After you conduct a network Discovery, you must convert the IP networks that were found into range sets for use in discovering other devices.After creating discovery range sets from a network discovery, add the sets to a discovery schedule. This process narrows down the range of IP addresses that Shazzam probes can scan. You can also add a behavior.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-10-20"
reading_time_minutes: 8
breadcrumb: [Running discoveries in your network, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Network discovery

Network Discovery discovers the internal IP networks and subnets within your organization.

**Note:** If you already know the IP address ranges in your network, it's not necessary to run Network Discovery. It is intended for organizations that don't have complete knowledge of the IP addresses available for Discovery in their networks.

## How network discovery works

Discovery uses the information it gathers to update routers and Layer 3 switches in the Configuration Management Database \(CMDB\). A single MID Server begins its scan on a configurable list of starting \(or seed\) routers performs network Discovery. The starting routers are the default routers used by all the MID Server host machines in the network, but can be any designated routers. The MID Server uses the router tables on the starting routers to discover other routers in the network. The MID Server then spreads out through the network, using router tables it finds to discover other routers. It continues until the MID Server explored all the routers and switches.

After running Network Discovery, convert the IP networks it finds into IP address Range Sets that you use in Discovery schedules to discover configuration items \(CI\). Configure [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US). Port 161 must be open for SNMP access.

## Network Discovery properties

The default values are correct for most discoveries. Navigate to **Discovery Definitions** &gt; **Properties** to edit the properties.

<table id="table_jvq_fqq_hhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.discovery.bgp\_router\_disable

</td><td>

BGP router exploration disable: Disables running the SNMP – Routing probe or pattern when discovering a router running the BGP protocol. Normally such exploration IS inactive because of the huge size of BGP routing tables, and because generally such routers are only operating at the edge of large networks where further network discovery would be irrelevant. This value could be set to false if your organization only uses BGP routers as edge routers between relatively small networks \(such as between buildings on a single campus\).

 If you must populate the \[discovery\_device\_neighbors\] table during horizontal layer 2 discovery of the bgp-enabled devices, set the **BGP router exploration disable** property to **No**. Notice that enabling this property can cause performance issues including out-of-memory issues on the MID Server.

 -   Type: true \| false
-   Default value true

</td></tr><tr><td>

glide.discovery.debug.network\_discovery

</td><td>

Network discovery debugging: Enables extensive logging of all Network Discovery activities on the instance.

 -   Type: true \| false
-   Default value true
-   Learn More: [Discovery monitoring and issue resolution](c_DiscoveryTroubleshooting.md)

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
-   Default value 6,117,9,71,209

</td></tr><tr><td>

glide.discovery.switch\_interface\_types

</td><td>

Switch interface types: A comma-separated list of interface types that are considered. Interface type numbers are defined in the SNMP MIB-2, specifically in OID 1.3.6.1.2.1.2.2.1.3. Devices with any interface types that do NOT appear in this list are classified as routers, when they have routing. A complete list of the interface type numbers may be found on the [IANA web site](http://www.iana.org/assignments/smi-numbers), in the section "ifType definitions".-   Type: string
-   Default value: 7,8,9,26,53,62,69,71,78,115,117,209

</td></tr></tbody>
</table>## Learn

[What is network discovery?](https://www.servicenow.com/products/it-operations-management/what-is-network-discovery.html)

## Run network Discovery

Configure network Discovery from a Discovery schedule.

### Before you begin

Configure [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US), and keep port 161 open for SNMP access.

Role required: none

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules**.

2.  Click **New** and select **Networks** from the list in the Discover field.

3.  Select a MID Server.

    This field is mandatory.

4.  Complete the form, including the scheduling fields.

5.  Right-click in the header bar and select **Save** from the pop-up menu.

    The **Related Links** and related lists appear.

6.  Click **Network Discovery Private IPs** in Related Links to view the list of default private IP networks in the Discovery IP Ranges Related List.

    The default IP networks in this list are available to every Network Discovery you conduct and are sufficient for most discoveries.

7.  If your organization has additional private IP addresses, click **New** to add them.

    ![Private IP addresses](../image/PrivateIPAddresses.png "Private IP addresses")

8.  Add starting routers to the schedule in the Discovery Range Sets list.

    1.  Click the **Network Discovery Auto Starting Routers** link to populate the list with the starting router for each MID Server in your network.

    2.  Click **Edit** to add or delete routers from the list.

    ![Network Discovery schedule](../image/NetworkDiscoverySchedule.png "Network Discovery schedule")

9.  Run Discovery manually, or through the scheduler.


## Convert IP networks into Discovery range sets

After you conduct a network Discovery, you must convert the IP networks that were found into range sets for use in discovering other devices.

### Before you begin

Role required: agent\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Output and Artifacts** &gt; **IP Networks**.

2.  Click **New** to add an IP network.

3.  Ensure that the following field values are provided:

    -   **State**: Ready
    -   **Discover**: selected \(true\)
    -   **Router**: Select a router from the list. This field must not be empty.

        If your IP Networks were created through network Discovery, then these fields are populated automatically in the IP Networks related list. However, if you entered the IP Networks manually, and you want to convert your IP Networks into range sets manually, you must edit these fields accordingly.

        ![IP network form](../image/IPNetworkForm.png "IP network form")

4.  Select **Submit** to return to the list of IP Networks.

5.  In **Related Links**, select **Create Range Sets**.

    Use this feature to convert all the IP networks in the list into range sets.

    ![IP network list](../image/IPNetworkList.png "IP network list")

    The [Discovery Status](c_DiscoveryStatus.md) page appears, displaying the progress of the conversion. The system increments the **Started** and **Completed** count of IP networks, until all the networks are converted.


### What to do next

Add discovery range sets to [Discovery schedules](../task/t_CreateADiscoverySchedule.md#).

## Add a Discovery range set to a Discovery schedule

After creating discovery range sets from a network discovery, add the sets to a discovery schedule. This process narrows down the range of IP addresses that Shazzam probes can scan. You can also add a behavior.

### Before you begin

Role required: agent\_admin or admin

### Procedure

1.  Open a [Discovery schedule](../task/t_CreateADiscoverySchedule.md#).

2.  In the **Discovery Range Sets** related list, click **Edit** to add an existing range set and use the slushbucket to add the range set.

3.  On the **Discovery schedule** form, click the name of the range set under the **Range** column in the **Discovery Range Sets** related list.

4.  On the **Discovery Range Set** form, add a [Discovery behavior](c_DiscoveryBehaviors.md) if necessary.

    You can also activate or deactivate the range set for this schedule.

5.  Right-click the header, and then click **Save**.



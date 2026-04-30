---
title: Network experience pages
description: The Network experience pages display information about multiple facets of the network configuration. This information includes connection details, stability metrics, path metrics, and live application hops.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Device details pages, DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Network experience pages

The Network experience pages display information about multiple facets of the network configuration. This information includes connection details, stability metrics, path metrics, and live application hops.

## Connection details page

<table id="table_swc_dnn_1yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Wi-Fi details

</td><td>

Wi-Fi connection details, including network name, signal strength, Wi-Fi protocol, transmit rate, and Basic Service Set Identifier \(BSSID\).

</td></tr><tr><td>

Wired connection details

</td><td>

Wired connection information, including network name, status, speed, and driver version

</td></tr><tr><td class="sub-head" colspan="2">

VPN connection details

</td></tr><tr><td>

Last data fetched

</td><td>

Timestamp indicating how recently the VPN data was collected from the device.

</td></tr><tr><td>

Name

</td><td>

Name of the network connection profile.For example, VPN or network profile name.

</td></tr><tr><td>

Interface alias

</td><td>

User-friendly alias given to the network interface.For example, Wi-Fi, Ethernet.

</td></tr><tr><td>

Interface index

</td><td>

Unique identifier or index number for the network interface on the system.

</td></tr><tr><td>

Network category

</td><td>

Indicates the network type. For example, Public, Private, DomainAuthenticated.

For installed VPNs \(for example, Zscaler\), the DomainAuthenticated value indicates that VPN is connected. However, for cloud VPNs \(for example, GlobalProtect\), you can only infer if VPN is connected by confirming that the Interface description matches your VPN name.

**Note:** DomainAuthenticated means that user is connected to installed VPN.

</td></tr><tr><td>

Domain auth type

</td><td>

Specifies the type of domain authentication used for the network.For example, Ldap.

</td></tr><tr><td>

IPv4 connectivity

</td><td>

IPv4 connection status. For example, internet, NoTraffic, Disconnected.

</td></tr><tr><td>

IPv6 connectivity

</td><td>

IPv6 connection status \(similar to IPv4 status\).

</td></tr><tr><td>

Interface description

</td><td>

Descriptive name of the hardware or virtual interface. For example, network adapter name like Intel\(R\) 82574L Gigabit Network Connection or PANGP Virtual Ethernet Adapter.

</td></tr></tbody>
</table>## App connection stability page

Applicable to Windows OS only, information about the network stability is expressed graphically by latency, packet loss, and jitter.

<table id="table_jkj_djz_cdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application

</td><td>

List of monitored applications to select from to see the connection performance of a specific applicationThe list contains applications with atleast one domain and only if they were used in the last seven days.

</td></tr><tr><td>

Domains

</td><td>

List of related domains to selectYou can select up to two domains related to a specific application.

</td></tr><tr><td>

Select start date

</td><td>

Start date and time of the range for which the connection stability data is displayedYou can select any time duration within the last seven days.

</td></tr><tr><td>

Select end date

</td><td>

End date and time of the range for which the connection stability data is displayedIf you select a duration that is more than two days, then select **View network path**, the time range is set to selectedEndTime - two days.

</td></tr><tr><td>

Latency

</td><td>

Delay between sending and receiving data High latency results in noticeable delays and slower application response times, impacting overall performance.

</td></tr><tr><td>

Packet loss

</td><td>

Loss that occurs when data packets fail to reach their destination, leading to missing informationHigh packet loss causes communication disruptions like dropped calls, distorted audio, or incomplete videos and files.

</td></tr><tr><td>

Jitter

</td><td>

Variation in time between data packet arrivals. In stable networks, packets arrive at regular intervalsHigh jitter causes inconsistent delivery, leading to choppy audio, video, or performance.

</td></tr></tbody>
</table>## App connection path page

The app connection path is a route that consists of several hops between an end user’s device and a destination. The data packets travel through various networking devices such as routers, switches, and gateways.

<table id="table_mk1_yvt_rdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Filters

</td></tr><tr><td>

Application

</td><td>

List of monitored applications to select from to see the connection performance of a specific applicationIf you selected any filters on the App connection stability page and then select **View connection path**, the selected filters persist on the App connection path page.

</td></tr><tr><td>

Domains

</td><td>

List of related domains to selectIf you selected any filters on the App connection stability page and then select **View connection path**, the selected filters persist on the App connection path page.

</td></tr><tr><td>

Select start date

</td><td>

Start date and time of the range for which the connection stability data is displayedYou can select any time duration within the last seven days.

</td></tr><tr><td>

Select end date

</td><td>

End date and time of the range for which the connection stability data is displayedThe selected end date and time are used to limit the connection path duration to 2 days or 48 hours.

</td></tr><tr><td>

Time frame

</td><td>

Time at which the network path details are fetched

</td></tr><tr><td class="sub-head" colspan="2">

Connection hops

</td></tr><tr><td>

Domain

</td><td>

Domains selected for the application

</td></tr><tr><td>

Gateway

</td><td>

IP address of the gateway

</td></tr><tr><td>

Number of hops

</td><td>

Number of stops that data packets take when they travel from one network node or router to another on their way to a destination

</td></tr></tbody>
</table>## Live application hops page

|Field|Description|
|-----|-----------|
|Hop|Specific stop that data packets take when they travel from one network node or router to another on their way to a destination|
|Domain Name|Name that identifies the network domain on the internet|
|Address|IP address assigned to the specific router|
|RTT1|Duration in milliseconds \(ms\) that it takes for the first packet to get to a hop and back|
|RTT2|Duration in milliseconds \(ms\) that it takes for the second packet to get to a hop and back|
|RTT3|Duration in milliseconds \(ms\) that it takes for the third packet to get to a hop and back|

**Parent Topic:**[Device details pages](user-device-details-pages.md)


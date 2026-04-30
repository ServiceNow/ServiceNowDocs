---
title: Network monitoring page
description: View the various aspects of the Network monitoring section of a user or device. This section includes network server information, connection details, performance metrics, and application network hops. Use this information to assess the user's network performance.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Device details pages, DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Network monitoring page

View the various aspects of the Network monitoring section of a user or device. This section includes network server information, connection details, performance metrics, and application network hops. Use this information to assess the user's network performance.

|Field|Description|
|-----|-----------|
|WiFi details|WiFi connection details, including network name, signal strength, WiFi protocol, transmit rate, and BSSID \(Basic Service Set Identifier\).|
|Wired connection details|Wired connection information, including network name, status, speed, and driver version.|

<table id="table_jkj_djz_cdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Network stability

</td><td>

Currently applicable to Windows OS only, information about the network stability expressed graphically by the following metrics:-   Latency
-   Packet loss
-   Jitter

</td></tr><tr><td>

Network path

</td><td>

Route that consists of several hops between a user’s device and a destination. The data packets travel through various networking devices such as routers, switches, and gateways.You can enable this field to test and validate the feature.

**Note:** For information on how to enable Network path, see the [Enabling network path for windows devices \[KB1705499\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1705499) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Hop|Specific stop that data packets take when they travel from one network node or router to another on their way to a destination.|
|Domain Name|Name that identifies the network domain on the internet.|
|Address|The IP address assigned to the specific router.|
|RTT1|Duration in milliseconds \(ms\) that it takes for the first packet to get to a hop and back.|
|RTT2|Duration in milliseconds \(ms\) that it takes for the second packet to get to a hop and back.|
|RTT3|Duration in milliseconds \(ms\) that it takes for the third packet to get to a hop and back.|

To return to the main network page, see [Network monitoring](../concept/users-network.md).

**Parent Topic:**[Device details pages](user-device-details-pages.md)


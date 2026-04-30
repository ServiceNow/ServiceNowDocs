---
title: Network monitoring
description: The Network monitoring page in the displays information about multiple facets of a user's network configuration. This information includes connection details, performance metrics, and application network hops.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Device details, Application and Device Health, Monitor, Digital End-User Experience, IT Service Management]
---

# Network monitoring

The Network monitoring page in the displays information about multiple facets of a user's network configuration. This information includes connection details, performance metrics, and application network hops.

## Connection details

The Connection details section has information about the user's network connection, including the connection status, WiFi and wired connection signal strength, WiFi protocol, and WiFi BSSID \(Basic Service Set Identifier\).

Under WiFi details, you can find metric names and the corresponding values that provide a comprehensive overview of their WiFi performance, including signal strength, WiFi protocol, and WiFi BSSID \(Basic Service Set Identifier\).

The Wired connection details contain metric names and values related to the user's wired network connection, including the MAC address, connection speed, connection duplex mode \(full or half\), and data usage. Additional metrics may include latency, packet loss, and jitter.

## Performance metrics

The Performance metrics section applies to Windows OS only. The section evaluates network stability using the following key factors:

-   Latency: The delay between sending and receiving data. High latency results in noticeable delays and slower application response times, impacting overall performance.
-   Packet loss: The loss that occurs when data packets fail to reach their destination, leading to missing information. High packet loss causes communication disruptions like dropped calls, distorted audio, or incomplete videos and files.
-   Jitter: The variation in time between data packet arrivals. In stable networks, packets arrive at regular intervals. High jitter causes inconsistent delivery, leading to choppy audio, video, or performance.

Improving these metrics promotes network consistency and reliability, which help create smooth user experiences and data-intensive application use.

## Application hops

This section showcases the applications drop-down menu, domain name, and address of the hop domain, as well as the round-trip times \(RTT1, RTT2, RTT3\). You can use this information to work on the network configuration performance.

Use the **Applications** drop-down menu to select an application to view its hop information. To get the latest information, select **Run**.

For more information on the network card, see [Network monitoring page](../reference/user-network-card.md).


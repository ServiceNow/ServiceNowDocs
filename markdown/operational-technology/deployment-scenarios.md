---
title: Discovery for Operational Technology \(OT\) deployment scenarios
description: The following section describes the different scenarios based on Network architecture details. It provides a description of how to use the Discovery for Operational Technology \(OT\) components depending on the set up of your Discovery Console for OT, Discovery Sensor for OT, Discovery OT Collector, and networks.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 3
breadcrumb: [Deploy Operational Technology Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Discovery for Operational Technology \(OT\) deployment scenarios

The following section describes the different scenarios based on Network architecture details. It provides a description of how to use the Discovery for Operational Technology \(OT\) components depending on the set up of your Discovery Console for OT, Discovery Sensor for OT, Discovery OT Collector, and networks.

**Note:** General recommendations and guidance are listed in the following sections. Not all networks are the same, it's important to point out that the requirements in this section are a generalization. Factors such as the level of segmentation, communication pathways, amount of traffic on the network, network redundancy, environmental conditions of the site, and physical constraints of the site must be considered when determining network requirements.

## Scenario \#1: Flat network architecture across multiple sites

A flat network architecture is a network design that has all available Discovery Consoles for OT, Discovery Sensors for OT, and Discovery OT Collectors connected to a single network, where the Sensors and Collectors can communicate with each other directly.

You can have one or more sites that communicate with each other.

![Flat network](../../operational-technology-discovery-deployment-guide/images/flat-network.png "Flat network")

The Console, Sensors, and MID Server connect at Purdue level 3.5 and push data through the switches and the firewall to the ServiceNow instance for ingestion.

**Components in the flat network**

The following are the components in a flat network.

-   Discovery Console for OT and Discovery Sensor for OT.
-   A localized appliance or VM that serves as the command-and-control interface for asset discovery and communication in its respective segment. This appliance or VM manages credentials, protocol handlers, and initiates querying operations locally. In such a scenario, a typical deployment would mean that one Console covers multiple sites.
-   Deploy the Console at a layer where the MID Server can connect to the Console and the ServiceNow instance.
-   Deploy Sensors based on the desired speed of the discovery. In a truly flat network, a Discovery Sensor for OT should be able to reach all the OT assets in that network. More Sensors in the network can help improve the speed of discovery.

## Scenario \#2: Multiple independent segmented sites

A segmented site architecture is a network design that has the network split into multiple segments. Each segment contains its own Discovery Console for OT and multiples of the Discovery Sensor for OT and the Discover OT Collector. There is no communication between sites. Each of the segments could be considered a flat network.

![Segmented site](../../operational-technology-discovery-deployment-guide/images/segmented-site.png "Segmented sites")

In this OT environment, the network is segmented into **three distinct zones** for operational clarity, security, and control:

-   Site 1 Operational Technology segment
-   Site 2 Operational Technology segment
-   Physical Security Network segment

Each segment contains its own isolated infrastructure to reduce risk and increase visibility in its respective domain. Components in each segment:

-   Discovery Console for OT or VM that serves as the command-and-control interface for asset discovery and communication in its respective segment. It manages credentials, protocol handlers, and initiates scanning operations locally.
-   Discovery Sensor for OT is deployed in each segment where the Sensor can perform active discovery in the segment and collect network traffic, and query for known protocols \(for example, Modbus, DNP3, BACnet\). It reports findings to its segment’s Console.

The Consoles and Sensors are deployed in their respective network zones and don't have direct outbound access to the internet.

## Scenario \# 3: Micro-segmented site with multiple networks

A segmented site architecture with multiple networks is a network design that has more than one network split into multiple segments. Each segment contains multiple network segments and its own Discovery Console for OT and Discovery Sensor for OT.

-   Make sure the Sensors and Collectors have a communication pathway to the Console.
-   Deploy Sensors in each segment where the Sensor can perform active discovery in the segment and collect network traffic and can scan or query for known protocols \(for example, Modbus, DNP3, BACnet\). It reports findings to its segment's Console.
-   If you want to leverage an existing host to do the discovery in the network such as Human Machine Interface \(HMI\) or Engineering Workstation \(EWS\), you can install the Discovery OT Collectors to do the discovery.

![](../images/seg-site-multi.png "Segmented site with multiple networks")


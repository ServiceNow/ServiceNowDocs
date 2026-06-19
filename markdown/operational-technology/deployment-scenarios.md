---
title: Operational Technology Discovery deployment scenarios
description: Deployment scenarios for OT Discovery vary based on a network's architecture. Use these scenarios to help determine how to deploy the OT Discovery components in your OT environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/deployment-scenarios.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 5
breadcrumb: [Deploy Operational Technology Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Operational Technology Discovery deployment scenarios

Deployment scenarios for OT Discovery vary based on a network's architecture. Use these scenarios to help determine how to deploy the OT Discovery components in your OT environment.

**Note:** The OT Discovery Collector can be deployed to the same locations as the Discovery Sensor for OT.

## General recommendations

General recommendations and guidance are listed in each scenario in these sections. Not all networks are the same. The requirements in this section are a generalization for the scenario. Consider factors such as segmentation level, communication pathways, network traffic, redundancy, and environmental conditions. For resource recommendations for the Operational Technology Discovery components see the [Resources for OT Discovery System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/deployment-scenarios.md) section.

## Flat network architecture across multiple sites

A flat network architecture is a network design that has all available Discovery Console for OT, Discovery Sensor for OT, and OT Discovery Collector connected to a single network, where the Sensors and Collectors can communicate with each other directly.

You can have one or more sites that communicate with each other.

\[Omitted image "flat-network.png"\] Alt text: Flat network

The Console, Sensors, and MID Server connect at Purdue level 3.5 and push data through the switches and the firewall to the ServiceNow instance for ingestion.

**Components in the flat network**

The following are the components in a flat network.

-   Discovery Console for OT and Discovery Sensor for OT.
-   A localized appliance or VM that serves as the command-and-control interface for asset discovery and communication in its respective segment. This appliance or VM manages credentials, protocol handlers, and initiates querying operations locally. In such a scenario, a typical deployment means that one Console covers multiple sites.
-   Deploy the Console at a layer where the MID Server can connect to the Console and the ServiceNow instance.
-   Deploy Sensors based on the desired speed of the discovery. In a truly flat network, a Discovery Sensor for OT can reach all the OT assets in that network. More Sensors in the network can help improve the speed of discovery.

## Multiple independent segmented sites

A segmented site architecture is a network design that has the network split into multiple segments. Each segment contains its own Discovery Console for OT and multiples of the Discovery Sensor for OT and the OT Discovery Collector. There is no communication between sites. Each of the segments could be considered a flat network.

\[Omitted image "segmented-site.png"\] Alt text: Segmented site

In this OT environment, the network is segmented into three distinct zones for operational clarity, security, and control:

-   Site 1 Operational Technology segment
-   Site 2 Operational Technology segment
-   Physical Security Network segment

Each segment contains its own isolated infrastructure to reduce risk and increase visibility in its respective domain. Components in each segment:

-   Discovery Console for OT or VM that serves as the command-and-control interface for asset discovery and communication in its respective segment. It manages credentials, protocol handlers, and initiates scanning operations locally.
-   Discovery Sensor for OT is deployed in each segment. The Sensor performs active discovery, collects network traffic, and queries for known protocols \(for example, Modbus, DNP3, BACnet\). It reports findings to its segment's Console.

The Consoles and Sensors are deployed in their respective network zones and don't have direct outbound access to the internet.

## Micro-segmented site with multiple networks

A segmented site architecture with multiple networks is a network design that has more than one network split into multiple segments. Each segment contains multiple network segments and its own Discovery Console for OT and Discovery Sensor for OT.

-   Make sure the Sensors and Collectors have a communication pathway to the Console.
-   Deploy Sensors in each segment where the Sensor can perform active discovery in the segment and collect network traffic and can scan or query for known protocols \(for example, Modbus, DNP3, BACnet\). It reports findings to its segment's Console.
-   If you use an existing host to do the discovery in the network such as Human Machine Interface \(HMI\) or Engineering Workstation \(EWS\), you can install the OT Discovery Collector to perform discovery.

\[Omitted image "seg-site-multi.png"\] Alt text: Micro-segmented site with multiple networks

## Resources for OT Discovery System

The requirements in this section are a generalization. Consider factors such as segmentation level, communication pathways, network traffic, redundancy, and environmental conditions. Also account for physical constraints when determining network requirements. The following tables provide resource estimates for each OT Discovery component. Review your system requirements beyond these minimums.

<table id="table_i5f_kpx_vgc"><thead><tr><th>

Component

</th><th>

Minimum System Requirements

</th></tr></thead><tbody><tr><td>

Discovery Console for OT

</td><td>

-   16 GB RAM
-   100 GB Hard drive
-   2 CPUs

</td></tr></tbody>
</table>For additional requirements for the Console, see [Requirements for Discovery Console for OT installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/reqs-ot-console-installation.md) and [Install the Discovery Console for OT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/install-discovery-console-ot.md).

<table id="table_sensor_requirements"><thead><tr><th>

Component

</th><th>

Minimum System Requirements

</th></tr></thead><tbody><tr><td>

Discovery Sensor for OT

</td><td>

-   2 GB RAM\*
-   100 GB Hard drive
-   2 CPUs
-   2 virtual NIC cards

\*8 GB of RAM is recommend for all queries.

</td></tr></tbody>
</table>For additional requirements for the Sensor, see .

**Collector minimum system requirements**

The OT Discovery Collector can be installed and run on either a Windows OS or a Linux OS.

<table id="table_collector"><thead><tr><th>

Component Operating System

</th><th>

Minimum System Requirements

</th></tr></thead><tbody><tr><td>

Windows

</td><td>

The OT Discovery Collector installation is compatible with Windows 10 or Windows 11 systems.

 The required Windows \(10 or 11\) environment for the OT Discovery Collector is x86\_64. ARM or Apple Silicon devices are not supported.

 See [Install the OT Discovery Collector on a Windows system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/installing-collector-on-windows.md).

</td></tr><tr><td>

Linux

</td><td>

See [Install OT Discovery Collector on a Linux system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/linux-install-ot-discovery-collector.md) for specific information.

</td></tr></tbody>
</table>
---
title: Architectural considerations
description: This document intends to describe the ServiceNow Operational Technology Discovery architecture and covers how discovery components find, identify, and inventory devices in an Operational Technology environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/architect-considerations.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 9
breadcrumb: [Deploy Operational Technology Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Architectural considerations

This document intends to describe the ServiceNow Operational Technology Discovery architecture and covers how discovery components find, identify, and inventory devices in an Operational Technology environment.

## Operational Technology Discovery software architecture

Today's industrial environments are made up of hundreds — sometimes thousands — of connected devices: programmable logic controllers, remote terminal units, human-machine interfaces, protection relays, and more. Tracking all of them — what they are, where they sit in your network, and whether they behave as expected — is one of the foundational challenges of operational technology.

The following describes the software architecture underlying the ServiceNow Operational Technology Discovery platform.

## How discovery works

At its core, Operational Technology Discovery actively reaches out to devices on your network using the same protocol language those devices already speak. Each device receives a query in its native protocol and responds with identifying information. A Modbus device gets a Modbus query. An EtherNet/IP device gets an EtherNet/IP query. This approach avoids aggressive network scanning that can disrupt sensitive industrial equipment.

The result is an updated inventory of your OT environment, visible through a single interface and integrated directly into your broader IT service management platform.

**Note:** The user sets the protocol parameters for the query from the Discovery Console for OT.

## The discovery components

The architecture is built around three components that work together. It is important to understand each component's distinct role and responsibilities.

The Discovery Console for OT is the interface you use to configure discovery, define the areas of your network you want to scan, and view the results. You can place more than one Console in your network.

-   The Console is your starting point. It is where you define your industrial sites, configure the network zones and sites you want to discover, and set up the queries that drive the process. After discovery is running, the Console is also where you view results — seeing your OT environment take shape as devices are identified and cataloged.
-   In terms of network placement, the Console typically, but not necessarily, sits in an IT/OT DMZ or a dedicated secure management zone. It doesn't perform discovery itself, but it configures the Sensor and serves as the central point of visibility across your entire deployment.

The Discovery Sensor for OT does the discovery work. Deployed as software on a virtual machine or physical server, the Sensor reaches out to devices in your network, identifies them, and builds your device inventory. It does this actively — on a schedule you configure. You can place Sensors throughout your network.

-   The Sensor does the active discovery. Deployed as software on a virtual machine or bare metal system, it executes the queries configured in the Console. It builds your device inventory from the responses it receives. When the Sensor queries a device, it uses that device's native industrial protocol — Modbus, DNP3, EtherNet/IP, and others. This keeps the interaction safe for the network. You can select the protocol for the query in the Console.
-   However, industrial environments are often deeply segmented by design — and the Collector addresses this.

The OT Discovery Collector extends the Sensor's reach into parts of your network that the Sensor can't access directly. In large or highly segmented industrial environments, a single Sensor may not have network visibility into every zone. Collectors are lightweight components deployed within those zones to bridge the gap. You can also use more than one of these components in your OT environment.

-   The Collector is a \(small\) application that can be installed on exiting systems \(for example, HMIs\) to extend discovery.
-   Combined with the Sensor, it offers flexible deployment options to assist with maximum coverage of the OT network.

## The discovery workflow

It is easier to understand how the three components work together when you follow a discovery job from start to finish. The following covers that process — from building a query in the Console through to a fully populated device inventory in the ServiceNow instance.

**Step 1: The network is built with Discovery in mind**

Before any discovery runs, the Consoles, Sensors, and Collectors are deployed at positions in the network that reflects the user's OT environment. There are no fixed rules about how many OT components are needed to deploy or exactly where to place them. This depends on your OT network.

Sensors and Collectors are deployed to cover the network. They can be deployed on bare-metal hardware or on a Virtual Machine, depending on what suits each part of the network. The Console, however, is recommended to run on a Virtual Machine. Discovery can return photographic data alongside standard device attributes. A Linux distribution should be installed on the same VM before the Console is installed.

**Step 2: Build a query in the Console**.

Discovery begins when you create a query in the Console, where you define exactly what you want to discover and how. Query parameters include:

-   **Protocols**: Which industrial protocols to use when communicating with devices, such as Modbus, DNP3, or EtherNet/IP.
-   **Brands**: Filtering discovery toward specific device manufacturers if needed.
-   **Ports**: Which network ports to include in the query.
-   **Assets**: Which devices or ranges of devices to target.
-   **Sites**: You can create or discover sites.
-   **Query type**: Simplified and advanced query types such as the OPC-UA type, which captures photographic and visual data from devices rather than relying solely on protocol-based communication.

You can also select specific Sensors and Collectors the query should use. Because Sensors and Collectors are deployed at known positions in the network, you can pick specific components by name — choosing the Sensor inside Line \#1, for example, because you know that's where the devices you want to discover are located. Alternatively, you can let the query use the appropriate components based on where they are positioned in the network.

**Step 3: The query runs through the selected components**.

Once configured and launched, the query drives everything. Each Sensor and Collector executes the query within its part of the network, reaching out to devices using the protocols and parameters the user defined. A Sensor handles discovery in the zones it can directly access. A Collector does the same in the deeper or more restricted zones where it has been positioned.

Because both Sensors and Collectors are independently deployed and selectable, a single query can span multiple zones simultaneously. A Sensor handles one part of the network and a Collector handles another, all driven by the same query configuration.

**Step 4: Results upload to ServiceNow**.

As devices respond, their details are collected and returned to the Console. These include device type, vendor, model, firmware version, network address, zone, Purdue level, and where applicable, photographic data. From the Console, the data is uploaded to the ServiceNow instance.

**Note:** It should be noted that depending your network structure, there are additional OT components used to reach the ServiceNow instance, if needed. For further information on OT Discovery connections, see the [Operational Technology Discovery deployment scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/deployment-scenarios.md) or the [Service Graph Connector for ServiceNow OT Discovery Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/sgc-ot-discovery-guided-setup.md).

Within the ServiceNow instance, discovered devices are mapped to configuration items predefined in the CMDB. These configuration items are based on industry and operational device types, reflecting the OT world your team works in every day. They can be edited and adjusted to fit the data retrieved, giving your team flexibility to tailor the inventory to your environment.

The result is an accurate, up-to-date inventory of your OT environment — built through the discovery components your company has positioned in the network. It is visible through a single interface and integrated directly to ServiceNow without manual surveys or spreadsheets.

## Active and passive discovery approaches

Before exploring how the discovery components work in detail, it helps to understand the two broad approaches to OT discovery and where each one fits. Both are used across the industry, and many operational environments already have some form of network monitoring in place. The difference between them also explains some of the design decisions behind the system described in this topic.

**Passive** discovery works by listening to network traffic rather than initiating communication with devices. Traffic is captured through one of two methods: SPAN ports or network TAPs. SPAN ports are software-based configurations on a network switch that mirror traffic to a monitoring point. Network TAPs are dedicated hardware devices that create exact copies of network traffic at wire speed.

After traffic is captured, Deep Packet Inspection \(DPI\) examines industrial protocol content. It identifies device vendors, models, firmware versions, and communication patterns without sending a query to a device. This makes passive discovery completely non-intrusive — devices are unaware they are being observed.

However, passive discovery has a fundamental limitation: it can only detect devices that are actively communicating during the observation window. Silent devices, dormant assets, or systems that communicate only within local sub-nets that don't cross a monitoring point remain entirely invisible. SPAN ports introduce an additional concern — because SPAN traffic receives the lowest priority on a switch, packets can be dropped even at low network utilization levels. Network TAPs avoid this by capturing 100% of traffic at wire speed but require physical hardware installation.

**Active** discovery initiates communication directly with devices using their native industrial protocol language — sending the same kinds of queries an engineering workstation or HMI would send to a PLC. These queries are indistinguishable from normal operations. Devices cannot distinguish these queries from regular engineering traffic, making properly implemented active discovery safe for operational networks.

Active discovery is easier to setup and start because it can require a Console and a single Sensor or Collector rather than a distributed set of SPAN ports and collection devices.

The key advantage of active discovery is coverage. Because it reaches out to devices rather than waiting for them to communicate, it can detect silent and dormant assets that passive monitoring would never see. It also retrieves granular details — firmware versions, serial numbers, configurations — that may never appear in normal network traffic.

|Interactions|Passive \(SPAN/TAP\)|Active \(Native Protocol\)|
|------------|--------------------|--------------------------|
|Device interaction|None — listens only|Direct query using native protocol|
|Silent device detection|No|Yes|
|Network impact|None|Minimal — read-only, rate-limited|
|Hardware required|TAP requires hardware; SPAN does not|No additional hardware|
|Data captured|Traffic observed during window only|On demand, scheduled, or continuous|
|Packet loss risk|Yes \(SPAN ports\)|Not applicable|

## Wrapping up

Operational Technology Discovery is built on the principle that visibility should not come at the cost of safety. By deploying the Console, Sensor, and Collector at deliberate positions within your network — and querying devices in a way that is safe for operational environments — the system adapts to your environment rather than requiring you to adapt your environment to it. Whether you're managing a single compact site or a large enterprise with dozens of segmented zones, the architecture scales accordingly. The result is a current, accurate inventory of your OT environment, fully integrated into ServiceNow and built without disrupting the operational processes your network supports.


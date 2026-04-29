---
title: Enabling OT Discovery component communications
description: This section describes how the OT Discovery components should be connected so they can communicate with each other.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 2
breadcrumb: [Deploy Operational Technology Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Enabling OT Discovery component communications

This section describes how the OT Discovery components should be connected so they can communicate with each other.

## Component communications

When determining the environment architecture for your deployment, consider how the following OT Discovery components interact.

-   MID Server-to-ServiceNow instance:
    -   The MID Server needs to communicate with the ServiceNow instance to push the information from Discovery Console for OT.

        **Note:** If the Discovery Console for OT can reach the internet, the MID Server might not be needed in your OT configuration.

    -   This configuration and deployment is the same as with any other MID Server.
    -   The Service Graph Connector \(SGC\) needs to communicate with the MID Server, the Console, and the ServiceNow instance.
-   Console-to-MID Server communication:

    -   Deploy a separate MID Server for each network or network segment.
    -   Configure firewall rules to enable communication across networks or network segment boundaries.
    -   The Console needs to communicate with the Sensors, the Collectors, the MID Server, the SGC, and your ServiceNow instance.
    ![Network setup](../../operational-technology-discovery-deployment-guide/images/network-setup-communications.png "Network communication setup")

-   Sensor-to-Console communication:
    -   Deploy a separate Console for each network, network segment, or system.
    -   Configure firewall rules to enable communication across networks or network segment boundaries.
    -   The Discovery Sensor for OT needs to communicate with OT assets and with the Discovery Console for OT.
    -   Discovery Sensor for OT data is pushed to the ServiceNow instance by the Service Graph Connector.
-   Sensor-to-asset communication:
    -   Deploy a separate Sensor for each network, network segment, or system.
    -   Configure firewall rules to enable communication across network, network segment, or system boundaries.
-   Discovery OT Collector-to-Console communication:
    -   Discovery OT Collector needs to communicate with the Console.
    -   The Collector communicates with the Console and with your system's assets.

## Network port map

The following table describes how to set up network ports.

|Source|Destination Port|Direction|Destination|Required/Optional|Description|
|------|----------------|---------|-----------|-----------------|-----------|
|Management Console|8443 \(HTTPS\) inbound|Bi &lt;-&gt;|Workstation|Required|Console web interface|
|Management Console|5671 \(AMQP\) inbound|Uni &lt;-|Sensor|Required|Communications from Sensors to Console|
|Management Console|123 \(NTP\) inbound|Uni &lt;-|Time Server /Esxi Host|Optional|Clock synchronization, Not needed it time server or hypervisor will provide time.|
|Management Console|8443 API|Uni &lt;-|MID Server|Required|Import data from Management Console via the APIs.|
|Management Console|22 \(SSH\) inbound|&lt;-|Host Setup Computer|Optional \(setup\)|Additional support during deployment|
|Sensor|5671 \(AMQP\) outbound|Uni &lt;-|Management Console|Required|Communications from Sensors to Console|
|Sensor|443 \(HTTP\) inbound|&lt;-|Host Setup Computer|Required|Additional support during deployment|
|Sensor|22 \(SSH\) inbound|&lt;-|Host Setup Computer|Required|Additional support during deployment|
|MID Server|443|Bi &lt;-&gt;|NOW instance /Web|Required|Communications from the MID Server to the NOW fabric internet facing.|


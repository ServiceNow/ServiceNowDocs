---
title: Explore the Discovery Sensor for OT
description: The Discovery Sensor for OT provides you with enhanced scanning and query functionality to manage your assets in the OT environment.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Discovery Sensor for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Explore the Discovery Sensor for OT

The Discovery Sensor for OT provides you with enhanced scanning and query functionality to manage your assets in the OT environment.

## Discovery Sensor for Operational Technology \(OT\) overview

This section provides an overview of the Discovery Sensor for OT and its integration with the Discovery Console for OT. For detailed functionality and configuration, refer to [Discovery Console for OT](ot-discovery-console-landing.md).

## Sensors page on the Discovery Console for OT

The Sensors page displays a list of all sensors that are associated with a Discovery Console for OT. To view the Sensors page, select the Sensors link in the Main Menu. Then select **Sensors** from the drop-down list to display the list of sensors. For monitoring purposes, the list is sorted first by Sensor Status, next by Configuration Status, and then by Sensor Name to allow users to quickly find a sensor that needs attention.

## Sensor Information

The Sensor Information page shows configuration and status information for the Sensor you select. In the Sensor List page, click on the name of a Sensor to view its information. Each tab on the Sensor Information page is detailed below.

Most Sensors have similar configuration settings; however, each type of Sensor has different settings available based on their capabilities. These differences are described in the sections below.

**Basic**

Displays the basic configuration information for a Sensor. This includes the Sensor Name, Sensor Type, Serial Number, Firmware Version, and user definable location information that includes fields for the Latitude, Longitude, and Location Description for the Sensor.

**Network**

A description of each field on the Network tab is as follows.

-   Console Endpoint – Shows the IP address of the Discovery Console for OT that the Sensor is configured to use.
-   Sensor Gateway – Shows the IP address assigned to the Sensor that is used to route traffic between networks.
-   Management Interface – Connects the Sensor to an out-of-band network for communication with the Discovery Console for OT.
    -   Management Endpoint: Sets the IP address for the Sensor which it uses to communicate with the Discovery Console for OT.
    -   Management Subnet: Sets the subnet mask/Classless Inter-Domain Routing \(CIDR\) for the Sensor's communication with the Discovery Console for OT.
    -   \(Optional\) Management VLAN: Specifies the VLAN identifier that the management interface will use to tag network communications for participation in VLAN segregated networks.
-   Span Interface: When enabled, allows the Sensor to enter a mode where it can collect all network traffic received on the ETHERNET 1 port. This allows the IDS to collect data from the network. When disabled, the Sensor will not be able to perform any data collection.
-   Ethernet Interfaces: Lists all Ethernet Interfaces for the Sensor. The list includes the Interface name and the MAC Address for each one.

**Services**

Allows you to configure specific services that run on a Sensor. Currently, the user can use this feature to enable or disable the SSH service on a Sensor. Click the Edit button and then click the toggle to turn the SSH service on or off. Below are the Status and Updated On fields for the SSH service. Similarly, this page also allows users to enable or disable the Web Management service \(see the Sensor Management Interface section for details\) and view the corresponding Status and Updated On fields. The SSH service is enabled by default on all Sensors to facilitate post-installation configuration and may be disabled if necessary to match OT network security policies.

**Services Config**

Includes the Log Streaming Service and the Web Management Service. The Log Streaming Service can be used to stream logs from Sensors to the Discovery Console for OT. The Log Streaming Service also provides the ability to retain logged information for a longer time and may result in quicker customer issue resolution.

To enable the Log Streaming service for a specific Sensor, turn it on using the Log Streaming toggle in the Services section of that Sensor. Next, navigate to the Services Config section and select the log severity. The user may select the minimum log severity to include in the streaming for each Sensor. Selecting Debug will result in the most information being logged. We recommend enabling this feature with Debug as the selected severity level unless the system is operating in a bandwidth-constrained environment. Click Save to make the changes permanent or click Cancel to undo.

The data streamed is not viewable in the Console UI. The Console only provides the ability to enable or disable the service and set the log severity level. Streamed log information is retained on the Console for 30 days.

The Web Management Service feature can be used to reset the password for the Web Management Service on the Sensor. To reset the password, click Edit, type a password into the edit field, enter it in the Confirm Password field, and click Save. Below the Confirm Password field are the Status and Updated On fields, which provide information about the Web Management Service on the Sensor.

**Sites**

The Sites tab displays which Sites are associated to the selected Sensor during an Auto Query. The Allow/Deny setting indicates whether the Sensor is associated to the particular Site. The tab also displays the Site name, what setting is recommended for that Site, and the reason for the recommendation. A Deny recommendation means the Site does not appear to be related to the Sensor. An Allow recommendation means the Site’s network ranges match the Device IP. Allow can also mean the Site allows All Sensors.![Sensor Sites tab](../images/sensor-sites-associated.png)

**Status**

Shows the connection status of the Sensor, including the deployment status for basic configuration, network configuration, arpwatch network configuration, allowlist configuration, policy, firmware updates, and security bypass mode updates.

**Actions**

The Actions menu in the top right corner of the Sensor Information page provides links to several actions related to the Sensor. These actions include Deregister Sensor, Enable Bypass Mode, Reboot Sensor, Remove Sensor from Console \(only for Sensors with Connection Lost status\), View Allowlist, View Data Streams, and View Health Overview. The last three actions can also be completed by clicking on the corresponding buttons at the bottom left of the page. Information about the first four actions in the list is included below.

-   **Deregister Device** – This setting deregisters the Sensor from the Console. This action resets the network settings to factory defaults and removes the Sensor from the Console.
-   **Reboot Device** – This setting reboots the Sensor.

## What to do next

To get started with the installation of the Discovery Sensor for OT, see [Configure the Discovery Sensor for OT](../task/configure-ot-discovery-sensor.md).


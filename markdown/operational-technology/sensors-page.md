---
title: Sensors page
description: The Sensors page is used to monitor the statuses and manage the Sensor settings.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Sensors page

The Sensors page is used to monitor the statuses and manage the Sensor settings.

The Sensors page displays a list of all Sensors that are associated with the Discovery Console for OT. To access the Sensors page, select the Sensors menu in the side panel and then, underneath that, select **Sensors**.

![On and offline Sensors](../images/sensor-page-new.jpeg)

## Sensor Information

The Sensor information page shows Sensor configuration and status information. To view this information, in the Sensor page, select the name of a Sensor to view its information. Most Sensors have similar configuration settings. However, each type of Sensor has different settings available based on their capabilities.

![Sensor information](../images/sensor-info.png)

The following sections describe the Sensor information available.

## Basic

Displays the basic configuration information for a Sensor. The configuration includes the Sensor Name, Sensor Type, Serial Number, Firmware Version, and user definable location information that includes fields for the Latitude, Longitude, and Location Description for the Sensor.

## Network

The Network tab shows the network settings as they’re currently configured for a Sensor. A description of each field is as follows:

-   Console Endpoint: Shows the IP address of the Discovery Console for OT that the Sensor is configured to use.
-   Sensor Gateway: Shows the IP address assigned to the Sensor that is used to route traffic between networks.
-   Management Interface: Connects the Sensor to an out-of-band network for communication with the Discovery Console for OT.
    -   Management Endpoint: Sets the IP address for the Sensor which it uses to communicate with the Discovery Console for OT.
    -   Management Subnet: Sets the subnet mask/Classless Inter-Domain Routing \(CIDR\) for the Sensor communication with the Discovery Console for OT.
    -   \(Optional\) Management VLAN: Specifies the VLAN identifier that the management interface uses to tag network communications for participation in VLAN segregated networks.
-   Span Interface: When enabled, enables the Sensor to enter a mode where it can collect all network traffic received on the ETHERNET 1 port. Doing this enables the IDS to collect data from the network. When turned off, the Sensor can't perform any data collection.
-   Ethernet Interfaces: Lists all Ethernet Interfaces for the Sensor. The list includes the Interface name and the MAC Address for each one.

## Health

The Health tab allows you to view graphs reflecting trends in CPU, memory, and disk utilization as well as temperature and network input and output over time.

## Services

Enables you to configure specific services that run on a Sensor. Currently, you can use this feature to enable or disable the SSH service on a Sensor. Select the **Edit** button and then select the toggle to turn the SSH service on or off. Below are the **Status** and **Updated On** fields for the SSH service. Similarly, you can enable or disable the Web Management service and view the corresponding **Status** and **Updated On** fields. The SSH service is enabled by default on all Sensors to facilitate post-installation configuration.

## Services Config

Includes the Log Streaming Service and the Web Management Service. The Log Streaming Service can be used to stream logs from Sensors to the Discovery Console for OT. The Log Streaming Service also provides the ability to retain logged information for a longer time and can result in quicker customer issue resolution.

To enable the Log Streaming service for a specific Sensor, turn it on using the Log Streaming toggle in the Services section of that Sensor. Next, navigate to the Services Config section and select the log severity. You can select the minimum log severity to include in the streaming for each Sensor. Selecting Debug results in the most information being logged.

The data stream isn’t viewable in the Console UI. The Console only provides the ability to enable or disable the service and set the log severity level. Streamed log information is retained on the Console for 30 days.

You can use the Web Management Service feature to reset the password for the Web Management Service on the Sensor. To reset the password, select Edit, enter a password in the **Edit** field, enter the same password in the **Confirm Password** field, and select **Save**.

Below the **Confirm Password** field are the **Status** and **Updated On** fields, which provide information about the Web Management Service on the Sensor.

## SSH Keys

On this tab, you can Add Public Keys by pasting them into the Paste SSH key\(s\) field. The **Password Authentication** is enabled by default in the initial sensor install. If you want to disable SSH password authentication, slide the toggle to the left. You can also upload your own SSH Keys. The required format for a key is .pub.

Duplicate keys are automatically removed, so the same SSH key only appears once, even if there are small formatting differences like extra spaces.

**Note:** As a safety feature to allow continued SSH access, disabling password authentication should only be considered if you have uploaded at least one SSH public key to the Sensor.

![Password Authentication](../images/ssh-key-tab.png)

## Sites

The **Sites** tab displays which Sites are associated with the selected Sensor during an Auto Query. The Allow/Deny setting indicates whether the Sensor is associated with the Site. The tab also displays the Site name, what setting is recommended for that Site, and the reason for the recommendation. A Deny recommendation means the Site does not appear to be related to the Sensor. An Allow recommendation means the Site’s network ranges match the Device IP.

![Allow-Deny settings](../images/allow-deny-sensors.png)

## Status

Shows the connection status of the Sensor, including the deployment status for basic configuration, network configuration, arpwatch networks configuration, allow list configuration, policy, and firmware updates.

## Actions

The Actions menu in the Sensor Information page lets you access the following actions available for your Sensors.

-   **Deregister Device**: Deregisters the Sensor from the Console. This action resets the network settings to factory defaults and removes the Sensor from the Console.
-   **Reboot Device**: Reboots the Sensor.

## What to do next

See the [Discovery Sensor for Operational Technology \(OT\)](ot-discovery-sensor-landing.md) section for procedures you can do with Sensors.


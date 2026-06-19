---
title: Edit an Appliance record
description: This section describes what information that is available and that is setup on an Appliance record
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/edit-appliance-record.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: concept
last_updated: "2026-06-10"
reading_time_minutes: 5
breadcrumb: [Appliances page, Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Edit an Appliance record

This section describes what information that is available and that is setup on an Appliance record

## Edit an Appliance

To edit any appliance, select the Name of the appliance. The appliance record opens.

\[Omitted image "appliance-record-tabs.png"\] Alt text: Appliance record

The appliance view has tabs with additional information and options. Move to a tab and then select the **Edit** button to edit any of the appliance settings. Select the **Save** button to save your changes or **Cancel** to discard them.

The following sections describe the available appliance information shown as tabs in the record.

## Basic

This tab displays the basic configuration information for the appliance. The configuration includes the **Name**, **Type**, **Serial Number**, and **Firmware Version**. It also contains user-definable location information including fields for **Latitude**, **Longitude**, and **Location Description**.

## Network

The **Network** tab shows the network settings as they're currently configured for the appliance. Each field is described in the following list:

-   **Console Endpoint**: Shows the IP address of the Discovery Console for OT that the appliance is configured to use.
-   **Appliance Gateway**: Shows the IP address assigned to the appliance that is used to route traffic between networks.
-   **Management Interface**: Connects the appliance to an out-of-band network for communication with the Discovery Console for OT.
    -   **Management Endpoint**: Sets the IP address for the Sensor which it uses to communicate with the Discovery Console for OT.
    -   Management Subnet: Sets the subnet mask/Classless Inter-Domain Routing \(CIDR\) for the appliance communication with the Discovery Console for OT.
    -   \(Optional\) **Management VLAN**: Specifies the VLAN identifier that the management interface uses to tag network communications for participation in VLAN segregated networks.
-   **Span Interface**: When enabled, allows the appliance to collect all network traffic received on the ETHERNET 1 port. This allows the IDS to collect data from the network. When disabled, the appliance can't perform any data collection.
-   **Networks Monitored by Arpwatch**: Lists networks that are being monitored by Arpwatch.
-   **Ethernet Interfaces**: Lists all Ethernet Interfaces for the appliance. The list includes the Interface name and the MAC Address for each one.

## Health

The **Health** tab enables you to view graphs reflecting trends in CPU, memory, disk utilization, and temperature and network input and output over time. You can set the data and time you want the CPU activity to reflect.

## Services

You can configure specific services that run on an appliance. Currently, you can use this feature to enable or disable the SSH service on an appliance. Select the **Edit** button and then select the toggle to turn the SSH service on or off. This setting provides the **Status** and **Updated On** fields for the SSH service. Similarly, you can enable or disable the Log Streaming and Web Management services and view the corresponding **Status** and **Updated On** fields. The SSH service is enabled by default on all Sensors to facilitate post-installation configuration.

## Services Config

The **Services Config** tab includes the **Log Streaming Service**, and the **Web Management Service**. You can use the Log Streaming Service to stream logs from appliances to the Discovery Console for OT. This service also retains logged information for a longer period, which can assist in quicker customer issue resolution.

To set the **Syslog Severity Level** for the Log Streaming Service, select **Edit** and use the drop-down menu to select the severity. You can select the minimum log severity, Informational, to include in the streaming for the appliance. Selecting the Debug level results in the most information being logged.

The data stream isn't viewable in the Console UI. The Console only provides the ability to enable or disable the service and set the log severity level. Streamed log information is retained on the Console for 30 days.

You can use the Web Management feature to reset the Web Management Service password on the appliance. To reset the password, select **Edit**. Enter a password in the **Password** field, enter the same password in the **Confirm Password** field, and then select **Save**. The **Status** and **Updated On** fields provide information about the Web Management Service on the appliance.

## SSH Keys

On this tab, you can add public keys by listing the SSH key name in the **SSH Key Name \(Optional\)** field. You can also select **Paste SSH key\(s\) - one per line** and paste in keys. **Password Authentication** is enabled by default in the initial appliance install. To enable or disable the SSH password authentication, slide the toggle. You can also upload your own SSH Keys. The required format for a key is .pub.

Duplicate keys are automatically removed, so the same SSH key appears only once, even with small formatting differences like extra spaces.

**Note:** As a safety feature that allows continued SSH access, disable **Password Authentication** only if you have uploaded at least one SSH public key to the appliance.

\[Omitted image "appliance-sshkeys-tab.png"\] Alt text: SSH Keys tab

## Sites

The **Sites** tab displays which sites are associated with the selected appliance record during an Auto Query. The Allow/Deny setting indicates whether the appliance is associated with a listed Site. The tab also displays the site name, recommended setting for that site, and the reason for the recommendation. A Deny recommendation means the Site does not appear to be related to the appliance. An Allow recommendation means the Site's network ranges match the Device IP. Select the **Edit** button to change the Allow/Deny settings. Select the **Save Associations** button to save changes or **Cancel** to discard any changes.

\[Omitted image "appliances-site-tab-allowdeny.png"\] Alt text: Sites tab

## Status

This tab shows the current connection status of the appliance, including deployment status for basic configuration, network configuration, arpwatch networks configuration, policy, and firmware updates. Editing these settings is not available.

## Actions button

The **Actions** button in the appliance record enables the following actions.

-   **Deregister**: Deregisters the appliance from the Console. This action resets the network settings to factory defaults and removes the appliance from the Console.
-   **Reboot**: Reboots the appliance.
-   **Remove from Console**: Removes the appliance from the Console.

\[Omitted image "appliance-action-button.png"\] Alt text: Action button


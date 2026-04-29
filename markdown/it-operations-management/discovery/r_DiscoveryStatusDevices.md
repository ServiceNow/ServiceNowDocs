---
title: Discovery device history
description: The Devices Related list in the Discovery Status form provides a summary list of all the devices scanned.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-24"
reading_time_minutes: 4
breadcrumb: [Discovery status, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery device history

The **Devices** Related list in the Discovery Status form provides a summary list of all the devices scanned.

During a Discovery, the list tracks current and completed activity and displays an incremental scan counter. When Discovery is finished for a device, the final disposition is displayed in the Completed activity column. Successful discoveries that result in updated or created configuration items \(CIs\) are highlighted in green. When device history or duplicate IP record is created, the classification\_probe is also populated. To view the log entries for errors \(such as connection failure\) on a specific device, select the **Details** link in the Issues column.

![Discovery device list](../image/discovery_device_list.png "Discovery device list")

Select the IP address of a device in this list for details about that device. The log results for that device are displayed in the list at the bottom of the form.

![Discovery device](../image/DiscoveryDevice.png "Discovery device")

The following fields are available in this form:

|Field|Input value|
|-----|-----------|
|Source|The IP address of the device discovered.|
|Completed activity|Indicates the outcome of Discovery for this device or the last completed activity for a Discovery in progress, such as Identified CI. Successful outcomes are indicated in green.|
|Current activity|The current scanning activity for this device for a Discovery in progress, such as Updating CI.|
|CMDB CI|The name of this device as it appears in the Configuration Management Database \(CMDB\).|
|Started|The number of device-specific probes run. This number does not include the universal probes, Shazzam and Ping, that run initially.|
|Completed|The number of sensor records created from the device-specific probes that were run.|
|Scan status|Shows the final scan count of a completed Discovery or an incremental scan counter for a Discovery in progress. For example, Scan 17 of 19.|
|Issues|Displays the number of issues encountered during Discovery of this device. Select the **Discovery Log** Related list to view these issues.|
|Fields that can be added by configuring the form:|
|DNS Names|Displays DNS names for each discovered device.|

During different phases of Discovery, you may see different values in the **Completed Activity** field on a discovery\_device\_history record.

|Value|When you might see this value|Meaning|
|-----|-----------------------------|-------|
|Common examples|
|Alive, not active, not classified|After Shazzam|Device is responding, but it does not have any open \(active\) ports that we can run classification against.|
|Active|After Shazzam|Device has open \(active\) ports that we potentially can run classification against.|
|Classified|After Classification Probe|We were able to classify the device type and will be proceeding to the Identification stage.|
|Active, couldn’t classify|After Classification Probe|We were unable to classify the device type. Sometimes, this value will also include a reason for why we were unable to classify. For example, Active, couldn't classify: No WMI connection.|
|Created CI|After Identification Probe/Pattern or after Discovery - Device Complete Business Rule runs \(for new CI\)|New CI has been created based on identification results.|
|Identified CI|After Identification Probe/Pattern|Existing CI has been found based on identification results.|
|Identified, ignored extra IP|After Identification Probe/Pattern|Device has already been discovered via a different IP in same Discovery status.|
|Updated CI|After certain Exploration Probes/Patterns or after Discovery - Device Complete Business Rule runs \(for existing CI\)|CI has been updated with additional information.|
|Less common examples|
|Unclassified|After Shazzam \(only for credential-less Discovery and the Discover value on the Discovery Schedule is set to IP Addresses\)|For the credential-less Discovery of the target IP, we were unable to match to an existing CI on the instance.|
|Classified|After Shazzam \(only for credential-less Discovery and the Discover value on the Discovery Schedule is set to IP Addresses\)|For the credential-less Discovery of the target IP, we were able to match to an existing CI on the instance.|
|Active, Windows Cluster VIP|After Windows - Classify|Device is a Windows Cluster VIP and will be updated as such.|
|Classified, but not disabled|After Classification Probe|We made a match to a Classifier type, but the classifier itself is disabled.|
|Classified, couldn't identify|After Identification Probe/Pattern|Couldn’t create or match to existing CI record.|
|Identified, not updating CI|After Identification Probe/Pattern|We were able to properly identify a CI record, but we are choosing not to update the CI.|

Any device that includes the following classes or one of its child classes will be displayed in the Discovery device history table.

-   Computer \[cmdb\_ci\_computer\]
-   Network Gear \[cmdb\_ci\_netgear\]
-   PDU \[cmdb\_ci\_pdu\]
-   Printer \[cmdb\_ci\_printer\]
-   UPS \[cmdb\_ci\_ups\]

If there were issues, or if Discovery failed to complete, select the **Details** link to view the log records for the issue. The failure of any probe is considered an issue, even if the device was eventually classified properly and updated in the CMDB.

![Discovery details about a device](../image/DiscoveryDetails.png "Discovery details about a device")

## Address scan data

When Discovery scans for IP addresses only \(without credentials or [identifiers](../concept/c_DiscoveryIdentifiers.md)\), no updates are made to the CMDB. All IP addresses discovered appear on this list, including multiple IPs on the same device. The results of IP address scans include slightly different information than the results of a CI scan. Since there is no CMDB activity associated with the IP address scan, the Completed activity column displays only the classification status.

Possible statuses are:

-   Classified
-   Unclassified
-   Alive, not classified

For Classified devices, Discovery might identify the type of device in the Current activity column. For example, Network Gear might be classified as Cisco Network Gear, and a Computer might be classified as a Windows Computer.

**Parent Topic:**[Discovery status](../concept/c_DiscoveryStatus.md)


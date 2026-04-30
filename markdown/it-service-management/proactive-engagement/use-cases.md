---
title: Proactive Engagement use cases
description: This section lists some of the most common use cases in Proactive Engagement that are designed for seamless implementation and quick results. You can deploy these use cases that are tailored to some of the common challenges seen as required by your organization to meet your specific needs.
locale: en-US
release: xanadu
product: Proactive Engagement
classification: proactive-engagement
topic_type: reference
last_updated: "2024-10-14"
reading_time_minutes: 2
breadcrumb: [Proactive Engagement reference, Proactive Engagement, IT Service Management]
---

# Proactive Engagement use cases

This section lists some of the most common use cases in Proactive Engagement that are designed for seamless implementation and quick results. You can deploy these use cases that are tailored to some of the common challenges seen as required by your organization to meet your specific needs.

<table id="table_c4x_v3l_xbc"><thead><tr><th>

`Use case name`

</th><th>

Description

</th><th>

Symptom

</th><th>

Configuration details

</th><th>

Resolution

</th></tr></thead><tbody><tr><td>

`Low disk space - Disk cleanup using windows disk clean-up`

</td><td>

The slow performance of the system is due to insufficient disk space. It can be resolved by freeing up disk space and restoring optimal system performance through **Windows Disk Cleanup** as a remedial action.

</td><td>

-   Low performance
-   Unable to install system updates

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**: Device disk space is greater than the set threshold.
-   **OS**: Windows

</td><td>

Clearing unwanted files/cache using windows disk cleanup-   Internet cache files
-   System error memory dump files
-   System error mini-dump files
-   Temporary files
-   Windows error reporting

</td></tr><tr><td>

`Low disk space - self-help instructions to clean up disk space`

</td><td>

The slow performance of the system is due to insufficient disk space. It can be resolved by freeing up disk space and restoring optimal system performance through self-help instructions to clean up disk space

</td><td>

-   Low performance
-   Unable to install system updates

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**: Device disk space is greater than the set threshold.
-   **OS**: Mac

</td><td>

Provide end users with self-help instructions to clean up disk space.

</td></tr><tr><td>

`Poor battery health - Catalog request for battery replacement`

</td><td>

The battery performance is low due to a deteriorated battery. This issue can be resolved by raising a battery replacement request with the user consent.

</td><td>

-   Fast discharge of the device battery and poor charging rate.
-   Overheating of the device

</td><td>

-   **Configuration Type**: Flow
-   **Threshold condition**: Battery health status is poor.
-   **OS**: Mac and Windows

</td><td>

Submit a catalog request to replace the deteriorated battery.

</td></tr><tr><td>

`System reboot - Notification to remind system reboot`

</td><td>

Notify the user of a required system reboot which is pending over a time period.Device not being rebooted for a long time, causing pending installations to be stalled or applications to run improperly in the background.

</td><td>

-   Slow system performance
-   incomplete software updates

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**: System up-time is greater than the set threshold.
-   **OS**: Mac and Windows

</td><td>

Notify the end user to reboot their device.

</td></tr><tr><td>

`Disconnected Zscaler - Self-help instructions to connect to Zscaler.`

</td><td>

Alert users when the VPN connection remains disconnected for an extended period.To confirm secure access to organization resources and maintain security compliance.

These instructions work for any installed VPN application.

</td><td>

Inability to access any application in a secure, private network.

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**: Zscaler is disabled.
-   **OS**: Windows

</td><td>

Provide end users with self-help instructions to reconnect to Zscaler.

</td></tr></tbody>
</table>**Parent Topic:**[Proactive Engagement reference](../proactive-engagement-reference.md)


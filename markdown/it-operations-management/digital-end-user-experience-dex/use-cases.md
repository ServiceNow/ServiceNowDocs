---
title: Proactive Engagement use cases
description: Proactive Engagement provides predefined use cases for common digital experience issues. Deploy the use cases that address the challenges in your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/use-cases.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Reference, Reference, Digital End-User Experience, IT Operations Management]
---

# Proactive Engagement use cases

Proactive Engagement provides predefined use cases for common digital experience issues. Deploy the use cases that address the challenges in your organization.

<table id="table_c4x_v3l_xbc"><thead><tr><th>

Use case name

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

The slow performance of the system is due to insufficient disk space. It can be resolved by freeing up disk space and restoring optimal system performance through Windows Disk Cleanup as a remedial action.

</td><td>

-   Low performance
-   Unable to install system updates

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**: Device disk space is greater than the set threshold.
-   **OS**: Windows

</td><td>

Clearing unwanted files and cache by using Windows Disk Cleanup-   Internet cache files
-   System error memory dump files
-   System error mini-dump files
-   Temporary files
-   Windows error reporting

</td></tr><tr><td>

`Low disk space - self-help instructions to clean up disk space`

</td><td>

The slow performance of the system is due to insufficient disk space. It can be resolved by freeing up disk space and restoring optimal system performance through self-help instructions to clean up disk space.

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

The battery performance is low due to a deteriorated battery. This issue can be resolved by raising a battery replacement request with the user's consent.

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

Notify the user of a required system reboot that has been pending for a period of time.The device hasn't been rebooted for a long time, which causes pending installations to stall or applications to run improperly in the background.

</td><td>

-   Slow system performance
-   Incomplete software updates

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**: System uptime is greater than the set threshold.
-   **OS**: Mac and Windows

</td><td>

Notify the end user to reboot their device.

</td></tr><tr><td>

`Disconnected Zscaler - Self-help instructions to connect to Zscaler`

</td><td>

Alert users when the VPN connection remains disconnected for an extended period.This alert helps confirm secure access to organization resources and maintain security compliance.

These instructions work for any installed or cloud VPN application.

-   Windows - any installed VPN solution
-   Mac - any installed or cloud VPN solution

</td><td>

Inability to access any application in a secure, private network.

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**: Zscaler is inactive.
-   **OS**: Mac and Windows

</td><td>

Provide end users with self-help instructions to reconnect to Zscaler.

</td></tr><tr><td>

`Zoom freeze`

</td><td>

Alert the users when the number of application freezes is greater than the set threshold. This can be resolved by clearing the application cache and reinstalling the application.

</td><td>

Application freeze

</td><td>

-   **Configuration Type**: Remedial action
-   **Threshold condition**:
-   **OS**: Mac and Windows

</td><td>

Clear app cache and restart the app.

</td></tr><tr><td>

`Google chrome freeze`

</td><td>

Alert the users when the number of application freezes is greater than the set threshold. This can be resolved by clearing the application cache and reinstalling the application.

</td><td>

Application freeze

</td><td>

-   **Configuration Type**: Remedial action
-   **Threshold condition**:
-   **OS**: Mac

</td><td>

Clear app cache and restart the app.

</td></tr><tr><td>

`Microsoft classic Teams freeze`

</td><td>

Alert the users when the number of application freezes is greater than the set threshold. This can be resolved by clearing the application cache and reinstalling the application.

</td><td>

Application freeze

</td><td>

-   **Configuration Type**: Remedial action
-   **Threshold condition**:
-   **OS**: Mac

</td><td>

Clear app cache and restart the app.

</td></tr><tr><td>

``Microsoft Teams freeze``

</td><td>

Alert the users when the number of application freezes is greater than the set threshold. This can be resolved by clearing the application cache and reinstalling the application.

</td><td>

Application freeze

</td><td>

-   **Configuration Type**: Remedial action
-   **Threshold condition**:
-   **OS**: Windows

</td><td>

Clear app cache and restart the app.

</td></tr><tr><td>

`Microsoft Outlook freeze`

</td><td>

Alert the users when the number of application freezes is greater than the set threshold. This can be resolved by clearing the application cache and reinstalling the application.

</td><td>

Application freeze

</td><td>

-   **Configuration Type**: Remedial action
-   **Threshold condition**:
-   **OS**: Windows

</td><td>

Clear app cache and restart the app.

</td></tr><tr><td>

`Microsoft Teams crash`

</td><td>

Alert the users when the number of application crashes is greater than the set threshold. This can be resolved by reinstalling/updating the application.

</td><td>

Application crash

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**: Microsoft Teams crashes multiple times.
-   **OS**: Mac

</td><td>

Reinstall or update to the latest version of Microsoft Teams by using the "execute Jamf policy" remedial action with the corresponding policy ID.

</td></tr><tr><td>

`Microsoft Outlook crash`

</td><td>

Alert the users when the number of application crashes is greater than the set threshold. This can be resolved by reinstalling/updating the application.

</td><td>

Application crash

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**: Microsoft Outlook crashes multiple times.
-   **OS**: Mac

</td><td>

Reinstall or update to the latest version of Microsoft Outlook by using the "execute Jamf policy" remedial action with the corresponding policy ID.

</td></tr><tr><td>

`Zoom crash`

</td><td>

Alert the users when the number of application crashes is greater than the set threshold. This can be resolved by reinstalling/updating the application.

</td><td>

Application crash

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**: Zoom crashes multiple times.
-   **OS**: Mac

</td><td>

Reinstall or update to the latest version of Zoom by using the "execute Jamf policy" remedial action with the corresponding policy ID.

</td></tr><tr><td>

`Microsoft Teams crash`

</td><td>

Alert the users when the number of application crashes is greater than the set threshold. This can be resolved by reinstalling/updating the application.

</td><td>

Application crash

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**: Microsoft Teams crashes multiple times.
-   **OS**: Mac

</td><td>

Provide self-help instructions to the end user to reinstall or update to the latest version of Microsoft Teams.

</td></tr><tr><td>

`Microsoft Outlook crash`

</td><td>

Alert the users when the number of application crashes is greater than the set threshold. This can be resolved by reinstalling/updating the application.

</td><td>

Application crash

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**: Microsoft Outlook crashes multiple times.
-   **OS**: Mac

</td><td>

Provide self-help instructions to the end user to reinstall or update to the latest version of Microsoft Outlook.

</td></tr><tr><td>

`Zoom crash`

</td><td>

Alert the users when the number of application crashes is greater than the set threshold. This can be resolved by reinstalling/updating the application.

</td><td>

Application crash

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**: Zoom crashes multiple times.
-   **OS**: Mac

</td><td>

Provide self-help instructions to the end user to reinstall or update to the latest version of Zoom.

</td></tr><tr><td>

`Poor wifi connectivity`

</td><td>

Alert the user if the Wi-Fi signal strength remains poor for an extended period.

</td><td>

-   Poor browsing experience.
-   Frequent buffering on web or SaaS applications.

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**:

    -   Mac - Wi-Fi RSSI value
    -   Windows - Wi-Fi signal strength
Internet or Wi-Fi is slow for an extended period.

-   **OS**: Mac and Windows

</td><td>

Alert the user to move closer to the Wi-Fi router.

</td></tr><tr><td>

`Device Crash`

</td><td>

Alert users when the number of device crashes is greater than the set threshold. This issue can be resolved by updating the OS and device drivers and uninstalling unnecessary applications.

</td><td>

Device crash

</td><td>

-   **Configuration Type**: Metric rule
-   **Threshold condition**: Device crashes multiple times.
-   **OS**: Mac and Windows

</td><td>

Provide self-help instructions to the end user to update their OS and device drivers and to uninstall unnecessary applications to help prevent device crashes.

</td></tr></tbody>
</table>
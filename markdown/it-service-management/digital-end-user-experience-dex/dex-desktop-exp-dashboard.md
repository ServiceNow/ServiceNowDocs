---
title: Desktop Assistant usage metrics
description: Usage metrics dashboard enables you to monitor the connection status of your device, user login status, application version, and the number of incidents created using the Desktop Assistant application, ensuring smooth communication with the ServiceNow instance.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [DEX Desktop Assistant reference, Reference, Digital End-User Experience, IT Service Management]
---

# Desktop Assistant usage metrics

Usage metrics dashboard enables you to monitor the connection status of your device, user login status, application version, and the number of incidents created using the Desktop Assistant application, ensuring smooth communication with the ServiceNow instance.

<table id="table_hqf_5xk_1xb"><thead><tr><th>

Cards

</th><th>

Description

</th><th>

Source table

</th></tr></thead><tbody><tr><td>

Connection Status

</td><td>

Shows whether the device is connected to a ServiceNow instance.

 **Note:** If a user remains inactive for 6 hours, their connection status is considered as "down", even if they're still logged in but not active.

 This information helps you troubleshoot connectivity issues and make sure that the device is able to access the resources it needs.

</td><td>

DEX Desktop Assistant\[sn\_dex\_desktop\_exp\]

</td></tr><tr><td>

Logged in

</td><td>

Indicates whether a user is logged in to the device or not. The login status of a user is updated when they either log in or log out.

 This information helps you determine whether the device is in use or not and track user activity over time.

</td><td>

DEX Desktop Assistant\[sn\_dex\_desktop\_exp\]

</td></tr><tr><td>

Desktop Assistant Version in use

</td><td>

Displays the current version of Desktop Assistant running on user devices.

 This information can help you confirm that the application is up to date and identify any potential compatibility issues with the OS or other applications.

</td><td>

DEX Desktop Assistant\[sn\_dex\_desktop\_exp\]

</td></tr></tbody>
</table>To return to the usage metrics page or the administration page, where you can access usage metrics, see [View Desktop Assistant usage metrics](../task/view-da-usage-metrics.md) or [DEX Administration](../concept/dex-workspace-administration-tab.md).

**Parent Topic:**[DEX Desktop Assistant reference](dex-desktop-experience-reference.md)


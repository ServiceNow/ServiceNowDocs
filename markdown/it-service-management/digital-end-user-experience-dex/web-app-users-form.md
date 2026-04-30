---
title: Web application — Devices page
description: The Active and Impacted devices list captures data about the devices, latest logged-in user, last logged in location, and time when the application was last accessed on the device. This information helps with security, access control, and provides insights into user behavior and application usage.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Applications list, DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Web application — Devices page

The Active and Impacted devices list captures data about the devices, latest logged-in user, last logged in location, and time when the application was last accessed on the device. This information helps with security, access control, and provides insights into user behavior and application usage.

<table id="table_lsb_btf_4wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Active or Impacted device that is connected to DEX.

</td></tr><tr><td>

Last logged-in user

</td><td>

Last logged-in user that accessed the device.

</td></tr><tr><td>

Last logged in location

</td><td>

The geographical position or physical location of the device where the application was recently accessed.**Note:** The device location is important in an outage or emergency situation when it’s important to be able to locate impacted devices and users to assist. Device location data can be used to identify the extent and severity of the outage, prioritize restoration efforts, and direct resources to the affected areas.

</td></tr><tr><td>

App last accessed

</td><td>

Date and time when the application was last accessed on the device.Only Active devices page has this field.

</td></tr><tr><td>

Alerts

</td><td>

This field represents the number of active alerts for the application on the device.Only Impacted devices page has this field.

**Note:** Select the alert count column to access the device alerts page.

</td></tr></tbody>
</table>**Note:**

-   The Active devices list displays the Agent Client Collector \(ACC\) installed on their devices.
-   By default, sorting is available only on the Impacted devices page and displays all devices on with ACC is installed for the latest 1000 records.
-   The list displays active devices and refreshes every five minutes, a maximum of 1000 devices listed. If no new data is available, the last available data is displayed.
-   Only device name filter is available on web applications.

**Parent Topic:**[Applications list](application-form.md)


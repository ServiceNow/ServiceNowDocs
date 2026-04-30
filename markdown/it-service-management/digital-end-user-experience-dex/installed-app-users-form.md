---
title: Installed application — Devices page
description: The devices lists capture data regarding the active devices, impacted devices, the last logged-in user, and the last logged-in location, and the date and time when the application was last accessed on the device. This information helps with security and access control, as well as providing insights into user behavior and application usage.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Applications list, DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Installed application — Devices page

The devices lists capture data regarding the active devices, impacted devices, the last logged-in user, and the last logged-in location, and the date and time when the application was last accessed on the device. This information helps with security and access control, as well as providing insights into user behavior and application usage.

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

Location of the device that the user most recently used.**Note:** The device location is important in an outage or emergency situation when it’s important to be able to locate impacted devices and users to assist. Device location data can be used to identify the extent and severity of the outage, prioritize restoration efforts, and direct resources to the affected areas.

</td></tr><tr><td>

App last accessed

</td><td>

Date and time when the application was last accessed by the device.Only Active devices page has this field.

**Note:** The **App last accessed** field displays the date and time when the application was last accessed on the device.

</td></tr></tbody>
</table>**Note:**

-   Both device name filter and app version filter are available on installed applications. This allows us to search all the devices listed in the *dex\_device* table.
-   The app versions drop-down allows us to search for all the versions present in the *dex\_application\_version* table.
-   The All Devices table lists devices where the app was accessed at least once \(for Windows\) and have the application installed \(for macOS\). This data refreshes every 24 hours.
-   There can be multiple records for a device if it has multiple versions of the same application.

<table id="table_bmv_2dk_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Device

</td><td>

Active or Impacted device that is connected to DEX.

</td></tr><tr><td>

Last logged-in user

</td><td>

Last logged-in user that accessed the device.

</td></tr><tr><td>

Last logged in location

</td><td>

Location of the device that the user most recently used.**Note:** The device location is important in an outage or emergency situation when it’s important to be able to locate impacted devices and users to assist. Device location data can be used to identify the extent and severity of the outage, prioritize restoration efforts, and direct resources to the affected areas.

</td></tr><tr><td>

App last accessed

</td><td>

Date and time when the application was last accessed by the device.Only Active devices page has this field.

**Note:** The **App last accessed** field displays the date and time when the application was last accessed on the device.

</td></tr><tr><td>

Alerts

</td><td>

This field represents the number of active alerts for the application on the device.Only Impacted devices page has this field.

**Note:** Select the alert count column to access the device alerts page.

</td></tr></tbody>
</table>**Note:**

-   The Active devices list displays the Agent Client Collector \(ACC\) installed on their devices.
-   By default, sorting is available only on the Impacted devices page and displays all devices on with ACC is installed for the latest 1000 records.
-   The list displays active devices and refreshes every 5 minutes, a maximum of 1000 devices are listed. If no new data is available, the last available data is displayed.

Selecting the user name takes you to the details page of that user. For detailed information on a user and associated applications, see [Device details](../concept/dex-workspace-user-details.md).

**Parent Topic:**[Applications list](application-form.md)


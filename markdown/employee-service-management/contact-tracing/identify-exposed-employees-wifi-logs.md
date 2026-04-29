---
title: Use Wi-Fi access logs from Mist Systems
description: Identify potentially exposed employees using Wi-Fi access logs from Mist Systems.
locale: en-US
release: australia
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Retrieving Wi-Fi access log data, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Use Wi-Fi access logs from Mist Systems

Identify potentially exposed employees using Wi-Fi access logs from Mist Systems.

## Before you begin

Role required: sn\_imt\_tracing.wifi\_admin

## About this task

ServiceNow Contact Tracing integrates with an external application, Mist Systems, to collect and process Wi-Fi access logs for organizations. To leverage access logs from Mist Systems, you must have Mist access points installed at your workplace.

## Procedure

1.  Set up the Contact Tracing Wi-Fi properties.

    -   By default, the asset data is available in the Computer table \[cmdb\_ci\_computer\]. If you are using a different table, specify it using the **sn\_imt\_tracing.wifi\_client\_table** property.
    -   Ensure that the MAC address is populated in the **mac\_address** field in the table that has the asset data.
    For more information, see [System properties for tracing systems in Emergency Exposure Management](../../business-continuity/reference/list-of-tracing-system-sys-properties.md).

2.  Set up the Contact Tracing BLE properties.

    -   By default, the asset data is available in the Wearable Technology \[cmdb\_ci\_wearable\] table. If you are using a different table, specify it using the **sn\_imt\_tracing.wifi\_ble\_client\_table** property.
    -   Ensure that the MAC address is populated in the **mac\_address** field in the table that has the asset data.
    **Note:** The Wearable Technology \[cmdb\_ci\_wearable\] table is installed with the CMDB CI Class Models application available on ServiceNow Store. For more information, see [CMDB CI Class Models](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-iot&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

    For more information on adding BLE-enabled devices or other wearable devices, see [Add wearable devices assigned to employees](add-wearable-devices.md).

3.  Set up an organization and load sites.

    For more information, see [Set up an organization and load sites](set-up-organization.md).

4.  Indicate that the diagnostic data should be accessed from Mist Systems.

    1.  Navigate to **Contact Tracing** &gt; **Wi-Fi Access Management** &gt; **Wi-Fi Diagnostic Preferences**.

    2.  Click **Generate Location Preferences**.

    3.  In the Generate Location Preferences window, select **Use Mist Integration** from the list.

    4.  Click **OK**.

    The access log data for all locations will be taken from Mist Systems access log files.

5.  If you want to use manually loaded access logs rather than Mist Systems logs for a specific location, create a separate location assignment.

    1.  Click **New**.

    2.  Specify the location for which you want to set the diagnostic preference.

    3.  Set the **Preference** value to **Use Manual Load**.

    4.  Click **Submit**.

6.  Run the diagnostic request.

    1.  Select the **Use Wi-Fi access log** check box.

    2.  Specify the start date and end date.

    3.  Click **Run Diagnostics**.

    For more information about how to run a diagnostic request, see [Run a diagnostic request](../../business-continuity/task/use-emergency-exposure-mgnt.md).


## Result

Mist Systems identifies the MAC addresses of the affected user for the specified start date and end date. The MAC addresses identify the zones visited by the affected employee. Potentially exposed employees who visited those zones are identified and displayed in the related list of the diagnostic request.

**Parent Topic:**[Retrieving Wi-Fi access log data](../concept/wifi-access-management.md)


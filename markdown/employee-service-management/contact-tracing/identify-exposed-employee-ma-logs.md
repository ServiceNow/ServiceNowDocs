---
title: Use imported Wi-Fi access logs
description: Identify potentially exposed employees by manually importing Wi-Fi access logs into the Wi-Fi Access Register table.
locale: en-US
release: yokohama
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Retrieving Wi-Fi access log data, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Use imported Wi-Fi access logs

Identify potentially exposed employees by manually importing Wi-Fi access logs into the Wi-Fi Access Register table.

## Before you begin

Role required: sn\_imt\_tracing.wifi\_admin

## Procedure

1.  Set up the Contact Tracing Wi-Fi properties.

    By default, the asset data is available in the Computer table \[cmdb\_ci\_computer\]. If you are using a different table, specify it using the **sn\_imt\_tracing.wifi\_client\_table** property.

    For more information, see [System properties for tracing systems in Emergency Exposure Management](../../business-continuity/reference/list-of-tracing-system-sys-properties.md).

2.  Indicate that the diagnostic data should be accessed from manually loaded access logs.

    1.  Navigate to **Contact Tracing** &gt; **Wi-Fi Access Management** &gt; **Wi-Fi Diagnostic Preferences**.

    2.  Click **Generate Location Preferences**.

    3.  In the Generate Location Preferences window, select **Use Manual Load** from the list.

    4.  Click **OK**.

    The access log data for all locations will be taken from manually loaded access logs.

3.  If you want to use Mist Systems access logs rather than manually loaded logs for a specific location, create a separate location assignment.

    1.  Click **New**.

    2.  Specify the location for which you want to set the diagnostic preference.

    3.  Set the **Preference** value to **Use Mist Integration**.

    4.  Click **Submit**.

4.  Import Wi-Fi access logs into the Wi-Fi Access Register table \[sn\_imt\_tracing\_wifi\_access\_register\] using an Excel spreadsheet.

    For more information, see [Import your Wi-Fi access logs spreadsheet](import-wifi-data.md).

5.  Run the diagnostic request.

    1.  Select the **Use Wi-Fi access log** check box.

    2.  Specify the start date and end date.

    3.  Click **Run Diagnostics**.

    For more information about how to run a diagnostic request, see [Run a diagnostic request](../../business-continuity/task/use-emergency-exposure-mgnt.md).


## Result

Potentially exposed employees are displayed in the related list of the diagnostic request.

**Parent Topic:**[Retrieving Wi-Fi access log data](../concept/wifi-access-management.md)


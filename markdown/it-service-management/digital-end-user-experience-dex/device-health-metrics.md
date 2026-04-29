---
title: Reviewing device health metrics in incident investigation with DEX
description: View the overall health and related metrics for Digital End-User Experience \(DEX\) monitored devices as part of incident investigation with DEX.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Incident diagnostics and suggested resolutions, DEX for service desk agents, Digital End-User Experience, IT Service Management]
---

# Reviewing device health metrics in incident investigation with DEX

View the overall health and related metrics for Digital End-User Experience \(DEX\) monitored devices as part of incident investigation with DEX.

The Device health section shows device and application performance classified as Good, Average, or Poor based on corresponding device health categories.

-   Device performance: Overall health and performance of the device.
-   Network stability: Performance and consistency of the network connection.
-   Security status: Security or protection level of the device.
-   Application performance: Performance of installed and web applications on the device.

## Device health checklist

The Device health checklist shows detailed performance data for device and application metrics. You can view data for the following durations through the **Show** drop-down list:

-   Latest available data
-   Last 24 hours
-   Last 7 days
-   Custom duration by selecting the start and end dates within the last seven days

By default, the latest available data is displayed.

A checklist shows basic device and application health metrics. You can display advanced metrics by toggling the **Show additional metrics** option.

**Note:** Metrics displayed in the Device health check list are included in the base system metric list. As a DEX administrator, you can customize the base system metrics. For more information, see [Customize metric definitions](../../dex-score/task/dexscr-customize-dex-score-metric-defs.md).

Selecting **View detailed device health** displays the Device details page. For more information, see [Device details pages](../reference/user-device-details-pages.md).

## Device metrics

The Device metrics section shows information about device, network, and security metrics. This section displays the following information:

-   Overview information like last access time, memory usage details, users logged in, and last Blue Screen of Death \(BSOD\) occurrence and cause, if applicable.
-   Device performance metric details like CPU, disk, and memory usage percentages, device up time, number of device crashes, and reboot duration.
-   Network metric details like WiFi RSSI value and transmission rate.
-   Device security metrics like firewall and antivirus status.

## Application metrics

The Application metrics section shows information related to application status and metric details. From the drop-down list, select the application you want to monitor for performance.

This section displays the following information:

-   Overview information like the application type \(installed or web\), application status and usage time, version number, and last access time.
-   Application performance metric details like CPU and memory usage percentages, number of crashes and freezes, and average page load and response times.


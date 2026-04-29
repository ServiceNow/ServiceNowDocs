---
title: Availability
description: The Availability section shows instance level availability on a geographic map and instance level ServiceNow generated alerts \(limited alert types\) since the past 7 days.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Instance Observer, Platform Health, Using Impact, Impact]
---

# Availability

The Availability section shows instance level availability on a geographic map and instance level ServiceNow generated alerts \(limited alert types\) since the past 7 days.

## Instance Availability

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Monitor** &gt; **Go to Instance Observer**.
2.  Select **Availability** tab and click **Instance Availability** value.
3.  Select an instance in the **Instance** field and click **Get Snapshot** to view the instance availability in a geographical map.

    The map plots and highlights the primary and standby data centers by Geo location together with the ServiceNow footprint \(all other data center locations\). The color of the plot determines the current availability:

    -   green = available
    -   red = unavailable
    based on an active Instance Up/Down alert.

    **Note:** All alerts generated for your instance are consolidated and listed in the Alert Console. To monitor the alerts, navigate to **Alerts** &gt; **Alert Console** and filter the **Alert Type** column with the value **Monitoring** to see the instance's Up/Down time.

    ![Instance up or down time filtered by Monitoring alert type.](../image/monitoring-alerts-up-down.png)

    ![Instance availability in a geographical map.](../image/io-instance-availability.png "Instance availability in a geographical map")

4.  Select **Detailed Instance Availability** to navigate to the Instances Dashboard

## Known Issues

A problem or defect of an instance that requires proactive mitigation is listed in the **Known Issues** tab of the **Availability** section.

-   **[Cloud availability](../reference/cloud-availability.md)**  
Check specific ServiceNow data center availability, service degradation, or for interruption.

**Parent Topic:**[Instance Observer](io-overview.md)


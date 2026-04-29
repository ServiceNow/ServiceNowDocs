---
title: Filter results for Host Status
description: Filter your query results by Host Status. Verify whether devices were reachable when the query was executed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Results page, Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Filter results for Host Status

Filter your query results by Host Status. Verify whether devices were reachable when the query was executed.

## Before you begin

Role required: admin

## About this task

In the Scan Results filtering types, the **Host Status** enables users to view scan results based on whether the scanned host was **Up** or **Down**. This filter is derived from the **Nmap XML status field** inside the Raw scan output.

![Select Host Status](../images/host-status-filter.png)

**Note:** This filter is based on raw scan output and does not depend on scan type. If a scan output does not contain a host `status state="up|down"` field, it does not match the Host Status filter.

Using the Host Status filter helps to quickly narrow results such as:

-   showing only reachable devices \(Up\) to review open ports or services.
-   showing only unreachable devices \(Down\) to troubleshoot network issues, firewall rules, wrong IPs, or powered-off devices.

Raw data is useful for debugging and verification for these reasons:

-   Raw data confirms why a host was marked Up or Down.
-   Raw data shows what the Nmap actually returned.
-   Raw data helps validate scripts when scan parsing or mapping doesn’t show expected information.

**Note:** You cannot export RAW XML results if your Console license is invalid \(absent or expired\).

## Procedure

1.  Navigate to the Results page.

2.  In the Filter panel, select the plus icon. ![](../images/filter-plus-icon.png)

    The **Select Filter Type** field opens.

    ![Select to add filter](../images/add-filter.png)

3.  Select inside the filter and select Host Status from the drop-down menu.

    The **Select Host Status** field opens.

4.  Select from the pop-up choices one of the following.

    **Note:** **Up/Down** in this instance means the **host status from the scan result \(Nmap\)** for that IP during that scan run.

    -   **Up** means the target device responded, that is, the scanner was able to reach it and also got a response back.
    -   **Down** means the target device did not respond; this could mean it is offline, blocked by firewall, unreachable, or it did not respond.
    ![Choose either Up or Down](../images/filter-host-status-up-down.png)

5.  Using the Host Status filter helps to quickly narrow results:

    -   Showing only **reachable devices** \(Up\) to review open ports/services.
    -   Showing only **unreachable devices** \(Down\) to troubleshoot network issues, firewall rules, wrong IPs, or powered-off devices.
6.  Raw data is useful for debugging and verification because:

    -   Raw data confirms why a host was marked Up/Down \(reason field\).
    -   Raw data shows what Nmap actually returned \(good for support/investigations\).
    -   Raw data helps validate scripts when scanning/mapping doesn’t show expected information.


---
title: Filter results for Host Status
description: Filter your query results by Host Status. Verify whether devices were reachable when the query was executed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/results-filter-host-status.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Results page, Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Filter results for Host Status

Filter your query results by Host Status. Verify whether devices were reachable when the query was executed.

## Before you begin

Role required: admin

## About this task

In the Scan Results filtering types, the **Host Status** enables users to view query results based on whether the queried host was **Up** or **Down**. This filter is derived from the **Nmap XML status field** inside the Raw scan output.

\[Omitted image "host-status-filter.png"\] Alt text: Select Host Status

**Note:** This filter is based on raw scan output and does not depend on scan type. If a scan output does not contain a host `status state="up|down"` field, it does not match the Host Status filter.

Using the Host Status filter helps to quickly narrow results such as:

-   shows only reachable devices \(Up\) to review open ports or services.
-   shows only unreachable devices \(Down\) to troubleshoot network issues, firewall rules, wrong IPs, or powered-off devices.

Raw data is useful for debugging and verification because:

-   Reason field: Raw data confirms why a host was marked Up/Down.
-   Good for investigation: Raw data shows what the Nmap actually returned.
-   Script validation: Raw data helps validate scripts when scan parsing or mapping doesn’t show expected information.

## Procedure

1.  Navigate to the Results page.

2.  In the Filter panel, select the plus icon. \[Omitted image "filter-plus-icon.png"\] Alt text:

    The **Select Filter Type** field opens.

    \[Omitted image "add-filter.png"\] Alt text: Select to add filter

3.  In the Filter field, select Host Status from the drop-down menu.

    The **Select Host Status** field opens.

4.  Select from the pop-up choices one of the following.

    **Note:** **Up/Down** in this instance means the **host status from the scan result \(Nmap\)** for that IP during that query run.

    -   **Up** means the target asset responded, that is, the appliance was able to reach it and also got a response back.
    -   **Down** means the target asset did not respond; this could mean it is offline, blocked by firewall, unreachable, or it did not respond.
    \[Omitted image "filter-host-status-up-down.png"\] Alt text: Choose either Up or Down

5.  Using the Host Status filter helps to quickly narrow results:

    -   Showing only **reachable assets** \(Up\) to review open ports/services.
    -   Showing only **unreachable assets** \(Down\) to troubleshoot network issues, firewall rules, wrong IPs, or powered-off devices.
6.  Raw data is useful for debugging and verification because:

    -   Raw data confirms why a host was marked Up/Down \(reason field\).
    -   Raw data shows what Nmap actually returned \(good for support/investigations\).
    -   Raw data helps validate scripts when querying/mapping doesn’t show expected information.


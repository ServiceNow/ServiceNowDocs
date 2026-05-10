---
title: Operational Technology Vulnerability Response \(PA\) dashboard collection jobs
description: The Operational Technology Vulnerability Response \(PA\) dashboard uses collection jobs to collect the data that is shown on the dashboard.
locale: en-US
release: australia
product: Industrial Workspace
classification: industrial-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Industrial Workspace, Operational Technology]
---

# Operational Technology Vulnerability Response \(PA\) dashboard collection jobs

The Operational Technology Vulnerability Response \(PA\) dashboard uses collection jobs to collect the data that is shown on the dashboard.

The following collection jobs collect the data that is shown on the Operational Technology Vulnerability Response \(PA\) dashboard:

-   **\[PA OT VR\] Historical Vulnerability Data Collection**

    Collection job for the historical data of existing records.

    **Note:** The Historical Vulnerability Data Collection is an on-demand job that you only need to execute once. After the historical data is collected, the daily data collection jobs run on a scheduled time every day. For more information, see [Collect historical data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/t_RunHistoricalDataCollection.md).

-   **\[PA OT VR\] Daily Collection for Remediation Tasks**

    Collection job for the remediation task data that occurs daily.

-   **\[PA OT VR\] Daily Collection for Vulnerable Items 1**

    Collection job that occurs daily for non-deferred overdue critical vulnerable items, deferred vulnerable items, vulnerable items, and critical vulnerable items.

-   **\[PA OT VR\] Daily Collection for Vulnerable Items 2**

    Collection job that occurs daily for unassigned vulnerable items, closed vulnerable items, summed duration of closed vulnerable items, and critical deferred vulnerable items.


**Parent Topic:**[Using the Industrial Workspace](../../operational-technology-management/concept/using-industrial-workspace.md)


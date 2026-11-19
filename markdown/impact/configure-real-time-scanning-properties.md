---
title: Configure real-time scanning properties
description: Real-time scanning properties allow control over which users have access to real-time scanning, and how the scan operates within their environment. Perform the following procedure to configure real time scanning properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/configure-real-time-scanning-properties.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Scan Engine properties, Activate Scan Engine and review settings, Run Impact Guided Setup, Configuring Impact, Impact]
---

# Configure real-time scanning properties

Real-time scanning properties allow control over which users have access to real-time scanning, and how the scan operates within their environment. Perform the following procedure to configure real time scanning properties.

## Before you begin

-   The application scope is set to a scope that is not part of the Scan Engine project. When the scope is set to Scan Engine real-time scanning doesn't activate
-   The tables that you want to scan have active entries in the sn\_se\_applicable\_table table.
-   The tables that you want to scan aren't listed in the **excluded\_tables** property. on the Real Time Scanning properties tab.
-   The **read\_access** attribute of the sys\_update\_version table is set to true. If it is not, the Scan Engine disables itself.

Role required: Scan Engine Admin \(`sn_se.scan_engine_admin`\) or admin.

## Procedure

1.  Navigate to **ALL &gt; Impact &gt; Configuration &gt; Scan Engine Properties**.

2.  On the Real Time Scanning tab, select the **Enforce real time validation** checkbox to activate real-time scanning.

3.  In the Real time message visibility drop-down, select who will see real-time scanning results:

    -   All users: All users in Impact can access real-time messages.
    -   Only users with the scan\_engine\_user role: LImited to users with the assigned role to view real-time messages.

    Users designated in **Real Time Message Visibility** will be required to correct findings at the Error or Warning level before saving the form. Approved exception requests for Recommend level findings can bypass this requirement.

4.  Select whether to **Exclude suggestion finding**, which hides Suggestion level findings from real-time display, showing only Review, Warning, and Error levels.

    The Excluded tables area lists which tables are being excluded from real-time scanning. To add a table to this list, select the field and enter the name. You can't remove default tables from this list.

    **Note:** The tables listed here will be included in scheduled scans but will not display findings in real-time.

5.  Enter a number for the **Maximum Lines for Real-Time Scan**.

    This sets the maximum number of code lines that can be scanned in real-time. Scripts exceeding this limit will not be scanned during editing.


If you cannot edit the properties, or real-time scanning does not activate after you complete these steps, check your instance for custom ACLs or property overrides.

## What to do next

After you change the properties, you might need to log out and log back in for the settings to take effect.

**Parent Topic:**[Configure Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-scan-engine-properties.md)


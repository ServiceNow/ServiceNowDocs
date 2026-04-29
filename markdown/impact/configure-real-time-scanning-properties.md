---
title: Configure real-time scanning properties
description: Real-time scanning properties allow control over which users have access to real-time scanning, and how the scan operates within their environment. Perform the following procedure to configure real time scanning properties.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Scan Engine properties, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure real-time scanning properties

Real-time scanning properties allow control over which users have access to real-time scanning, and how the scan operates within their environment. Perform the following procedure to configure real time scanning properties.

## Before you begin

Role required: Scan Engine Admin \(`sn_se.scan_engine_admin`\).

## Procedure

1.  Navigate to **ALL &gt; Impact &gt; Configuration &gt; Scan Engine Properties**.

2.  Select who will see real time scanning results:

    -   All users
    -   Only users with the `sn_se.scan_engine_user` role.

        Or, to turn off real-time scanning, select **Disable**.

3.  Select whether to **Enforce real time validation**.

    Users designated in **Real Time Message Visibility** will be required to correct findings at the Error or Warning level before saving the form, as long as those findings do not have approved exception reasons.

4.  Select whether to **Exclude suggestion finding**, which hides Suggestion level findings from real-time display, showing only Review, Warning, and Error levels.

    The Excluded tables area lists which tables are being excluded from real-time scanning. To add a table to this list, click at the bottom, and enter its name. You cannot remove default tables from this list.

    **Note:** The tables listed here will be included in scheduled scans but will not display findings in real-time.

5.  Enter a number for the **Maximum Lines for Real-Time Scan**. This sets the maximum number of code lines that can be scanned in real-time. Scripts exceeding this limit will not be scanned during editing.



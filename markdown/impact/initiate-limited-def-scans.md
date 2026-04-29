---
title: Initiate limited definition scans
description: You can scan individual definitions or suites of definitions on-demand.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Running on-demand scans, Scan Engine, Platform Health, Using Impact, Impact]
---

# Initiate limited definition scans

You can scan individual definitions or suites of definitions on-demand.

## Before you begin

Limited definition scans run faster than full instance scans because they only execute specific definitions rather than all active definitions. They are useful for quickly verifying fixes, testing new definitions, or focusing on specific areas of concern.

Role required:

-   Scan Engine users can initiate scans.
-   System Admins have read/write access to the custom application table.

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Platform Health**, and then select one of the following:

    -   **Definitions**
    -   **Definition Suites**
2.  Select the definitions or definition suites that you want to scan.

3.  Select one of the following:

    -   On the definition record, select the **Actions** menu, then select **Scan Instance for this Definition**.

        This initiates an on-demand scan that applies only this definition across your entire instance.

    -   On the suite record, select **Scan this Suite** to initiate the scan.

        Definition suites group related definitions. Scanning a suite runs all definitions in that suite.



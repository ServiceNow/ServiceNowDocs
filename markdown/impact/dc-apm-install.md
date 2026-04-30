---
title: Install the Data Collection Pack for APM
description: To enable the Data Collection Pack, you must install dependent plugins and activate Data Collection jobs.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Impact Value Management Data Collection for APM, Impact Value Management data collection apps, Configuring Impact, Impact]
---

# Install the Data Collection Pack for APM

To enable the Data Collection Pack, you must install dependent plugins and activate Data Collection jobs.

## Before you begin

The APM Success Metric Definitions in this application rely on another application. Ensure that the required plugins are installed if they are not already. For more information, see [Install Impact Value Management Data Collection Content Pack Apps dependent plugins](dc-install-plugins.md).

**Note:** If you have SPM Data Collection packs activated, navigate to the APM indicator \(Impact VM - \# of Applications Migrated\) &gt; indicator source \(Impact VM APM - Number of Applications Migrated\) and ensure that the state is set to complete.

Role required: Impact user

## Procedure

1.  Navigate to the Impact workspace on your instance.

2.  Navigate to **All &gt; Impact &gt;Configuration &gt;Value PA Data Collection Jobs** &gt; **.**

3.  Select **Value PA Data Collection jobs**.

4.  Search for and select the following:

    -   **Impact VM - APM - Monthly Data Collection**
    -   **Impact VM - APM - Historical Data Collection**
    If you're having trouble finding the data collection jobs, check whether the required data collection-dependent plugins are installed correctly. See [Install Impact Value Management Data Collection Content Pack Apps dependent plugins](dc-install-plugins.md).



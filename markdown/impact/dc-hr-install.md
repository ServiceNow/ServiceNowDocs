---
title: Install the Data Collection Pack for HR
description: To enable the Data Collection Pack, you must install dependent plugins and activate Data Collection jobs.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Impact Value Management Data Collection Content Pack for HR, Impact Value Management data collection apps, Configuring Impact, Impact]
---

# Install the Data Collection Pack for HR

To enable the Data Collection Pack, you must install dependent plugins and activate Data Collection jobs.

## Before you begin

The HR Success Metric Definitions in this application rely on another application. Ensure that the required plugins are installed if they are not already installed. For more information, see [Install Impact Value Management Data Collection Content Pack Apps dependent plugins](dc-install-plugins.md).

The HR Success Metric Definitions in this application are also dependent on the following Content Packs from the store for the pre-build HR Service Definitions:

-   [Offboarding - Voluntary Separation](https://store.servicenow.com/sn_appstore_store.do#!/store/application/956a8357dbcc241039f49ee4db961912)
-   [Offboarding - Reduction In Force](https://store.servicenow.com/sn_appstore_store.do#!/store/application/04061a28db0e6c108fc25e77dc961927)
-   [Offboarding - Involuntary Separation](https://store.servicenow.com/sn_appstore_store.do#!/store/application/ef6f9001db21a81034ac581adc9619ac)
-   [Employee Transfers](https://store.servicenow.com/sn_appstore_store.do#!/store/application/6e755ee4db0e6c108fc25e77dc961950)

Role required: Impact users

## Procedure

1.  Navigate to the Impact workspace on your instance.

2.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Value PA Data Collection Jobs**.

3.  Select **Value PA Data Collection jobs**.

4.  Search for and select the following:

    -   **Impact VM - HR - Monthly Data Collection**
    -   **Impact VM - HR - Historical Data Collection**
    If you're having trouble finding the data collection jobs, check whether the required data collection-dependent plugins are installed correctly. See [Install Impact Value Management Data Collection Content Pack Apps dependent plugins](dc-install-plugins.md).



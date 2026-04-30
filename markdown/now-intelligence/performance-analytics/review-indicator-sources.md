---
title: Review the indicator sources
description: Determine which fields contain the data you are looking for in each application you are enabling for Performance Analytics.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Platform Analytics Solutions, Platform Analytics solutions, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Review the indicator sources

Determine which fields contain the data you are looking for in each application you are enabling for Performance Analytics.

## Before you begin

You have enabled Performance Analytics according to your entitlement. You have also installed the relevant Analytics and Reporting solutions, and run diagnostics.

Role required: pa\_admin, admin

## About this task

Ensure that the indicator sources that Platform Analytics Solutions contain point at the correct fields for you to measure the performance of your processes.

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Administration Console**.

2.  Click the **Dashboards** link in the **Explore and Manage** tile.

    ![The Performance Analytics admin console with the Dashboards link highlighted](../image/pa-admin-console-dashboards.png)

3.  Verify the names of the dashboards that have been installed with this Platform Analytics Solution.

4.  Open the **Indicator Sources** tab.

5.  For each dashboard included in this Platform Analytics Solution:

    1.  Filter the indicator sources on the dashboard name.

        This screenshot shows the indicator sources filtered on the Self-Service Analytics dashboard from the Self-Service Analytics for CSM Platform Analytics Solution. ![The Indicator sources tab of the PA Admin Console showing the indicator sources for the Self-Service Analytics dashboard](../../dashboards/image/pa-admin-console-indicator-sources.png)

    2.  Review the facts table, conditions, and frequency of the indicator sources compared to the data structure on your own instance.

        **Important:** Pay particular attention to time stamp fields such as Resolved, Opened, or Created in the Conditions. You may need to use different time stamp fields.

    3.  If necessary, open an indicator source and make corrections.

    4.  If you are editing an indicator source record, go to the Indicators related list and review the **Conditions** field for each indicator.

        Changing the indicator source can also affect the additional conditions on the individual indicators.

    5.  Click **Update** to save your changes.


**Parent Topic:**[Configure Platform Analytics Solutions](../concept/configure-nowintel-solutions.md)

**Previous topic:**[Configure Platform Analytics Solutions](../concept/configure-nowintel-solutions.md)

**Next topic:**[Update Performance Analytics scripts](update-pa-scripts.md)

**Related topics**  


[Indicator sources](../concept/c_IndicatorSources.md#)


---
title: Configure the Platform Analytics Solution for Health Log Analytics
description: Run diagnostics, review and customize components, and start collecting data.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Platform Analytics Solutions for Health Log Analytics, Analytics and Reporting in Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure the Platform Analytics Solution for Health Log Analytics

Run diagnostics, review and customize components, and start collecting data.

## Before you begin

A ServiceNow AI Platform administrator must have installed the content pack plugins or ServiceNow Store application for this Platform Analytics Solution.

Role required: pa\_admin

## Procedure

1.  Run diagnostics on all records.

    These diagnostics can catch many mismatches between the configuration of your Platform Analytics Solutions and your tables.

2.  Navigate to **All** &gt; **Performance Analytics** &gt; **Administration Console**.

3.  Verify the name of the dashboard that has been installed with this Platform Analytics Solution:

    Health Log Analytics Overview dashboard.

4.  Open the **Indicator Sources** tab.

5.  For each dashboard included in this Platform Analytics Solution:

    1.  Filter the indicator sources on the dashboard name.

    2.  Review the facts table, conditions, and frequency of the indicator sources compared to the data structure on your own instance.

        **Important:** Pay particular attention to time stamp fields such as Resolved or Created that are referenced in the **Conditions** field. You may need to use different time stamp fields.

    3.  If necessary, open an indicator source and make corrections.

    4.  If you are editing an indicator source record, go to the Indicators related list and review the Conditions field for each indicator.

        Changing the indicator source can also affect the additional conditions on the individual indicators.

6.  If you changed the time field stamps in any indicator sources, then change any related Performance Analytics scripts.

7.  Open the **Breakdown Sources** tab.

8.  For each dashboard included in this Platform Analytics Solution:

    1.  Filter the breakdown sources on the dashboard name.

    2.  Review the conditions on the breakdown source as described in Review the breakdown sources.

9.  Navigate to **All** &gt; **Performance Analytics** &gt; **Jobs**.

10. Set up and run the historical job for this Platform Analytics Solution, **\[PA HLA\] Historic Data Collection**.

11. Edit and activate the scheduled data collection job for this Platform Analytics Solution, **\[PA HLA\] Historic Data Collection**.


**Parent Topic:**[Platform Analytics Solutions for Health Log Analytics](hla-content-pack.md)


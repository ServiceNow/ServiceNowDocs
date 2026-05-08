---
title: Configure the Platform Analytics Solution for Self-Service Analytics for Customer Service
description: Run diagnostics, review and customize components, and start collecting data.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Extend capabilities, Configure, Customer Service Management]
---

# Configure the Platform Analytics Solution for Self-Service Analytics for Customer Service

Run diagnostics, review and customize components, and start collecting data.

## Before you begin

Role required: pa\_admin

A ServiceNow AI Platform administrator must have installed the content pack plugins or ServiceNow Store application for this Platform Analytics Solution.

## Procedure

1.  Run all diagnostics on all records, as described in Performance Analytics diagnostics.

    These diagnostics can catch mismatches between the configuration of your Platform Analytics Solutions and your tables.

2.  Navigate to **Performance Analytics** &gt; **Admin Console**.

3.  Click the **Dashboards** link in the **Explore and Manage** tile.

4.  Verify the names of the dashboards that have been installed with the Self-Service Analytics Platform Analytics Solution.

5.  Open the **Indicator Sources** tab.

6.  For each dashboard included in this Platform Analytics Solution:

    1.  Filter the indicator sources on the dashboard name.

        This screenshot shows the indicator sources filtered on the Self-Service Analytics dashboard from the Self Service Analytics for Customer Service Platform Analytics Solution. ![Indicator Sources tab showing the indicator sources and their details for the Self-Service Analytics dashboard.](../../../product/customer-service-management/image/pa-admin-console-indicator-sources.png)

    2.  Review the facts table, conditions, and frequency of the indicator sources compared to the data structure on your own instance.

        **Important:** Pay particular attention to time stamp fields such as Resolved or Created that are referenced in the **Conditions** field. You may need to use different time stamp fields.

    3.  If necessary, open an indicator source and make corrections.

    4.  If you are editing an indicator source record, go to the Indicators related list and review the **Conditions** field for each indicator.

        Changing the indicator source can also affect the additional conditions on the individual indicators.

7.  If you changed the time field stamps in any indicator sources, also change any related Performance Analytics scripts.

8.  Open the Breakdown Sources tab.

9.  For each dashboard included in this Platform Analytics Solution:

    1.  Filter the breakdown sources on the dashboard name.

    2.  Review the conditions on the breakdown source.

10. Navigate to **Performance Analytics** &gt; **Jobs**.

11. Set up and run the historical job for this Platform Analytics Solution, \[SSA\] Self-Service Analytics Data Collection.

12. Edit and activate the scheduled data collection job for this Platform Analytics Solution, \[SSA\] Self-Service Analytics Data Collection.


**Related topics**  


[Platform Analytics Solutions for Self-Service Analytics for Customer Service](../../dashboards/application-content-packs/ssa-cs-content-pack.md)

[bundle-platcap.self-service-analytics]


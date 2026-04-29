---
title: Upgrade a dashboard
description: When you upgrade a dashboard, solution metadata that have updates available, including any new records added to the dashboard, are installed. Solution metadata records that you have customized, even if those records are updated in the newer release​, are not affected.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install a dashboard, Platform Analytics solutions, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Upgrade a dashboard

When you upgrade a dashboard, solution metadata that have updates available, including any new records added to the dashboard, are installed. Solution metadata records that you have customized, even if those records are updated in the newer release​, are not affected.

## Before you begin

Role required: pa\_admin

## About this task

When you install or upgrade a Performance Analytics solution, out of the box content in the instance is overwritten and new content is added to the dashboard. Any content that you have previously customized on the dashboard is not changed.

## Procedure

1.  Navigate to **PA Solution Library** &gt; **Solutions**.

    Records where the **Update Available** field is true can be upgraded.

2.  Select the dashboard you want to upgrade.

3.  Review the **Solution Metadata** related list.

    When you click **Upgrade**, solution metadata records in which update\_available = true are installed. Previously customized records are not overwritten.

4.  Click **Upgrade**.

    The **Upgrade** button is available if at least one solution metadata record has an update available and the solution content has been installed at least once.

5.  In the confirmation window, click **Upgrade**.

    The upgrade may take some time to complete after you confirm. If you click **Cancel** during this time, the confirmation window closes, but does not stop an in-progress upgrade.


## Result

New dashboard records are added to the dashboard. Updates to dashboard records that are not customized are applied. Dashboard records that you have customized are left unchanged.

## What to do next

If the dashboard does not appear as you expected after installing the solution content, see if the uninstalled records appear on the customer update table. Any uninstalled records on this table were previously customized. To view the customer updates table, enter `sys_update_xml.list` in the filter navigator.

**Parent Topic:**[Install a dashboard](install-content.md)


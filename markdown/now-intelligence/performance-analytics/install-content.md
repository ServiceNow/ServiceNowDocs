---
title: Install a dashboard
description: Use the Solution Library to install a dashboard and all its associated visualizations such as widgets and reports, and to configure existing dashboards.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Platform Analytics solutions, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Install a dashboard

Use the Solution Library to install a dashboard and all its associated visualizations such as widgets and reports, and to configure existing dashboards.

## Before you begin

Role required: pa\_admin.

## About this task

When you install or upgrade a Performance Analytics solution, out of the box content in the instance is overwritten and new content is added to the dashboard. Any content that you have previously customized on the dashboard is not changed.

To reinstall a solution metadata record from a dashboard, such as a widget, without impacting other records used by the same dashboard, see [Install a single solution metadata record](install-content-single-record.md).

## Procedure

1.  Navigate to **PA Solution Library** &gt; **Solutions**.

2.  Select the dashboard you want to install.

    The dashboards provided in the Solution Library may depend on indicators, indicator sources, or other configuration records. Solution Library content always includes the associated visualization and configuration content.

3.  Click **Install**.

4.  In the confirmation window, click **Install**.

    The installation may take some time to complete after you confirm. Clicking **Cancel** during this time closes the confirmation window but does not stop the in-progress installation.

    When the installation is complete, the confirmation window disappears and the **Installed Metadata** related list is populated with the records that were installed.


## What to do next

Navigate to the dashboard to begin analyzing your data.

-   **[Upgrade a dashboard](upgrade-content.md)**  
When you upgrade a dashboard, solution metadata that have updates available, including any new records added to the dashboard, are installed. Solution metadata records that you have customized, even if those records are updated in the newer release​, are not affected.
-   **[Install a single solution metadata record](install-content-single-record.md)**  
Install a single solution metadata record used by a dashboard, such as a widget, to match the latest version of the record without impacting other records used by the same dashboard.
-   **[Duplicate an Analytics and Reporting Solution dashboard](duplicate-dashboard.md)**  
Copy an Platform Analytics Solution dashboard, including the tabs, portal pages, and canvas records. Widgets on the dashboard are not duplicated.

**Parent Topic:**[Platform Analytics solutions](../concept/content-packs-in-form-analytics-published.md)

**Related topics**  


[bundle-platadm.t_ActivateAPlugin]


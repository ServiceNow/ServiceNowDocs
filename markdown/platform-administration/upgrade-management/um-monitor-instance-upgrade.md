---
title: Monitor an upgrade to an instance
description: Monitor the progress of an ongoing upgrade in an instance with the Upgrade Monitor. When the upgrade is done, you can view a summary of the results on the Upgrade Summary Report.
locale: en-US
release: australia
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Upgrade Monitor tool in Upgrade Console, Upgrade Console tools, Use, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Monitor an upgrade to an instance

Monitor the progress of an ongoing upgrade in an instance with the Upgrade Monitor. When the upgrade is done, you can view a summary of the results on the Upgrade Summary Report.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to Upgrade Monitor using one of the following ways.

    |Option|Navigation|
    |------|----------|
    |Using left navigation|Navigate to **All** &gt; **Admin Center** &gt; **Upgrade Management** &gt; **Upgrade Monitor**.|
    |Using Admin tab option|Navigate to **Admin** &gt; **Upgrade Management** &gt; **Upgrade Monitor**.|

    **Note:** If an upgrade is in progress, the user is automatically directed to the Upgrade Monitor page.

    A list of upgrades is displayed.

2.  Monitor the progress of the upgrade.

    When the system finishes the upgrade, it displays the Complete upgrade summary report.

    **Note:** You can now view the status of every stage in the upgrade process. See [Upgrade Progress](../reference/um-monitor-progress.md) for more information.


## What to do next

From the Upgrade Summary Report, [resolve any conflicts](um-process-skipped-records.md) that prevented the system from upgrading records.

-   **[Upgrade Progress](../reference/um-monitor-progress.md)**  
When an upgrade is underway, Upgrade Progress displays progress bars and other information to help you monitor the process.
-   **[Upgrade Summary Report](../reference/um-complete-summary.md)**  
The Upgrade Summary report summarizes the actions taken, provides tools to resolve conflicts between customizations and changes that are part of the upgrade, and provides information to help estimate time for upgrades to other instances.

**Parent Topic:**[Upgrade Monitor tool in Upgrade Console](../concept/um-upgrade-monitor-tool.md)


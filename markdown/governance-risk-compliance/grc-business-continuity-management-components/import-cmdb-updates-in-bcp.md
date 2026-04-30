---
title: Update the planning dependencies
description: Update the plan dependencies manually from the snapshot if the scheduled job is not activated in the Planning dependency update configuration module. You can update the dependencies in an active plan.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Scheduling auto-update of related assets, Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Update the planning dependencies

Update the plan dependencies manually from the snapshot if the scheduled job is not activated in the Planning dependency update configuration module. You can update the dependencies in an active plan.

## Before you begin

Role required: sn\_bcm.program\_manager, sn\_bcm.planner, sn\_bcm.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  Open a BCP in the **Draft** state and navigate to the **Scope** tab.

    If the dependencies have been updated in the sources, the scheduled job fetches the dependencies. You can select the snapshot record to view the updates.

3.  To view the snapshot record, select the **Pending updates** module in the **Planning** list view and select a snapshot record.

    The Plan dependency delta snapshot is displayed.

    ![Plan snapshot record.](../image/plan-snapshot.png)

    The BCM application stores one active snapshot for the BCP at a time. The snapshots that are in the **Completed** state and that have not been updated in the past six months are removed from the application automatically.

4.  To update the dependencies manually, navigate to the plan and select **Update dependencies**.

    A UI message is displayed on the screen: `Dependencies are being updated.`

5.  To save the changes to the plan, select **Save**.

    The plan owners and BCM lead can update the planning dependencies by saving the changes to the plan.


**Parent Topic:**[Scheduling auto-update of related assets](../concept/import-cmdb-updates-in-plans.md)


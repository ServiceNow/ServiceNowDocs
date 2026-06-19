---
title: Synchronize assets between loss scenarios and recovery strategies
description: Use the asset syncing fields in the plan template to configure whether assets synchronize to loss scenarios, to recovery strategies, or both. Syncing is a two-step process: assets flow from the plan to loss scenarios first, and then from loss scenarios to recovery strategies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/syn-ast-be-lo-sce-and-rec-stgy.html
release: australia
topic_type: task
last_updated: "2026-04-06"
reading_time_minutes: 2
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Synchronize assets between loss scenarios and recovery strategies

Use the asset syncing fields in the plan template to configure whether assets synchronize to loss scenarios, to recovery strategies, or both. Syncing is a two-step process: assets flow from the plan to loss scenarios first, and then from loss scenarios to recovery strategies.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## About this task

Synchronization behavior:

-   Assets added to a plan synchronize to loss scenarios based on element definition.
-   Assets added to loss scenarios synchronize to recovery strategies.
-   Direct syncing from plan assets to recovery strategies is not supported in a single step.
-   Syncing to loss scenarios and syncing to recovery strategies are configured independently.
-   Filters for loss scenarios and plan assets are independent of each other.

**Note:** If you attempt to delete an asset that is in use by a recovery strategy, an error message appears with a direct link to the related recovery strategies.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Plan record** and open the plan template you want to configure.

2.  To configure asset syncing in a plan template, locate the two new asset syncing fields in the template form.

3.  Select the option to enable syncing assets to loss scenarios if required.

4.  Select the option to enable syncing assets to recovery strategies if required.

5.  Save the template.

    **Note:** Both fields can be enabled independently. Enabling one does not automatically enable the other.

6.  To add assets to a plan and synchronize to loss scenarios, open the plan where you want to add assets.

    1.  In the Plan assets section, select Add to add one or more assets.

        Assets synchronize to associated loss scenarios automatically based on the element definition.

    2.  Verify the synced assets by opening a loss scenario and reviewing its assets list.

7.  To synchronize assets from a loss scenario to a recovery strategy, open the loss scenario that contains the assets you want to synchronize.

    1.  Confirm the assets are listed in the loss scenario’s assets section.

        Assets synchronize to the associated recovery strategies automatically.

    2.  Open the recovery strategy and verify that the assets appear in its assets list.

8.  To delete an asset used in a recovery strategy, open the plan’s assets and select the asset you want to delete and select **Delete**.

    If the asset is in use by one or more recovery strategies, an error message appears.

    1.  Select the link in the error message to navigate to the related recovery strategies.

    2.  Remove the asset from the recovery strategies, then return to the plan assets and retry the deletion.


**Parent Topic:**[Structured workflows for BCPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcp-tasks-performed-by-bcp-owner.md)


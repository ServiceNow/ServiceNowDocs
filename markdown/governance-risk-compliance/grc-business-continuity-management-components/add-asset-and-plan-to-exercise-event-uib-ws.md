---
title: Track impacted assets and add associated plans
description: Track the impacted assets and add an associated plan to the exercise. You can then monitor the assets and plans for the exercise in BCM UIB Workspace.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Track impacted assets and add associated plans

Track the impacted assets and add an associated plan to the exercise. You can then monitor the assets and plans for the exercise in BCM UIB Workspace.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** &gt; **Exercises** &gt; **Pending** and select the exercise event in the list.

2.  Select **Add** in the **Assets** tab.

    You can add an asset that you want to recover during the exercise. The primary elements of the asset are listed as **Asset types**. The primary elements belong to the element definition type that is identified in the plan template. When you add an asset to the event, its associated dependencies are pulled into the event. The dependencies are displayed in the **Asset types** panel.

    When you select **Add** for an application, all the dependencies that you had identified in the business impact analysis of that application are also added to the exercise. The example shows the dependencies for Business Application: Acrobat in the **Asset types** panel of the exercise.

    **Note:** Starting with the Xanadu and later releases, the Crisis manager can initiate an event task even if the plan includes recovery tasks that do not have any assets tagged. The former requirement that every activated plan should have at least one tagged asset has been removed.

    ![Adding an asset to the event.](../image/add-asset-to-an-event.png)

    **Note:**

    The **source\_table\_fields** configuration applies to the **Assets** tab in recovery events. The purpose of **source\_table\_fields** is to set the columns for the modal based on the asset types.

    The following modal shows the columns that appear when you select **Add** for Applications asset type.

    ![The source_table_fields are used to set the columns for the modal based on the asset type.](../image/event-asset-types.png)

3.  Add an asset in the **Assets** tab and review the populated RTO values in the **Finalized RTO** and **Finalized RPO** columns.

    When you add an event asset, for example Acrobat, the finalized RTO and RPO values from its BIA are populated in the **Finalized RTO** and **Finalized RPO** columns.

    **Note:** Recovery assets are now linked to their corresponding BIA records, enabling automatic retrieval of key data such as RTO, RPO, and Recovery Tier.

    ![Event assets.](../image/acrobat-event-asset-rto.png)

    When you open the event asset record \(for example, "Acrobat"\), the "Finalized RTO," "Finalized RPO," "Recovery Tier," and "BIA" values are automatically populated and displayed in the record as shown in the example.

    ![Event.](../image/acrobat-event-record.png)

4.  To update the state of the impacted asset, open the newly added asset record from the list and select **State**.

5.  To add a plan, navigate to the **Plans** tab and select **Add**.

    1.  Select the plan from the displayed plans list and select **Add**.

        The plans list is shown in the example.

        ![Plans list.](../image/plans-list-in-event.png)

        **Note:** Starting with GRC: Crisis Management, version 9.1.4, the logic for fetching the plans into a recovery event is updated. Previously, all plans related to the target plan were automatically included. With a clear upstream and downstream plan hierarchy, pulling in a plan does not pull its upstream plans automatically.

        The plans are added to the event.

        ![Plans added in event.](../image/plans-added-in-event.png)

6.  To add all plans that are related to the asset, select **Add all plans related to asset**.

    Archived plans: Archived plans are not displayed in the selection modal when adding associated plans. Within an exercise or event, archived plans are no longer available in the selection modal, preventing you from adding them directly. When using **Add all plans related to asset**, primary archived plans are not pulled in. However, associated archived plans are still included, since they may be dependencies of active plans required for the event to run successfully. If you do not want these archived downstream plans included, adjust the relationships accordingly.

    An informational message is displayed that all plans related to the selected application are added in the background as shown in the example.

    ![Add all plans related to asset.](../image/exercise-event-add-all-plans-related-to-asset.png)

7.  Select **Save**.

    The actual end time for the impacted assets is updated in the **Details** tab when all event tasks associated with the assets are completed. Once these tasks are completed, the actual end time is recorded, and the actual time taken is calculated. The total effort is calculated based on the total time taken for all the tasks where this asset is related. After completion, the state of the impacted asset is updated to **Recovered**. If any tasks are in the **Close failed** state, the state of the impacted asset is not updated and it is marked as **Not recovered**.

    In the **Tag assets** field on the recovery task form of the plan, you can select the assets:

    -   If you select all assets, all assets present in the plan are added to the impacted assets of the event task.
    -   If you select specific assets, only those specific assets present in the plan are added to the impacted assets of the event task.
    -   If you select none assets, no assets present in the plan are added to the impacted assets of the event task.
    **Note:**

    The current demo data has an issue where both **Included task in** and **Tag asset** fields are empty. To resolve this, you have to add tasks to **Included task in** manually and select assets for the **Tag asset** field. Without these, event tasks won't be created and assets won't be marked as impacted.

    If you haven't selected **Included task in**, your event task won't be created. If you don't select **Tag asset**, your asset won't be marked as an impacted asset.

    This issue doesn't apply to newly created plans.

    The exercise is saved in the **Pending** state.


**Parent Topic:**[Structured workflows for exercises](../concept/performing-tasks-to-manage-exercise-events.md)


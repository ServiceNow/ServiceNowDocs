---
title: Track impacted assets and add related plans
description: Track the impacted assets and add a related plan during a crisis event. You can monitor the assets and plans for the crisis event in BCM UIB Workspace. You can then recover your assets in the planning stage.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Structured workflows for crisis events, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Track impacted assets and add related plans

Track the impacted assets and add a related plan during a crisis event. You can monitor the assets and plans for the crisis event in BCM UIB Workspace. You can then recover your assets in the planning stage.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  In the List view, navigate to **Crisis events** &gt; **Pending** and select the crisis event in the list.

3.  Select the **Assets** tab and select **Add**.

    You can add an asset that you want to recover during the crisis. The primary elements of the asset are listed as **Asset types**. The primary elements belong to the element definition type that is identified in the plan template. When you add an asset to the event, its associated dependencies are pulled into the event. The dependencies are displayed in the **Asset types** panel.

    **Note:** When you select **Add** for an application, all the dependencies that you had identified in the business impact analysis of that application are also added to the exercise.

4.  In the Applications list, select the application and navigate to the **Plans** tab.

    When you add a plan to the crisis event, the related plans, assets, and event tasks that are associated with the plan also get pulled into the event.

5.  Select **Add all plans related to asset**.

    If you have any plans related to the selected application in the instance, they are added to the exercise event.

6.  Select **Save**.

    The crisis event is saved in the **Pending** state.


**Parent Topic:**[Structured workflows for crisis events](../concept/perform-tasks-to-manage-crisis-events.md)


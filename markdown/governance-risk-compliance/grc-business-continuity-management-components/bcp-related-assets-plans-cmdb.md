---
title: Add related assets and related plans
description: Identify related assets and their referred plans to recover the assets in your planning stage. Reuse the configuration item relationship data that flow from CMDB to business impact analysis \(BIA\) during dependency assessment to identify the assets in your plan.
locale: en-US
release: zurich
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Structured workflows for Business Continuity Planning, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Add related assets and related plans

Identify related assets and their referred plans to recover the assets in your planning stage. Reuse the configuration item relationship data that flow from CMDB to business impact analysis \(BIA\) during dependency assessment to identify the assets in your plan.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## About this task

With this feature enhancement, the relationship data of the configuration items in CMDB flow in to the business impact analysis \(BIA\) when you [Add dependencies based on CI relationships in CMDB](add-dependencies-based-on-cmdb.md). If you have done the BIA, then the related assets data flow to the planning phase. In the planning phase, you can identify these BIA-dependent items as related assets. Additionally, if you have done the BIA and if your related assets has a plan, then you also have the capability to add the plan existing for the related assets as related plans in the planning phase, and as sub-plans in the execution phase of the event recovery process.

Therefore, instead of identifying new assets and creating plans to recover the assets you can use the BIA-dependent items that are added as configuration items from CMDB based on their CI relationship and reuse these items as related assets in the planning stage.

This feature gives you the ability to:

-   Identify the related assets based on dependencies established in the CMDB and BIA during planning.
-   Create a main plan and set a task that refers to another related plan.

## Procedure

1.  Navigate to **All** &gt; **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

3.  Click **In Draft** state in the Planning list.

4.  Click the link to the plan record in the **Name** column.

5.  Click the **Related Assets** tab to view the assets that are pulled from the BIA to the plan.

    If you have added a business process or a location as an item in the **Scope** tab, and if the scoped item is related to the BIA, then all the related assets of the BIA are lined in to the **Related Assets** tab of the plan. In other words, the CMDB configuration item added as a dependency in BIA is pulled into the plan as related assets. The source of these related assets is displayed as BIA.

    When you create a plan, you also select a primary element that the plan covers. Based on the [scope that you selected in the business continuity plan](add-plan-asset-scope-bcp.md) or the primary element of the plan, the application adds the related assets and related plans during the planning phase. These items could be business processes, critical business applications, data centers, or resources working from a location. All these dependencies if stored in the BIA are copied over to the plan in the **Related Assets** tab in addition to other dependencies that are added while creating the BIA.

    ![Related assets tab with source.](../image/SourceRelAssetsBCP.png "Related assets tab")

    **Note:** Unless you do the business impact analysis, the related items of the configured item data will not flow to the plan, although you have the option to manually add the related assets and related plans in the planning phase.

6.  To add an asset manually, click the **Add** button.

    1.  Select a type of the impacted item in the Add Items pop-up.

    2.  Click **Next** and select the items that belong to the impacted item type.

    3.  Click **Add**.

        **Note:** If the item did not come from the BIA but added during the planning phase, then the source of the impacted item that you added is **Manual**.

7.  To remove a related asset, select the related asset and click **Remove**.

8.  Click the **Related Plans** tab to view the plans that are related to the items in the **Related Assets** tab.

    After the assets are copied over to the plan, if there are plans attached to any of the related assets, then these plans are automatically pulled and listed in the **Related Plans** tab. Assets in the plan are those that are to be recovered by the plan during the event.

    When the related plans are pulled into the planning phase, you can also create the recovery tasks. As a planner you can set a sequence to the execution of the recovery tasks of the main plan and its dependent sub-plans.

    If you have not done the BIA or scoped the plan to a BIA, you can manually add plans at this stage.

9.  To add a plan manually, click the **Add** button.

    1.  Select a plan in the Add pop-up.

    2.  Click **Add**.

        ![Related plan tab with source.](../image/SourceRelPlanBCP.png "Related plan tab")

        **Note:** The source of the related plan that you added is **Manual**, as the plan did not come from the BIA but added during the planning phase.

10. To remove a related plan, select the related plan and click **Remove**.


## What to do next

You can [refer one of the related plans](bcp-recovery-tasks-grid.md#refer-related-plan-bcp) in a recovery task of the main plan and sequence the order of execution in the event.


---
title: Assets and plans related to BCP
description: You can identify the assets and plans related to a business continuity plan. You can then recover the assets in your planning stage. Reuse the configuration item relationship data that flow from CMDB to business impact analysis \(BIA\) during dependency assessment to identify the assets in your plan.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Business continuity planning, Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# Assets and plans related to BCP

You can identify the assets and plans related to a business continuity plan. You can then recover the assets in your planning stage. Reuse the configuration item relationship data that flow from CMDB to business impact analysis \(BIA\) during dependency assessment to identify the assets in your plan.

## Related assets

If you have added a business process or a location as an item in the **Primary scope** panel of the record, and if the scoped item is related to the business impact analysis, then all the related assets of the business impact analysis are listed in the **Related assets** panel in the record.

In other words, the CMDB configuration item added as a dependency in the business impact analysis is pulled into the plan as a related asset. The source of these related assets is displayed as the business impact analysis.

When you create a plan, you also select a primary element that the plan covers. Based on the scope that you selected in the business continuity plan or the primary element of the plan, the application adds the related assets and related plans during the planning phase. These items could be business processes, critical business applications, datacenters, or resources working from a location. All these dependencies if stored in the business impact analysis are copied over to the plan in the **Related assets** panel in addition to other dependencies that are added while creating the business impact analysis.

The example shows the primary scope and related assets for a business continuity plan.

![Primary scope and related assets.](../image/primary-scope-related-assets.png)

## Related plans

After the assets are copied over to the plan, if there are plans attached to any of the related assets, then these plans are automatically pulled and listed on the **Related Plans** tab. Assets in the plan are the entities that are to be recovered by the plan during the event. When the related plans are pulled into the planning phase, you can also create the recovery tasks. As a planner, you can set a sequence to the execution of the recovery tasks of the main plan and its dependent subplans.


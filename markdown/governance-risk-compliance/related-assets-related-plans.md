---
title: Assets and plans related to BCP
description: You can identify the assets and plans related to a business continuity plan. You can then recover the assets in your planning stage. Reuse the configuration item relationship data that flow from CMDB to business impact analysis \(BIA\) during dependency assessment to identify the assets in your plan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/related-assets-related-plans.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Business continuity planning, Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# Assets and plans related to BCP

You can identify the assets and plans related to a business continuity plan. You can then recover the assets in your planning stage. Reuse the configuration item relationship data that flow from CMDB to business impact analysis \(BIA\) during dependency assessment to identify the assets in your plan.

## Related assets

If you have added business process or location as an item in **Primary scope**, and scoped item is related to BIA, all related assets of the BIA are listed in **Related assets**.

In other words, the CMDB configuration item added as a dependency in the business impact analysis is pulled into the plan as a related asset. The source of these related assets is displayed as the business impact analysis.

When you create a plan, you also select a primary element that the plan covers. Based on the scope in the plan or the primary element of the plan, the application adds related assets and related plans during the planning phase. These items could be business processes, critical business applications, datacenters, or resources working from a location. All these dependencies if stored in the business impact analysis are copied over to the plan in **Related assets** in addition to other dependencies added while creating the BIA.

The example shows the primary scope and related assets for a business continuity plan.

\[Omitted image "primary-scope-related-assets.png"\] Alt text: Primary scope and related assets.

## Related plans

After the assets are copied over to the plan, plans attached to any of the related assets are automatically pulled and listed on the **Related Plans** tab. Assets in the plan are the entities that are to be recovered by the plan during the event. When the related plans are pulled into the planning phase, you can also create the recovery tasks. As a planner, you can set a sequence to the execution of the recovery tasks of the main plan and its dependent subplans.


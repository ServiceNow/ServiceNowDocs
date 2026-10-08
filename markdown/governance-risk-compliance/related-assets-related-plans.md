---
title: Assets and plans related to BCP
description: You can identify the assets and plans related to a business continuity plan. You can then recover the assets in your planning stage. Reuse the configuration item relationship data that flow from CMDB to business impact analysis \(BIA\) during dependency assessment to identify the assets in your plan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/related-assets-related-plans.html
release: australia
topic_type: concept
last_updated: "2026-10-02"
reading_time_minutes: 2
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

Along with each related asset, the **Related assets** panel also displays the **Impact analysis**, **Recovery tier**, **Recovery time objective** \(RTO\), and **Recovery point objective** \(RPO\) of the asset. The **Primary scope** panel shows the same information for the primary element. These values are copied from the Results section of the **Details** tab of the business impact analysis that is linked to the asset, so the plan reflects the same recovery requirements that were established during the business impact analysis. If a finalized or adjusted RTO or RPO value exists on the business impact analysis, that value is shown instead of the system-calculated value. These fields are read-only on the plan and are updated whenever the business impact analysis changes or the plan dependencies are refreshed. For information about these fields, see [View business impact analysis details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/view-bia-details.md).

## Related plans

After the assets are copied over to the plan, plans attached to any of the related assets are automatically pulled and listed on the **Related Plans** tab. Assets in the plan are the entities that are to be recovered by the plan during the event. When the related plans are pulled into the planning phase, you can also create the recovery tasks. As a planner, you can set a sequence to the execution of the recovery tasks of the main plan and its dependent subplans.


---
title: Assets and plans related to BCP
description: You can identify the assets and plans related to a business continuity plan. You can then recover the assets in your planning stage. Reuse the configuration item relationship data that flow from CMDB to business impact analysis \(BIA\) during dependency assessment to identify the assets in your plan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/related-assets-related-plans.html
release: zurich
topic_type: concept
last_updated: "2026-10-02"
reading_time_minutes: 2
breadcrumb: [Business continuity planning, Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# Assets and plans related to BCP

You can identify the assets and plans related to a business continuity plan. You can then recover the assets in your planning stage. Reuse the configuration item relationship data that flow from CMDB to business impact analysis \(BIA\) during dependency assessment to identify the assets in your plan.

## Related assets

If you add a business process or location to the **Primary scope** panel, and that item is related to a business impact analysis, the **Related assets** panel lists all associated assets.

In other words, the CMDB configuration item added as a dependency in the business impact analysis is pulled into the plan as a related asset. The source of these related assets is displayed as the business impact analysis.

When you create a plan, you also select a primary element that the plan covers. The application adds related assets and related plans based on the BCP scope or primary element. These items can be business processes, critical business applications, datacenters, or resources at a location. Dependencies from the business impact analysis are copied to the **Related assets** panel, including dependencies added while creating the business impact analysis.

The example shows the primary scope and related assets for a business continuity plan.

\[Omitted image "primary-scope-related-assets.png"\] Alt text: Primary scope and related assets.

Along with each related asset, the **Related assets** panel also displays the **Impact analysis**, **Recovery tier**, **Recovery time objective** \(RTO\), and **Recovery point objective** \(RPO\) of the asset. The **Primary scope** panel shows the same information for the primary element. These values are copied from the Results section of the **Details** tab of the business impact analysis that is linked to the asset. The plan reflects the same recovery requirements that were established during the business impact analysis. If a finalized or adjusted RTO or RPO value exists on the business impact analysis, that value is shown instead of the system-calculated value. These fields are read-only on the plan. They are updated whenever the business impact analysis changes or the plan dependencies are refreshed. For information about these fields, see [View business impact analysis details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/view-bia-details.md).

## Related plans

After the assets are copied to the plan, any plans attached to the related assets are automatically pulled and listed on the **Related Plans** tab. Assets in the plan are the entities recovered during the event. When related plans are pulled into the planning phase, you can also create recovery tasks. As a planner, you can set the execution sequence for recovery tasks of the main plan and its dependent subplans.


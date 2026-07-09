---
title: Demand tasks
description: Demand tasks are units of work within a demand that help you plan and organize initial activities before converting the demand into a work entity such as a product, feature, or enhancement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/portfolio-planning/demand-tasks-ppw.html
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Demand tasks

Demand tasks are units of work within a demand that help you plan and organize initial activities before converting the demand into a work entity such as a product, feature, or enhancement.

## Demand task overview

Demand tasks enable you to organize and track early-stage planning activities within the demand record before you convert a demand into a work entity such as a feature, product, or enhancement. Unlike project tasks, which track execution and drive project completion dates, demand tasks focus on planning and preparation. This fundamental difference shapes what demand tasks can do and how you use them.

Examples of demand tasks include:

-   Gathering and documenting requirements from stakeholders
-   Conducting design or architecture reviews
-   Validating technical feasibility or dependencies
-   Completing business case analysis or ROI assessment
-   Conducting security, compliance, or impact assessments
-   Assigning resources for discovery or planning phases

Demand tasks aren't appropriate for execution work. After the demand is approved and converted into a work entity such as a project or feature, execution work moves into project tasks.

## Assigning resources and tracking effort

You can assign resources to demand tasks using the standard assignment fields. Resources assigned to demand tasks can submit time spent on them using a time card, enabling you to track actual effort and cost during the planning phase.

Resource assignments on demand tasks aren't transferred to the work entity created from that demand. If you later convert the demand into a project or work item, you must reassign resources in the new work entity. Similarly, the time and cost tracked on demand tasks remain within the demand record and don't transfer to the resulting work entity.

The actual cost for the demand task effort is derived from the hourly resource rate defined in the rate model, default labor rate, or default system property. The actual cost and effort for all demand tasks roll up to the associated demand. For more information, see [Actual cost and effort calculations for demands](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/actual-cost-and-effort-calculation-ppw.md).

## Differences from project tasks

Because demand tasks are used for early-stage planning and not execution tracking so they don't support some features that project tasks do:

-   Planned dates, actual dates, and original dates aren't supported in demand tasks.
-   The due date indicates when the task is targeted for completion and doesn't affect the demand workflow. Project tasks affect project completion dates when planned dates and actual dates are changed.
-   Nested demand tasks aren't supported.
-   Task constraints such as Start ASAP and Start on a specific date aren't supported.
-   Execution types such as Agile, Waterfall, or Hybrid aren't supported.


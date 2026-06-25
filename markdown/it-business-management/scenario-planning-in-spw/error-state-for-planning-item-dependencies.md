---
title: Item dependency errors in Strategic Planning Workspace
description: Learn about the scenarios when the planning item dependencies on the portfolio plan roadmap or free-form roadmap in Strategic Planning and Portfolio Planning can be in an error state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/error-state-for-planning-item-dependencies.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Item dependency errors in Strategic Planning Workspace

Learn about the scenarios when the planning item dependencies on the portfolio plan roadmap or free-form roadmap in Strategic Planning and Portfolio Planning can be in an error state.

A dependency between two planning items can be in an error state when a scheduling conflict exists between the items. In a linear \(Depends on\) dependency, the items are scheduled in a way that starting the work on one item requires completing the work on another item.

**Note:** Error states are displayed for only if the planning items have a **Depends on** type of relationship.

In the sample roadmap shown here, starting work on **Employee onboarding process improvement** is dependent on the completion of **Specific onboarding path for new hire**. This relation is considered a linear dependency. Here, **Employee onboarding process improvement** is scheduled to start before the end date of **Specific onboarding path for new hire**. This conflict is indicated on the roadmap with an error icon \(\[Omitted image "icon-dependency-error.png"\] Alt text: Dependency error icon.\), and is also mentioned in the Dependencies tab of the Item details side panel.

To resolve such errors, review the scope of the planning items and update the start or end dates to adjust their scheduling accordingly.

\[Omitted image "dependency-conflict.png"\] Alt text: planning item dependency conflicts.

**Parent Topic:**[Strategic Planning Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/alignment-planner-workspace-reference.md)

**Related topics**  


[Add dependencies for roadmap items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/create-planning-item-dependencies-in-a-roadmap.md)

[Update roadmap item dependencies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/manage-planning-item-dependencies-apw.md)


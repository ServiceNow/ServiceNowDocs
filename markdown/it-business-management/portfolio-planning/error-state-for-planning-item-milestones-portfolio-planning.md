---
title: Item milestone errors in Portfolio Planning Workspace
description: Learn about the scenarios when the planning item milestones on the portfolio plan roadmap or free-form roadmap can be in an error state in the Portfolio Planning Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-planning/error-state-for-planning-item-milestones-portfolio-planning.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Portfolio Planning, Strategic Portfolio Management]
---

# Item milestone errors in Portfolio Planning Workspace

Learn about the scenarios when the planning item milestones on the portfolio plan roadmap or free-form roadmap can be in an error state in the Portfolio Planning Workspace.

An item milestone can fall out of the approved start or end dates of the item when you reschedule the existing planning item.

When you reschedule a planning item on the roadmap, the due dates of its milestones don’t change. So, if the due date of a milestone is falls outside the item’s date range, the indicator for that out-of-range milestone is hidden and moved to an error state. Indicators for milestones that are still within the item's date range are visible.\[Omitted image "milestone-out-of-range.gif"\] Alt text: Milestone out of item's date range.

The milestones that are out of sync with the item's schedule can be viewed from the Milestones tab on the side panel. From the side panel, you can edit and adjust the due date of the milestone to reflect the change of plans. See [Update roadmap item milestones](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/manage-planning-item-milestones.md).\[Omitted image "milestone-out-of-range.gif"\] Alt text: Item milestone out of date range.

**Note:** You can’t update a project milestone from the roadmap view. Updating project milestones may impact the associated cost and resource plans of the project. So, it’s recommended to update project milestones using Project Workspace in Project Portfolio Management \(PPM\).

**Parent Topic:**[Portfolio Planning reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/portfolio-planning-reference.md)


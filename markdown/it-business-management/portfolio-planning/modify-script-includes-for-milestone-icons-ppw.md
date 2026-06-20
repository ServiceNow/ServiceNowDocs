---
title: Modify Script Includes for milestone icons in Portfolio Planning Workspace
description: Modify the Script Includes for milestone icons of the roadmap and portfolio plan to customize the icons to be shown in the Roadmap tab in the workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/portfolio-planning/modify-script-includes-for-milestone-icons-ppw.html
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-06-20"
reading_time_minutes: 1
breadcrumb: [Configuring Prioritization and Roadmap settings in Portfolio Planning, Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Modify Script Includes for milestone icons in Portfolio Planning Workspace

Modify the Script Includes for milestone icons of the roadmap and portfolio plan to customize the icons to be shown in the Roadmap tab in the workspace.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  From the list, select RoadmapMilestoneAPIImpl.

3.  Update the milestone icon type in the **Script** field of the Script Include.

    In the **getMilestoneMetadata** method, update the return value to the required icon.

    For example, if you want to display the Circle exclamation icon \(\[Omitted image "circle-exclamation-outline.png"\] Alt text: Circle exclamation outline icon.\) for key event milestone, update the return value to `'circle-exclamation-outline'` for the key\_event milestone.

    The default icons are as follows:

    -   key\_event: `'flag-fill'`
    -   launch\_date: `'rocketship-fill'`
    -   important\_date: `'calendar-clock-fill'`
    -   key\_milestone: `'diamond-fill'`
    -   deadline: `'star-fill'`
    \[Omitted image "milestone-icon-types-spw.png"\] Alt text: Milestone types in Strategic Planning.

4.  Select **Update**.


**Parent Topic:**[Configuring Prioritization and Roadmap settings in Portfolio Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/configuring-prioritization-and-roadmap-settings-in-portfolio-planning.md)


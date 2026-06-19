---
title: Modify Script Includes for milestone icons in Strategic Planning
description: Modify the Script Includes for milestone icons in the roadmap and portfolio plan to customize the icons displayed in the Roadmap tab in the workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/scenario-planning-in-spw/modify-script-includes-for-milestone-icons-spw.html
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Prioritization display settings in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Modify Script Includes for milestone icons in Strategic Planning

Modify the Script Includes for milestone icons in the roadmap and portfolio plan to customize the icons displayed in the Roadmap tab in the workspace.

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


**Parent Topic:**[Prioritization display settings in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/configuring-prioritization-and-roadmap-settings-strategic-planning.md)


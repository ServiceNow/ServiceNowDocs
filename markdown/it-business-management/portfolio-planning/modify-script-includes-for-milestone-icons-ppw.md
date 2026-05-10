---
title: Modify Script Includes for milestone icons in Portfolio Planning Workspace
description: Modify the Script Includes for milestone icons of the roadmap and portfolio plan to customize the icons to be shown in the Roadmap tab in the workspace.
locale: en-US
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-05-09"
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

    For example, if you want to display the Circle exclamation icon \(![Circle exclamation outline icon.](../../spw-roadmap/images/circle-exclamation-outline.png)\) for key event milestone, update the return value to `'circle-exclamation-outline'` for the key\_event milestone.

    The default icons are as follows:

    -   key\_event: `'flag-fill'`
    -   launch\_date: `'rocketship-fill'`
    -   important\_date: `'calendar-clock-fill'`
    -   key\_milestone: `'diamond-fill'`
    -   deadline: `'star-fill'`
    ![Milestone types in Strategic Planning.](../../spw-roadmap/images/milestone-icon-types-spw.png)

4.  Select **Update**.


**Parent Topic:**[Configuring Prioritization and Roadmap settings in Portfolio Planning](../concept/configuring-prioritization-and-roadmap-settings-in-portfolio-planning.md)


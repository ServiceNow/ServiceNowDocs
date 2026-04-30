---
title: Hierarchy view configuration in Portfolio Planning
description: Show or hide parent records of planning items shown in the Hierarchy view for high-level and regular portfolio plans by configuring system properties.
locale: en-US
release: xanadu
product: Portfolio Planning
classification: portfolio-planning
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Prioritization and Roadmap settings in Portfolio Planning, Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Hierarchy view configuration in Portfolio Planning

Show or hide parent records of planning items shown in the Hierarchy view for high-level and regular portfolio plans by configuring system properties.

-   **Display empty parent entities in the Hierarchy view**

    In the Hierarchy view of the Prioritization tab, the parent records are displayed only if they have any associated planning items.

    For example, a portfolio plan built from the Organization lens \(Company &gt; Business Unit &gt; Department\) is used to manage and track plans for Demands and Projects. So, when you switch to the Prioritization Hierarchy view, only those departments that have at least one Demand or Project associated with it are shown in the view.

    If you want to see other departments that are included in this portfolio plan but have no planning items associated to them, work with your administrator to create the system property **sn\_align\_ws.gantt\_hide\_empty\_entities** and set it to **false**.

    ![Hierarchy view showing parent records without associated planning items.](../../spw-prioritization/images/hierarchy-show-empty-entities.png)

-   **Display complete hierarchy for high-level portfolio plans**

    For high-level portfolio plans, the Hierarchy view by default shows only the hierarchy up to the parent level.

    For example, a portfolio plan built from the Strategic Investment lens \(Company &gt; Strategic priority &gt; Initiative &gt; Strategic program\) is used to manage and track plans for strategic programs. So, when you switch to the Prioritization Hierarchy view, only Strategic Priority &gt; Initiative levels are shown by default.

    If you want to see the whole hierarchy of Strategic priority &gt; Initiative &gt; Strategic program &gt; planning items, work with your administrator to create the system property **true**.

    ![Hierarchy view showing the whole hierarchy.](../../spw-prioritization/images/hierarchy-show-full.png)


**Parent Topic:**[Configuring Prioritization and Roadmap settings in Portfolio Planning](configuring-prioritization-and-roadmap-settings-in-portfolio-planning.md)


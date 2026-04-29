---
title: Perform PI planning in EAP
description: Using the Planning board of Enterprise Agile Planning, plan work for multiple teams across iterations \(for example, Big Room Planning\). Track the progress of work, create and visualize dependencies between work items, and reschedule work to react quickly to changes while confirming alignment with business priorities.
locale: en-US
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Perform PI planning in EAP

Using the Planning board of Enterprise Agile Planning, plan work for multiple teams across iterations \(for example, Big Room Planning\). Track the progress of work, create and visualize dependencies between work items, and reschedule work to react quickly to changes while confirming alignment with business priorities.

## Layout of Planning board

![ART planning board in EAP.](../images/eap-planning-board-art.png "Planning Board for an Agile Release Train (ART)")

Based on the EAP configuration, the layout of the Planning board across different team levels such as Agile Team, ART, Solution Train, or Portfolio is:

-   ART, Solution Train, and Portfolio: Two-dimensional Kanban board layout with differences in the horizontal and vertical lanes.
-   Agile Team: Simple Kanban board with work item States as the vertical lanes.

The work items are represented as cards. You can choose to display cards in the compact or full size. Full size cards have data points on them such as item Number, State, and indicators for enabler, dependencies, or blocked whereas compact cards display just the short description.

## Default grouping of work items

As you go bottom to top in an Agile structure, the cards are grouped as follows for each team:

**Important:** The team hierarchy and the iterations within teams are based on your EAP configuration. The following information applies to the default Full Configuration.

-   Agile Team: For an iteration, vertical lanes represent the State of the story.

    For example, if Sprint is the planning calendar configured for an Agile Team, the cards on the Planning Board represent the work assigned for the selected Sprint. For an Agile Team, you can see Stories on the planning board.

-   ART: For an iteration, the Story cards are horizontally grouped by child teams and vertical lanes represent the iterations of the child teams.

    If Planning Interval \(PI\) is the planning calendar configured for ART, the vertical lanes represent the Sprints within the selected PI.

-   Solution Train: Horizontally grouped by child ARTs and vertical lanes represent the state of the item.
-   Portfolio: Horizontally grouped by child Solution Trains and vertical lanes represent the state of the item.
-   If the **Dependency** toggle is enabled, you can visualize the dependencies between work items.
-   If the **Capacity** toggle is enabled, you can visualize the work load of the teams.

The Planning board for an EAP team shows only those work items that are enabled in its default configuration. For example, for an ART with Full Configuration, the Planning board shows only Features by default. If your product managers or team members want to switch to viewing other work item types such as Capabilities, Epics, or Stories, work with your admin to update the required EAP configuration details. For more information, see [Configure display of other work item types in EAP Backlog and Planning board](../task/configure-other-work-item-types-for-eap-teams-in-backlog-and-planning-board.md).

![Switch between viewing Feature and Story on ART planning board.](../images/eap-art-feature-story-switch.png)

**Tip:** For an ART, if you switch from viewing Story to another work item type on the planning board for the first time after updating this configuration, you might not have your work item cards displayed. To resolve this, ensure that the Vertical lane selection in the Planning board personalization is not set to Enterprise agile iteration.

## Layout and default grouping for Kanban teams

The Planning board for Kanban teams is grouped as follows:

-   Portfolio: Assigned work items are displayed in a two-dimensional Kanban board, with the teams as the horizontal lanes and state of the assigned work as the vertical lanes. Any work item that is not assigned to the child teams is displayed in the Portfolio section.

    ![Planning Board for an EAP portfolio of the type Kanban.](../images/eap-kanban-portfolio-planning-board.png)

-   Team: Assigned work is displayed in one-dimensional Kanban board.

As with Backlog, you can change the **Type** of work items displayed and create work items of multiple types from the Planning board.

Use the following tasks to get started with PI Planning within Enterprise Agile Planning.

-   **[Plan work for an ART in EAP](../task/plan-work-for-teams-using-planning-board-in-eap.md)**  
Plan work across all teams in an ART for multiple Planning Intervals, coordinate with different teams to manage dependencies and resolve blockers in real-time using the Planning board in Enterprise Agile Planning.
-   **[Work item dependencies in EAP](work-item-dependencies-in-eap.md)**  
Learn about work item dependencies and how they're shown on the Planning board for a team in Enterprise Agile Planning.
-   **[Personalize the EAP Planning board](../task/personalize-cards-in-eap-planning-board.md)**  
Choose metrics and indicators to be shown on cards so that key information is available at a glance on the Planning board in Enterprise Agile Planning workspace.

**Parent Topic:**[Using Enterprise Agile Planning](using-enterprise-agile-planning.md)


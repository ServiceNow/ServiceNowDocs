---
title: Manage team backlog in EAP
description: Using the Backlog page of Enterprise Agile Planning, create, update, and prioritize work items. Additionally, schedule work items into iterations such as Planning Intervals \(PI\) or Sprints.
locale: en-US
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Manage team backlog in EAP

Using the Backlog page of Enterprise Agile Planning, create, update, and prioritize work items. Additionally, schedule work items into iterations such as Planning Intervals \(PI\) or Sprints.

![EAP Backlog.](../images/eap-backlog.png)

The following sections provide a brief overview of EAP Backlog and the actions that you can perform in it.

## Layout and default grouping

The layout of Backlog across different team levels such as Agile Team, Agile Release Train \(ART\), Solution Train, or Portfolio, remains the same. The change is in the way that the work items are grouped. As you go bottom to top in an Agile structure, the work assigned to the teams is grouped as follows:

**Important:** The team hierarchy and the iterations within teams are based on your EAP configuration. The following information applies to the default Full Configuration.

-   Agile Team: Grouped by Sprints.
-   ART: Grouped by Planning Intervals.
-   Solution Train: Grouped by child ARTs.
-   Portfolio: Grouped by child Solution Trains.

Any work item that doesn't fall into any of these groups is displayed in the Backlog section.

By default, the number of iterations that the Backlog page displays is set to 6. You can work with your admin to modify this number using a system property. For more information, see [Configure the display limit of iterations in EAP Backlog](../task/configure-the-display-limit-of-iterations-in-eap-backlog.md).

## Layout and default grouping for Kanban teams

The Backlog for teams using the Kanban configuration is grouped as follows:

-   Portfolio: Assigned work items are grouped by child teams. Any work item that is not assigned to the child teams is displayed in the Backlog section.

    ![Backlog view of EAP Kanban portfolio.](../images/eap-kanban-portfolio-backlog.png)

-   Team: Assigned work is displayed in a list.

## Default work items

The work items shown in Backlog are of the Type that is mapped for this team in the configuration. As you move up in your Agile structure, the level of the work assigned also increases. At an Agile Team level, you see information of stories. As you move up through ARTs and Portfolios, you see information of Features, Capabilities, and Epics. However, at any level, you can change the type of the work items displayed.

![Work item mapping for an EAP team.](../images/eap-backlog-item-type.png)

For example, in the screenshot, **Capability** is the default item type mapped to **Compliance and onboarding tech** Solution Train based on its configuration. You can change this selection to see work of other types assigned to this team. When this selection is changed to **Feature**, you can see all the features assigned to this ART. Similarly, you can choose to create and assign a different type of work item for this Solution Train, even though its default item type is **Capability**.

View the details of any work item in the side panel by selecting its primary column. To access all the fields and related lists of the work item, select **Full details** from the side panel.

**Note:** The Backlog page for an EAP team shows only those work items that are enabled in its default configuration. For example, for an ART with Full Configuration, the Backlog might show only Features by default. If you want to view other work item types such as Capabilities, Epics, or Stories, work with your admin to update the required EAP configuration details. For more information, see [Configure display of other work item types in EAP Backlog and Planning board](../task/configure-other-work-item-types-for-eap-teams-in-backlog-and-planning-board.md).

## Column-level filtering of data

Quickly find the work items that you need by using column-level filters for the data on your EAP Backlog. Using the Column filtering option \(![](../images/eap-icon-backlog-column-filter.png)\), you can filter data on any column displayed on the **Backlog** tab, which is of the type choice, string, or reference.

![Column level filtering for EAP Backlog.](../images/eap-backlog-column-level-filters.png)

## Actions within the Backlog

Within the Backlog, you can perform the following actions:

-   Create iterations such as PIs or Sprints for your teams.
-   Add work to the team's Backlog.
-   Schedule work from Backlog into different iterations.
-   Make in-line edits to update information of work such as Status, Assigned to, or Story points.
-   Reorder planning items \(in a section\) to prioritize them.

    However, reordering is not possible when the planning items are grouped. For example you grouped the items in the Backlog section by State, you won't be able to reorder the items unless the grouping is removed.

-   Start and complete those iterations.
-   Move incomplete work to the Backlog.
-   Filter the data that's displayed.
-   Choose the columns to be displayed.
-   Open a work item in a new tab.

Use the following tasks to start creating and scheduling work for teams in EAP.

-   **[Create next PI and Sprint from EAP Backlog](../task/create-pi-sprint-eap-backlog.md)**  
Create iterations of Planning Intervals \(PI\) and Sprints so that teams can start prioritizing and scheduling their work from the Backlog in Enterprise Agile Planning \(EAP\).
-   **[Update iteration details in EAP](../task/edit-pi-sprint-iteration-details-in-eap.md)**  
Edit details of a PI or a Sprint to update details such as name, team capacity, committed points.
-   **[Create work items for teams in EAP Backlog](../task/create-work-items-for-teams-in-eap-backlog.md)**  
Create stories, features, epics, or capabilities for teams to add work to their backlog in Enterprise Agile Planning.
-   **[Breakdown work from parent work item into child items in EAP](../task/breakdown-work-eap-epics-capabilities-child-work.md)**  
Streamline breaking down work by creating child work items directly from the parent record page in Enterprise Agile Planning workspace.
-   **[Create stories for work items in EAP](../task/create-single-or-multiple-child-items-for-epic-in-eap.md)**  
Create stories directly from a work item's form. Create them manually or save time by generating them using Now Assist in the Enterprise Agile Planning \(EAP\) workspace.
-   **[Generate acceptance criteria for stories using Now Assist for Strategic Portfolio Management \(SPM\)](../task/generate-acceptance-criteria-for-eap-stories.md)**  
Create clear, comprehensive, and testable acceptance criteria for user stories without writing them manually in Enterprise Agile Planning \(EAP\). Review and refine suggested options to ensure they meet your requirements.
-   **[Create a copy of work items in EAP Backlog](../task/create-copy-of-work-items-in-eap-backlog.md)**  
For creating work items with details similar to an existing item, save time and effort by creating a copy of the existing item.
-   **[Schedule work items into iterations in EAP Backlog](../task/schedule-work-items-into-iterations-in-eap-backlog.md)**  
Perform backlog grooming and schedule work from the team's backlog for the upcoming iteration Enterprise Agile Planning.
-   **[Start or complete iterations in EAP](../task/start-or-complete-iteration-in-eap.md)**  
Start an iteration of a Sprint or PI so that your team can start working and tracking progress of work, and after your team finishes the assigned work, mark this iteration as complete, directly from the Backlog in Enterprise Agile Planning.
-   **[Add or remove teams from Favorites in EAP](../task/mark-teams-as-favorite-in-eap.md)**  
Add the EAP teams that you frequently work with to Favorites so that you can save time navigating to them in the workspace without searching for them.
-   **[Personalize and filter data in EAP Backlog](../task/personalize-and-filter-data-in-eap-backlog.md)**  
View the information that is most relevant to you and your team on the Backlog tab by choosing the columns to be displayed and applying filters to narrow down the data on the page.

**Parent Topic:**[Using Enterprise Agile Planning](using-enterprise-agile-planning.md)


---
title: Scrum program planning board
description: Use a centralized view on Agile Board to plan work for the teams that are working on your scrum program.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/agile-development/planning-scrum-program-overview.html
release: australia
product: Agile Development
classification: agile-development
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Scrum Programs for Agile Development 2.0, Agile Development, Strategic Portfolio Management]
---

# Scrum program planning board

Use a centralized view on Agile Board to plan work for the teams that are working on your scrum program.

Agile Board has a program planning board where you can plan, schedule, and review work for your scrum teams. The planning page contains the following components that guide you during your planning process.

-   **Program selector**

    Select a program that you want to plan or review. After you select a program, you can add teams or update other information by clicking the edit icon \(\[Omitted image "edit-icon.png"\] Alt text: Edit icon.\).

-   **Program timeline**

    Navigate the program timeline by scrolling horizontally or by using the forward \(\[Omitted image "calendar-forward.png"\] Alt text: Forward icon.\) and back \(\[Omitted image "calendar-backward.png"\] Alt text: Backward icon.\) icons.

-   **Epic Backlog filter**

    Select an epic backlog that is associated with your scrum program. You can filter the stories on the program planning board and the epic backlog pane. By analyzing the workload for just these selected epics, you can understand how the workload is scheduled across sprints.

-   **Configuration panel**

    Turn on or off the following components on the planning board by using the configuration panel icon \(\[Omitted image "Configuration-icon.png"\] Alt text: Configuration panel icon.\).

    -   **Team backlog**

        Enables you to show or hide the team's backlog lane.

    -   **Story dependencies**

        Enables you to visually analyze dependencies between the stories of different sprints and teams by using the story dependency lines. You can use the dependencies option to show or hide these dependency lines. If you choose to hide the dependencies or if the dependencies involve a story that's not on the board, then you can see a colored border on the story card.

        The color of the dependency indicates the way you've scheduled the stories.

        -   Green: The prerequisite story is scheduled in a sprint first. Then, the dependent story is scheduled in a later sprint.
        -   Red: The dependent story is scheduled in a sprint first. Then, the prerequisite story is scheduled in a later sprint. Review the dependency and reschedule the story as required.
        If none of the stories have a prerequisite or dependent story that is associated with them, the dependencies option is not visible.

        For information on how to add story dependencies, see [Add dependencies for Agile Development 2.0 stories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-development/Add-dependencies-to-stories.md).

-   **Epic Backlog pane**

    Enables you to see a list of all the epics that are based on the filter criteria in the epic backlog definition. For more information, see [Create an epic backlog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-development/create-epic-backlog.md).

    In the backlog pane, you can do the following actions for an epic:

    -   View the epic description.
    -   View the unassigned and unscheduled stories of the epic as cards with their short descriptions and story points.
    -   Edit the epic's information by clicking its name.
    -   Add a new story to the epic by clicking **Create Story**.
-   **Scrum teams**

    View all the teams that are involved in the selected scrum program toward the left of the planning board.

    You can update a team's information, such as the team members, group capacity, or description, by clicking the team's name.

    If your teams do not have sprints added to them, or if you want to add more sprints, you can [Add sprints from the program planning board](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-development/add-sprints-from-planning-page.md) directly.

-   **Team backlog lane**

    Enables you to see the stories that are assigned to the team but these stories aren't scheduled yet into any sprint.

    While planning your scrum program, if you know which stories must be assigned to the team but you don't know what sprints to use, you can move these stories to the team's backlog lane. By doing so, you can have a clear idea of the team's workload for the upcoming sprints and then eventually add these stories to the correct sprints.

    You can also unplan a story that has already been scheduled to a sprint by dragging the story card back to the team's backlog. Use the backlog lane on the planning board to see which team has the story. Then, decide which sprint to schedule it in.

    If you want to unassign a story from a team, you can drag the story card and drop it back into the epic backlog lane.

-   **Team sprint lanes**

    Enable you to see the sprint cadences of the teams.

    Pointing your cursor to a sprint's name shows you its details such as the duration, total story points, and filled capacity. You can edit details, such as group capacity and planned start and end dates, by clicking the sprint name.

    While planning your scrum program, if you know the sprint in which the story would be worked on, you can move the story card to that sprint.

-   **Story cards**

    Enable you to see the stories of the epics from your scrum program in the form of cards. You can move these cards around to assign them to teams and to plan them into sprints.

    If you have activated the Agile Development — Unified Backlog plugin \(com.snc.sdlc.agile.multi\_task\), you can also see stories that were added from the triage board to your unified backlog. From the planning board, you can double-click a story card to open it in a pop-up window and edit its details. If the story is created from a record on the triage board, such as a defect, you can see both the story information and the defect information side-by-side.

    **Note:** Stories can be created from enhancements, defects, incidents, or other such records only if you have activated the Agile Development — Unified Backlog plugin \(com.snc.sdlc.agile.multi\_task\).

-   **Sprint workload capacity bar**

    Plan a sprint efficiently. The bar, which is under a sprint name, indicates the workload that is planned for the team versus the team's capacity for that sprint. Pointing your cursor to the sprint name gives you additional details.

-   **Zoom in and zoom out**

    Adjust the board view using the zoom in icon \(\[Omitted image "zoom-in.png"\] Alt text: Zoom in icon.\) and the zoom out icon \(\[Omitted image "zoom-out.png"\] Alt text: Zoom out icon.\).

-   **Search**

    Filter the stories on the planning board using a search term. For example, you can enter a story number or a phrase from a short description.

-   **Stories list**

    View a list of all stories of the program using the standard list view icon \(\[Omitted image "standard-list-icon.png"\] Alt text: Standard list view icon.\).


-   **[Plan a scrum program](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-development/plan-scrum-program.md)**  
Plan work for sprints, using a centralized view on Agile Board, of multiple scrum teams that are working together on a scrum program.
-   **[Add sprints from the program planning board](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-development/add-sprints-from-planning-page.md)**  
Add sprints to your scrum teams directly from the scrum program planning board without having to navigate to another module.

**Parent Topic:**[Scrum Programs for Agile Development 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/agile-development/scrum-programs-concept.md)


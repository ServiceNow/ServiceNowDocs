---
title: SAFe PI planning board
description: Use a centralized board to plan your program increments \(PIs\) for an agile release train \(ART\). You can create and assign stories to teams, add and view story dependencies, track stories by sprints, and re-plan these stories if required.
locale: en-US
release: yokohama
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [SAFe Board — ART level, Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# SAFe PI planning board

Use a centralized board to plan your program increments \(PIs\) for an agile release train \(ART\). You can create and assign stories to teams, add and view story dependencies, track stories by sprints, and re-plan these stories if required.

The SAFe PI planning board contains the following components that guide you during your planning process.

-   **Stories and Features toggle**

    Select the **Stories** toggle to plan stories of your PI into sprints.

    Select the **Features** toggle to track the progress of all features of the PI.

-   **SAFe PI selector**

    Select a PI that you want to plan or review.

-   **Feature filter**

    Select a feature that is associated with your PI. By selecting a feature, you can filter the stories on the program planning board and on the feature backlog pane. You can analyze the workload from this feature and understand how the workload is scheduled across sprints.

-   **Story dependencies**

    Visually analyze dependencies between stories of different sprints and teams by using the story dependency lines. Use the dependencies icon \(![Dependencies icon.](../images/hide-dependencies.png)\) to show or hide these dependency lines. If you choose to hide the dependencies or if the dependencies involve a story that is not present on the board, you can see a colored border on the story card.

    The color of the dependency indicates the way you've scheduled the stories. Possible colors are the following:

    -   Green: A prerequisite story is scheduled in a sprint that's before the sprint of the dependent story.
    -   Yellow: A prerequisite story is scheduled in the same sprint as the dependent story.
    -   Red: A prerequisite story is scheduled in a sprint that's after the sprint of the dependent story. Review the dependency and reschedule the story as required.
    If none of the stories are associated with a prerequisite or dependent story, the dependencies icon \(![Dependencies icon.](../images/hide-dependencies.png)\) is not visible. For information on how to add story dependencies, see [Add dependencies to your SAFe stories](../task/add-dependencies-safe-stories.md).

-   **Feature Backlog pane**

    Use the backlog pane to view a list of all the features of the selected PI. You can do the following actions for a feature:

    -   View the description.
    -   Edit the information by clicking the feature's name.
    -   Add a new story to the feature by clicking **Create Story**.
    -   View the unassigned and unscheduled stories of this feature as cards that show the short descriptions and story points.
-   **SAFe Teams**

    View all the teams of the selected ART toward the left of the planning board. At a time, the planning board can display a maximum of 15 teams. This limit is set to ensure optimum performance of the board during planning activities.

-   **Team backlog lane**

    See the stories that are assigned to the team but that aren't scheduled yet into any sprint.

    If you know which stories must be assigned to the team but you don't know what sprints to use, then you can move these stories from the feature backlog lane to the team's backlog lane. By doing so, you can have a clear idea of the team's workload for the upcoming sprints and then eventually add these stories to the correct sprints.

    You can also unplan a story that has already been scheduled to a sprint by dragging the story card back to the team's backlog. When you later revisit the planning board, you know which team has this story and you can decide on which sprint to use.

-   **Team sprint lanes**

    See the sprint cadences of the teams.

    By pointing your cursor to a sprint's name, you can see the sprint details such as the duration, total story points, and filled capacity. You can click the sprint name to edit details such as group capacity, the planned start date, and the end date.

    While planning your PI, if you know the sprint in which the story would be worked on, then you can move the story card to that sprint.

-   **Story cards**

    See the stories of your SAFe features in the form of cards. You can move these cards around to assign them to teams and to plan them into sprints.

    If you have activated the SAFe — Unified Backlog plugin \(com.snc.sdlc.safe.multi\_task\), then you can also see stories that were added from the triage board into your unified backlog. From the PI planning board, you can double-click a story card to open it in a modal form and edit its details. If the story is created from a record on the triage board, such as an incident, then you can see both the story information and the defect information side-by-side.

    The story cards use the following indicators:

    ![SAFe PI story card legend.](../images/safe-story-cards.png "Legend for story cards on the SAFe PI Planning board")

    |Number|Indicator description|
    |------|---------------------|
    |1|Story is not complete.|
    |2|Story is complete.|
    |3|Story points.|
    |4|Story is associated with a dependent story. If this band appears in red or yellow, the color indicates that the dependency is not set correctly and needs to be reviewed.|
    |5|Story is associated with a prerequisite story. If this band appears in red or yellow, the color indicates that the dependency is not set correctly and needs to be reviewed.|
    |6|Story belongs to a feature that has this color attributed to it. Point your cursor to the dot to view the feature's name.|
    |7|Story belongs to a feature that does not have a color attributed to it. Point your cursor to the dot to view the feature's name.|
    |8|Short description of the story.|
    |9|Story is a regular story. This icon changes with the type of the story record. For example, you can create stories from incidents, enhancements, defects, problems, and other such records.|

    **Note:** Stories can be created from enhancements, defects, incidents, or other such records only if you have activated the SAFe — Unified Backlog plugin \(com.snc.sdlc.safe.multi\_task\).

-   **Sprint workload capacity bar**

    Plan a sprint efficiently by using the workload capacity bar that is located under a sprint name. The bar indicates the workload that is planned for the team versus the team's capacity for that sprint.

    If the group capacity of a sprint is zero, then you can't view the details of the sprint load and capacity.

-   **Zoom in and zoom out**

    Adjust the board view using the zoom in icon \(![Zoom in icon.](../../scrum-programs/images/zoom-in.png)\) and zoom out icon \(![Zoom out icon.](../../scrum-programs/images/zoom-out.png)\).

-   **Search**

    Filter the stories on the planning board by using a search term. For example, you can enter a story number or a phrase from a short description.

-   **Stories list**

    View the list of all stories of the program by using the standard list view icon \(![Standard list view icon.](../images/viewstandardlist.png)\).


-   **[Plan a SAFe program increment](../task/perform-bigroom-planning.md)**  
Plan your SAFe program increments \(PIs\) and track the progress of stories and features in an interactive planning board.

**Parent Topic:**[SAFe Board — ART level](program-level-tabs.md)


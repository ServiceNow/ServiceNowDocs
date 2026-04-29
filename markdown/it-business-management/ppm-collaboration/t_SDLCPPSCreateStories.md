---
title: Add stories to a project
description: Create stories and associate them to a project or add existing stories to your project.
locale: en-US
release: australia
product: PPM Collaboration
classification: ppm-collaboration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Agile Development 2.0 integration with Project Portfolio Management, Explore Project Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Add stories to a project

Create stories and associate them to a project or add existing stories to your project.

## Before you begin

Role required: it\_project\_manager

## About this task

-   The stories list displays current active stories. You can create a story from this list or view the story form for a current story. You can also add scrum tasks from the story form and view the story and task progress boards.
-   Stories can be associated to projects, but is not mandatory. While creating a story, if a project has only one phase then the story automatically gets tagged to the only phase.
-   One-off stories can be created without a link to a product or a project. One-off stories are created with only a short description, and can be assigned to a group.S
-   Stories can be added to only those projects that have the **Execution type** field set to **Hybrid** or **Agile**.

## Procedure

1.  Navigate to **All** &gt; **Projects**.

2.  Open a project that you want to add stories.

3.  From the Stories related list, select one of the following:

    -   **Add Existing** to add existing stories to this project.
    -   **New** to create a story and add it to this project.

        For information on the form fields, see the descriptions in [Story form](../../agile-development/task/create-a-story.md#table_story_form).

4.  Save the project form.


## What to do next

-   Create scrum tasks for this story. See [Create a scrum task for Agile Development 2.0 stories](../../agile-development/task/create-a-scrum-task.md).
-   Use the related links and lists of the story for more actions that you can perform. See [Related links and lists for a Story in Agile Development 2.0](../../agile-development/reference/agile-2-0-story-related-lists-related-links.md).
-   [Add dependencies for Agile Development 2.0 stories](../../scrum-programs/task/Add-dependencies-to-stories.md)
-   You can create a story with the same details as this story by using the **Insert** or **Insert and Stay** options from the story additional actions \(![Additional actions icon.](../../agile-development/image/additional-options.png)\).

    When you use **Insert and Stay**, the form of the newly created story stays open. You can modify the details of the story or create more stories with these details. On the Agile board, the new story is positioned right below the original story. The global rank of the new story is set accordingly.

    **Note:** Set the **glide.ui.task.insert** and **glide.ui.advance** properties to **true** to access these actions. These actions are not allowed on stories added from the triage board.


**Parent Topic:**[Agile Development 2.0 integration with Project Portfolio Management](../concept/c_SDLCIntegrationWithProjectPortfolioSuite.md)


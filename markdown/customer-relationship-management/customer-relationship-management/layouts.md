---
title: Layouts
description: Layouts set how a playbook's stages and activities are presented to different users in the workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 3
keywords: [Playbook layouts, horizontal layout, vertical layout, playbooks]
---

# Layouts

Layouts set how a playbook's stages and activities are presented to different users in the workspace.

Playbooks support two record page variants: a horizontal stages layout and a vertical stages layout. Both are available as page templates in UI Builder and can be activated for any CRM product that uses playbooks.

Each page variant is created from its corresponding page template and determines how the stage picker and activities are displayed to the user. The 'Active' setting combined with the page order determines which page the workspace uses to display record information.

## Stages and activities

Before choosing a layout, it helps to understand the two things a layout arranges on the page:

-   **Stage:** A sequence of activities grouped in a logical way. A playbook can contain one or more stages, and each stage includes one or more activities to complete. Stages can also include automated activities. Stages are added to a playbook in Workflow Studio.
-   **Activity:** A single step in the business process the playbook represents — a task, step, or action taken to move the process forward. Activities are grouped into stages and sequenced in a logical order. Manual activities can be completed or skipped, and some activities are completed automatically.

A layout controls how these stages and activities appear on the page. A horizontal layout runs the stages across the top of the page; a vertical layout runs them down the side. In both, the activities belonging to the selected stage appear in the work area.

## Horizontal vs vertical layouts

There are two predefined layouts that determine how users navigate through stages.

Choosing a layout affects presentation, not content — the stages, activities, and logic stay the same based on the user they are calibrated for. Horizontal works well for playbooks with a clear left-to-right progression, while vertical suits playbooks with many stages or longer activity lists.

## Horizontal stages layout

The horizontal stages page variant includes a stage picker that displays across the top of the workspace, with persistent information in the left panel. Selecting a stage reveals its activities in the activity picker, and the list of activities can be expanded or collapsed.

## Vertical stages layout

The vertical stages page variant includes a stage picker that displays in the left panel and tracks overall progress in a vertical view. Selecting a stage expands it to display the included activities.

## Stage status icons

Both page variants use the same stage status icons:

-   A check mark indicates a completed stage
-   A pen icon indicates the current stage
-   A lock icon indicates a stage that is locked and cannot be started until the previous stage is complete

## Components in a layout

A layout arranges the components a user relies on to move through a playbook. Some of these components include:

-   **Stage picker:**displays the stages in a playbook and where the user is within it, oriented horizontally or vertically, with icons that indicate the stage status.
-   **Activity picker:**displays the activities in the current stage, with indicators that show each activity's state.
-   **Activity viewer:**displays the details of the current activity, where the user performs the work to complete itA pen icon indicates the current stage.
-   **Activity card:**displays the details of the current activity within the viewer. Users work through the cards to complete each activity.

Other components such as the page header, contextual side panel, and activity stream also appear on the page and can be kept, removed, or rearranged. For the full list of playbook components, see.

## Activity viewer layouts

Independent of the stage layout, the activity view determines how activities are displayed in the playbook. There are two activity view modes, plus custom layout styles an administrator can build in UI Builder:

-   **Stacked:**Displays the stages in the playbook life cycle panel, and cards for each of the activities in the current stage in the playbook work area
-   **Focused:**Displays the stages and activities in the playbook life cycle panel, and the current activity in the playbook work area.
-   **Guided layout:**Presents activities as a step-by-step flow with back and next navigation, showing progress through the current stage.
-   **Wizard layout:**Presents the stages as sequential steps across the top of the page, with one activity shown at a time.

Stacked and Focused are set in the playbook component configuration in UI Builder. For more information, see.


---
title: Define a story in SAFe
description: Create high-level definitions of your requirements in the form of stories in SAFe.
locale: en-US
release: australia
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [SAFe entities, Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# Define a story in SAFe

Create high-level definitions of your requirements in the form of stories in SAFe.

## Before you begin

Role required: safe\_sprint\_planner, safe\_art\_user, safe\_scrum\_master, safe\_story\_editor, safe\_team\_member, or safe\_admin

## Procedure

1.  Create a story using either of the following options.

<table id="choicetable_djp_xvn_mcb"><thead><tr><th align="left" id="d94456e61">

Option

</th><th align="left" id="d94456e64">

Steps

</th></tr></thead><tbody><tr><td id="d94456e70">

**From the Story module**

</td><td>

1.  Navigate to **Scaled Agile Framework \(SAFe\)** &gt; **Stories**.
2.  Click **New**.


</td></tr><tr><td id="d94456e100">

**From the SAFe stories related list**

</td><td>

1.  Navigate to **Scaled Agile Framework \(SAFe\)** &gt; **Feature**.
2.  Click any feature.
3.  Click the **SAFe Stories** related list and click **New**.


</td></tr></tbody>
</table>2.  In the form, fill in the fields:

<table id="table_jpv_hwh_mcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated number for the story.

</td></tr><tr><td>

Feature

</td><td>

Feature to which the story belongs.

</td></tr><tr><td>

SAFe epic

</td><td>

Epic to which the story belongs.

</td></tr><tr><td>

SAFe sprint

</td><td>

Sprint in which the story is scheduled for completion.

</td></tr><tr><td>

Points

</td><td>

Number of points indicating the estimated effort required to complete the story. A larger point value indicates that a greater amount of effort is required.

</td></tr><tr><td>

State

</td><td>

State of the story. Select one of the following:-   **Draft**: In this state, the story requirements, such as the description and acceptance criteria, are still being drafted.
-   **Ready**: In this state, the story is marked as ready to be picked up by the development team.
-   **Work in Progress**: In this state, the development team works on the story and records their changes in the work notes field.
-   **Ready for Testing**: In this state, the story is marked as ready to be taken up by a tester.
-   **Testing**: In this state, the tester works on testing the story based on the requirements provided in the story.
-   **Complete**: In this state, the development and testing efforts on a story are complete.
-   **Cancelled**: In this state, a story has been cancelled.
The default state for a new story is **Draft**.

</td></tr><tr><td>

SAFe team

</td><td>

Team to which the story is assigned.

</td></tr><tr><td>

Assigned to

</td><td>

User to which the story is assigned.

</td></tr><tr><td>

Enabler

</td><td>

Check box identifying the story as an enabler. Enablers do not add direct business value but help lay a foundation for future work.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the story.

</td></tr><tr><td>

Description

</td><td>

A more detailed description of the story.

</td></tr><tr><td>

Acceptance criteria

</td><td>

The functional criteria or testing results required to move the story to the state of **Complete**.

</td></tr><tr><td>

Work notes

</td><td>

Work notes indicating the progress of the story at various stages in its life cycle.

</td></tr></tbody>
</table>3.  Click **Submit**.


## What to do next

-   Use the related links and lists of the story to create tasks for this story, or add dependencies of the current story to other stories. You can also convert this story into a SAFe feature or split this story into two, based on your requirements. For more information, see [Related links and lists for a SAFe story](../reference/related-links-and-lists-of-a-safe-story.md).
-   You can create a story with the same details as this story using the **Insert** or **Insert and Stay** options from the story additional actions \(![Additional options](../../agile-development/image/additional-options.png)\).

    When you use **Insert and Stay**, the form of the newly created story remains open so that you can modify its details, create more stories with these details, or do both.

    On SAFe Board, the new story is positioned right below the original story and the global rank of the new story is set accordingly.

    **Note:**

    -   Set the glide.ui.task.insert and glide.ui.advance properties to **true** to access these actions.
    -   These actions are not allowed on stories added from the triage board.

-   **[Related links and lists for a SAFe story](../reference/related-links-and-lists-of-a-safe-story.md)**  
Use the related links and related lists in your SAFe story form based on the actions that you need to perform on your story.
-   **[Add dependencies to your SAFe stories](add-dependencies-safe-stories.md)**  
Set dependencies to your SAFe story by adding prerequisite and dependent stories to it. Using the SAFe Planning board, you can distinguish these dependencies between stories during your big room planning and replan the stories as required.

**Parent Topic:**[SAFe entities](../concept/key-entities-SAFe.md)


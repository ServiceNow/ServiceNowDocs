---
title: Create a story in Agile Development 2.0
description: Create high-level definitions of your requirements in the form of stories in Agile Development 2.0. Manage and track your stories by associating them to a product, project, or release and by assigning them to an assignment group.
locale: en-US
release: yokohama
product: Agile Development
classification: agile-development
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Use, Agile Development 2.0, Strategic Portfolio Management]
---

# Create a story in Agile Development 2.0

Create high-level definitions of your requirements in the form of stories in Agile Development 2.0. Manage and track your stories by associating them to a product, project, or release and by assigning them to an assignment group.

## Before you begin

Role required: scrum\_story\_creator, scrum\_admin

## Procedure

1.  Navigate to **All** &gt; **Agile Development** &gt; **Stories**.

2.  Select **New**.

    Alternatively, you can create a Story from one of the following:

    -   Backlog Planning or Sprint Planning tab of the Agile board.
    -   Stories related list of a product, release, sprint, theme, or epic.
    -   Defect or enhancement record.
3.  On the form, fill in the fields.

    **Note:** Some of the fields on the Story form may appear filled depending on the option that you used to create the story.

<table id="table_story_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated number for the story.

</td></tr><tr><td>

Theme

</td><td>

Theme associated with the story. A theme can have one or more stories, but a story can belong to only one theme at a time.

 Select the theme for this story from a list of themes that are associated with the **Product** field.

</td></tr><tr><td>

Epic

</td><td>

Epic associated with the story. An epic can have one or more stories, but a story can belong to only one epic at a time.

 Select an epic for this story from the epics that are associated with the **Product** field.

</td></tr><tr><td>

Type

</td><td>

Type of story. Choose from options such as Development, Documentation, Spike, and others.

</td></tr><tr><td>

Classification

</td><td>

Type of development that the story involves. This field is automatically set to **Feature**. This field has no connection to the **Defect** and **Enhancement** fields in the **Related Records** tab.

</td></tr><tr><td>

State

</td><td>

State of the story. Select one of the following:-   **Draft**:The story requirements, such as the description and acceptance criteria, are still being drafted.
-   **Ready**: The story is ready for pickup by the development team.
-   **Work in Progress**: The development team is working on the story and recording the changes in the work notes field.
-   **Ready for Testing**: The story is ready for pickup by a tester.
-   **Testing**: The tester is testing the story based on the requirements provided in the story.
-   **Complete**: The development and testing efforts on the story are complete.
-   **Cancelled**: The story has been canceled.
This field is automatically set to **Draft**.

</td></tr><tr><td>

Points

</td><td>

Number of points that indicate the estimated effort that is required to complete the story. A larger point value indicates that the story requires a greater amount of effort.

</td></tr><tr><td>

Priority

</td><td>

Priority assigned to the story. A product owner can use priorities to rank stories in the planning board.

</td></tr><tr><td>

Product

</td><td>

Product that this story is associated with.

</td></tr><tr><td>

Release

</td><td>

Release that this story is associated with. The release can be from the releases associated with the selected product.

</td></tr><tr><td>

Assignment group

</td><td>

Agile team that the story belongs to.

</td></tr><tr><td>

Sprint

</td><td>

Sprint that this story is associated with.This field is available only when a value is selected from the **Assignment group** field.

</td></tr><tr><td>

Assigned to

</td><td>

User who is working on the story. Users on this list have appropriate scrum roles.

</td></tr><tr><td>

Demand

</td><td>

Demand that this story is associated with. When the demand is converted to project, the demand stories move from demand to project.

 When a demand is converted to a story, the reference to the demand is displayed here.

</td></tr><tr><td>

Project

</td><td>

Project that this story is associated with.

</td></tr><tr><td>

Project phase

</td><td>

Name of the agile project phase that this story is associated with. This field is available only when a value is selected from the **project** field. If a project has only one phase, then the story is automatically tagged to that phase.

 **Note:** An agile phase can have stories that belong to more than one group.

</td></tr><tr><td>

Blocked

</td><td>

An indicator to show that there are issues that prevent the story from progressing.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the story.

</td></tr><tr><td>

Description

</td><td>

A detailed description of the story.

</td></tr><tr><td>

Acceptance criteria

</td><td>

The functional criteria or testing results that are required to move this story to the Complete state.

</td></tr><tr><td>

Work notes

</td><td>

Notes about the work done for this story.

</td></tr></tbody>
</table><table id="table_gpb_bqb_ddc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Defect

</td><td>

Defect that is associated with the story. This field is a reference field from the Defect \[rm\_defect\] table. This field is required if the story is created for a defect.Click the search icon \(![Search icon](../../project-workspace/image/lookup_icon.png)\) in this field to display the existing defects or to open a new defect.

 Only users with the feature\_user role can open a defect. The admin must grant the feature\_user role to all users who are expected to open defects in the Agile Development application. This field is the only location in the Agile Development application where records from the Defect \[rm\_defect\] table appear.

 For more information on defects, see [Reporting defects in Agile Development 2.0](../concept/defect-reports.md#).

</td></tr><tr><td>

Enhancement

</td><td>

Enhancement associated with the story. This field is a reference field from the Enhancement \[rm\_enhancement\] table. This field is required if the story is created for an enhancement.Click the search icon \(![Search-icon](../../project-workspace/image/lookup_icon.png)\) in this field to display the existing enhancement requests or to open a new enhancement.

 Only users with the feature\_user role can open an enhancement. The admin must grant the feature\_user role to all users who are expected to open enhancement requests in the Agile Development application. This field is the only location in the Agile Development application where records from the Enhancement \[rm\_enhancement\] table appear.

 For more information on enhancements, see [Enhancement requests in Agile Development 2.0](../concept/enhancement-requests.md#).

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

-   The story is created and the form reopens with related links and lists.
-   The story is listed in the backlog depending on the fields filled in the story form.

## What to do next

-   Use the related links and lists of the story to create scrum tasks for this story, or convert this story into an epic or split this story into two stories. For more information, see [Related links and lists for a Story in Agile Development 2.0](../reference/agile-2-0-story-related-lists-related-links.md).
-   [Add dependencies for Agile Development 2.0 stories](../../scrum-programs/task/Add-dependencies-to-stories.md)
-   You can create a story with the same details as this story by using the **Insert** or **Insert and Stay** options from the story additional actions \(![Additional actions icon.](../image/additional-options.png)\).

    When you use **Insert and Stay**, the form of the newly created story stays open. You can modify the details of the story or create more stories with these details. On the Agile board, the new story is positioned right below the original story. The global rank of the new story is set accordingly.

    **Note:** Set the **glide.ui.task.insert** and **glide.ui.advance** properties to **true** to access these actions. These actions are not allowed on stories added from the triage board.


**Parent Topic:**[Using Agile Development 2.0](../concept/using-agile-development-2-0.md)


---
title: Report a defect in Agile Development 2.0
description: Track issues associated to your product or feature by reporting defects in Agile Development 2.0.
locale: en-US
release: zurich
product: Agile Development
classification: agile-development
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Agile Development 2.0, Strategic Portfolio Management]
---

# Report a defect in Agile Development 2.0

Track issues associated to your product or feature by reporting defects in Agile Development 2.0.

## Before you begin

Role required: feature\_user, scrum\_story\_creator, or scrum\_admin

The administrator must grant the feature\_user role to all those users who are expected to report defects using the Agile Development 2.0 application.

## About this task

Create a defect record using the Defects module. You can later create a story for this defect so that the relevant assignment group can work on resolving the issues.

## Procedure

1.  Navigate to **All** &gt; **Agile Development** &gt; **Defects**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_defect_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier for the defect.

</td></tr><tr><td>

Priority

</td><td>

Priority assigned to the defect. A product owner can use priorities when creating stories.

</td></tr><tr><td>

State

</td><td>

State of the defect. Select one of the following:-   **Draft**:The defect details are still being drafted.
-   **Scoping**: The defect is being triaged and the scope of the defect and its fix is being analyzed.
-   **Awaiting approval**: The scope of the defect is finalized and the team is awaiting approval to start working on it.
-   **Work in progress**: The team is working on the fix for the defect.
-   **Testing/QA**: The tester is testing the defect fix based on the scope provided.
-   **Deploy/Launch**: The team is ready to launch the fix for the defect.
-   **Closed Complete**: The fix for the defect is deployed into the product.
-   **On Hold**: The defect is put on hold due to any blockers and until further review.
-   **Cancelled**: The team cancels working on this defect.
This field is automatically set to **Draft**.

</td></tr><tr><td>

Assignment group

</td><td>

The group to which the defect belongs.

</td></tr><tr><td>

Assigned to

</td><td>

The user assigned to the defect.

</td></tr><tr><td>

Product

</td><td>

Product with which this defect is associated. The field is required if the defect is part of a product.

</td></tr><tr><td>

Reported against

</td><td>

Problem, change, or other task record that this defect is reported against.

</td></tr><tr><td>

Short Description

</td><td>

Brief description of the defect.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the defect.

</td></tr><tr><td>

Work notes

</td><td>

Notes about the work being performed on the defect. Work notes can be updated as the work progresses on this defect.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The defect is created and the form reopens with the Stories related list. The list of stories is only visible to users with a scrum role.

## What to do next

A scrum product owner can review the defect and decide if a story must be created for it. See [Create a story in Agile Development 2.0](create-a-story.md).

**Parent Topic:**[Using Agile Development 2.0](../concept/using-agile-development-2-0.md)


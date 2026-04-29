---
title: Related links and lists for a Story in Agile Development 2.0
description: Use the related links and related lists on the Story form for the actions that you need to perform on your story in Agile Development 2.0, such as adding scrum tasks, dependencies, or splitting the story.
locale: en-US
release: australia
product: Agile Development
classification: agile-development
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Agile Development 2.0 reference, Agile Development 2.0, Agile Development, Strategic Portfolio Management]
---

# Related links and lists for a Story in Agile Development 2.0

Use the related links and related lists on the Story form for the actions that you need to perform on your story in Agile Development 2.0, such as adding scrum tasks, dependencies, or splitting the story.

<table id="table_fvc_l4s_klb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Split Story

</td><td>

Splits the story into two stories by creating a new story with the same details. Any incomplete tasks from the old story are moved to this new story.**Note:** State of the Story cannot be **Cancelled** or **Completed**, and the **Original task** field, if present, cannot contain a non-story record such as a Catalog Task or Defect.

</td></tr><tr><td>

Add Scrum Tasks

</td><td>

Enables you to create multiple scrum tasks for the current story. The scrum tasks are listed in the Scrum Tasks related list of the story.

 For more information, see [Create multiple scrum tasks for stories in Agile Development 2.0](../task/create-multiple-scrum-tasks.md).

</td></tr><tr><td>

Convert into epic

</td><td>

Converts an active story into an epic and moves the story into the Cancelled state.If the story that you created is too large, you can convert it into an epic and then break it down into multiple stories.

-   If this story is already associated with an epic, then the story is turned into a child epic for this epic.

For example, STRY01 is converted to EPIC01. If STRY01 was associated with EPIC02, then EPIC01 becomes a child epic to EPIC02. Otherwise, EPIC01 is created as a standalone epic.

-   The state of the newly created epic is automatically set to **Draft**.
-   The canceled story is associated with the newly created epic.

</td></tr><tr><td>

Copy Story

</td><td>

Copies the details of an existing active story to a new story. The tests and tasks of the story are also copied.The state of the newly created story is automatically set to Draft.

This action is not available for stories added from the triage board.

**Note:** State of the Story cannot be **Cancelled** or **Completed**, and the **Original task** field, if present, cannot contain a non-story record such as a Catalog Task or Defect.

</td></tr></tbody>
</table><table id="table_osj_pz5_cdc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scrum Tasks

</td><td>

Lists the scrum tasks created for the story. Click **New** to create a scrum task. For more information, see [Create a scrum task for Agile Development 2.0 stories](../task/create-a-scrum-task.md).

</td></tr><tr><td>

Prerequisite Stories

</td><td>

Lists the stories that must be completed before the current story can be completed. Click **Edit** to add prerequisite stories.

</td></tr><tr><td>

Dependent Stories

</td><td>

Lists the stories that depend on the current story. Click **Edit** to add dependent stories.

</td></tr><tr><td>

Tests

</td><td>

Adds existing tests to the story.These tests are also listed on the **Sprint Tracking** tab of Agile Board after the sprint of this story starts.

</td></tr></tbody>
</table>**Parent Topic:**[Agile Development 2.0 reference](agile-development-2-reference.md)

**Related topics**  


[Create a story in Agile Development 2.0](../task/create-a-story.md)

[Writing effective stories in Agile Development 2.0](../concept/how-to-write-stories.md)


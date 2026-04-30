---
title: Manage your product backlog in Agile Development 2.0
description: Manage your product backlog from a centralized location called the Agile board in Agile Development 2.0. Add stories to a personalized backlog and prioritize them as needed.
locale: en-US
release: xanadu
product: Agile Development
classification: agile-development
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Use, Agile Development 2.0, Strategic Portfolio Management]
---

# Manage your product backlog in Agile Development 2.0

Manage your product backlog from a centralized location called the Agile board in Agile Development 2.0. Add stories to a personalized backlog and prioritize them as needed.

## Before you begin

Role required: scrum\_product\_owner

## About this task

Prioritize stories in your backlog. You can add stories, assign stories to a release or a product, add triaged records, and so on.

-   Steps 1 and 2 take you to where you can manage your scrum backlogs.
-   Steps 3 through 12 provide guidance on the different actions that you can perform on your backlog. Choose the actions based on your requirement.
-   All actions that involve a triage board are accessible only when the Agile Development — Unified Backlog plugin \(com.snc.sdlc.agile.multi\_task\) is active.

## Procedure

1.  Navigate to **All** &gt; **Agile Development** &gt; **Agile Board** &gt; **Backlog**.

    If you have already created a personalized backlog, it automatically appears in this tab. If you have not created a personalized backlog, then a welcome page appears that provides a link to create a backlog.

2.  From the list at the top-left corner, select the required backlog or create a backlog by using the Create Backlog icon \(![Create Backlog icon.](../image/createbacklog.png)\).

3.  Update the existing filter criteria of your selected backlog by using the Edit Backlog icon \(![Edit Backlog icon.](../../agile-development/image/edit-icon.png)\).

4.  Personalize columns in a list by selecting the personalize icon![Update Personalized list icon.](../../application-portfolio-management/image/personalisecolumns.png).

5.  Add a story to the backlog.

    1.  Click **Create Story**.

    2.  Specify the required details in the Story form.

    3.  Click **Submit**.

        The story is listed at the bottom of the backlog on the last page.

    If you want to add a story at a particular position in the backlog, select a story just above this position, and then click **Create Story**. The new story is listed below the story that you selected.

6.  Update a story from the backlog.

    1.  Click the story number of the story that you want to update.

    2.  Edit the story details and click **Update**.

        If you have read-only access, you can open the Story form but cannot edit the story details.

7.  Create an epic or a theme directly from the **Backlog** tab.

    1.  Select the options icon \(![options icon.](../../agile-development/image/create-story-arrow.png)\) next to the **Create Story** option.

        ![Drop down option to create story, epic, or theme on Agile board](../../agile-development/image/create-story-epic-theme-dropdown.png)

    2.  Select **Create Epic** or **Create Theme** from the list.

    3.  On the form, fill in the fields and submit it.

    The new epic is listed in the epics filter only if its stories meet the filter criteria of the selected backlog.

8.  Arrange stories within a Backlog page using one of the following options.

    -   Use the mouse device to select and hold a story, drag it to the required position, and drop it.
    -   Use the keyboard. For more information, see [Arrange Agile Development 2.0 stories in Agile Board using the keyboard](arrange-stories.md)
    Rearranging stories in the backlog adjusts the ranking of stories in the global\_rank column in the Story \[rm\_story\] table. When you move a story within a backlog, its rank changes relative to the stories within the same backlog. So, the story at the top of the backlog list has a lower rank value and assumes higher priority while the story at the bottom of the backlog list has a higher rank value and assumes lower priority.

9.  Perform any of the following actions on a single story or a set of stories by selecting the required stories and clicking the Options icon \(![Options icon.](../image/ellipsis.png)\).

    |Option|Description|
    |------|-----------|
    |**Move to top**|Moves the stories to the top of the Backlog list.|
    |**Move to next page**|Moves the stories to the top of the Backlog list on the next page.|
    |**Move to previous page**|Moves the stories to the top of the Backlog list on the previous page.|
    |**Move to page**|Moves the stories to a page of your choice. The stories are listed at the bottom of the new page that they are moved to.|
    |**Move to bottom**|Moves the stories to the bottom of the Backlog list.|
    |**Assigned to**|Opens the Users list. Select the user who you want to assign the stories to.|
    |**Assigned group**|Opens the Groups list. Select the group that you want to assign the stories to.|
    |**Epic**|Opens the Epic list. Select the epic that the stories belong to.|
    |**Product**|Opens the Product list. Select the product that the stories belong to.|
    |**Project**|Opens the Project list. Select the project that the stories belong to.|
    |**Project Phase**|Opens the Project Phase list. Select the project phase that the stories belong to.|
    |**Release**|Opens the Scrum Releases list. Select the release in which the stories are scheduled for completion.|
    |**Theme**|Opens the Theme list. Select what theme to apply on the stories.|

10. Use the **Triage Board** option to view and edit the records in your triage boards.

    You can do the following actions using the **Triage Board** option:

    -   View and edit the total number of records \(such as problems or defects\) in the triage boards of all task types
    -   Open the list of a specific task type
    -   Edit an existing triage filter definition
11. Add a triaged record, such as a defect, to the bottom of your backlog.

    1.  Click **Triage Board**.

    2.  Select your triage filter definition.

        For example, a definition for all defects.

    3.  Select the records that you want to add to your backlog.

    4.  Click **Add to Backlog**.

12. Move a triaged record from your backlog back to the triage board.

    1.  Open the triaged record by clicking its number.

    2.  Click the **Move back to triage board** related link.

    You need a specific role that provides access to a triaged record in the backlog. For example, to view a problem in the backlog, you must have the itil role. If you do not have access to any record, an error message appears.


-   **[Arrange Agile Development 2.0 stories in Agile Board using the keyboard](arrange-stories.md)**  
Learn how to use the keyboard to move and rearrange Agile Development 2.0 stories in the Backlog and Sprint Planning tabs of your Agile board.

**Parent Topic:**[Using Agile Development 2.0](../../agile-development/concept/using-agile-development-2-0.md)

**Related topics**  


[Agile board in Agile Development 2.0](../concept/agile-board.md)

[Create a personalized backlog in Agile Development 2.0](create-a-backlog.md)


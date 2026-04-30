---
title: Complete the prerequisites for converting teams to Agile Development 2.0 groups
description: Perform prerequisite steps to later ensure that the conversion of teams to Agile Development 2.0 groups is successful.
locale: en-US
release: xanadu
product: Agile Development
classification: agile-development
topic_type: task
last_updated: "2025-10-23"
reading_time_minutes: 2
breadcrumb: [Convert Agile Development 1.0 teams to Agile Development 2.0 groups, Migration from Agile Development 1.0 to Agile Development 2.0, Configure, Agile Development 2.0, Strategic Portfolio Management]
---

# Complete the prerequisites for converting teams to Agile Development 2.0 groups

Perform prerequisite steps to later ensure that the conversion of teams to Agile Development 2.0 groups is successful.

## Before you begin

Role required: admin

## About this task

**Important:** Agile Development 1.0 and its features such as Sprint burndown chart and release burndown chart are deprecated and no longer available. [Agile Development 2.0](../reference/agile-landing-page.md) provides the latest experience for supporting your Agile work methodology.

The team being selected should have at least one sprint that is current. The current sprint should have a few completed and a few WIP stories. This is to verify that the sprint burndown is updated correctly post conversion. If you do not have such a team, you may select any team for conversion.

## Procedure

1.  Find out the sprints assigned to the team across all a release.

    **Note:** Use this step to verify whether the assignment group is updated successfully across all the sprints.

    1.  In the search panel in navigator, type rm\_sprint.list to view the list of all sprints.
    2.  Display the **Team** and **Assignment group** fields if not displayed.
    3.  Apply the team name filter. The **Assignment group** field is empty.
    4.  Capture the screen or export the list of all sprints. In the sample example, sprint 5 is the current sprint for the team being converted.
    ![Sprints assigned to the team across all a release.](../image/teams-sprints.png)

2.  Find out the stories that are associated with the sprints of the team being converted.

    **Note:** Use this step to verify that the assignment group is updated successfully across all stories.

    1.  In search panel in navigator, type rm\_story.list to view the list of all stories.
    2.  Filter out the stories belonging to the sprints noted in the preceding step.
    3.  Display **Sprint.Team** and **Assignment group** fields in the list layout. The **Assignment group** field is empty.
    4.  Capture the screen or export this list.
    5.  Filter the story table to fetch the list of all stories belonging to sprints of the team being converted. Apply the following filter:

        **sprint.release\_teamSTARTSWITH&lt;name of the team&gt;**

    ![List of all stories belonging to sprints of the team being converted](../image/teams-sprints1.png)


**Parent Topic:**[Convert Agile Development 1.0 teams to Agile Development 2.0 groups](convert-teams-groups.md)


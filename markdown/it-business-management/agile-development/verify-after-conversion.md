---
title: Verify the conversion of Agile Development 1.0 teams to Agile Development 2.0 groups
description: Perform verification steps to ensure that the conversion of a team to an assignment group is successful.
locale: en-US
release: xanadu
product: Agile Development
classification: agile-development
topic_type: task
last_updated: "2025-10-23"
reading_time_minutes: 2
breadcrumb: [Convert Agile Development 1.0 teams to Agile Development 2.0 groups, Migration from Agile Development 1.0 to Agile Development 2.0, Configure, Agile Development 2.0, Strategic Portfolio Management]
---

# Verify the conversion of Agile Development 1.0 teams to Agile Development 2.0 groups

Perform verification steps to ensure that the conversion of a team to an assignment group is successful.

## Before you begin

Role required: admin

## About this task

**Important:** Agile Development 1.0 and its features such as Sprint burndown chart and release burndown chart are deprecated and no longer available. [Agile Development 2.0](../reference/agile-landing-page.md) provides the latest experience for supporting your Agile work methodology.

## Procedure

1.  Navigate to **All** &gt; **Agile Development** &gt; **Groups**.

2.  Verify that the team has been converted to an assignment group.

    If group appears here, it implies that the group type is already set to Agile Team.

    ![Group type is set to Agile Team in the screen shot](../image/agiledevelopment-groups.png)

3.  Verify that the assignment group is updated across all the sprints of the team.

    It is the same sprint list that you have noted prior to conversion. This list must have the assignment group updated after conversion.

    ![Verify that the assignment group is updated across all the sprints of the team.](../image/verify-sprints.png)

4.  Verify that the stories associated with the sprints of team have been updated with the assignment group.

    Following is the list of stories that were noted prior to converting to group:

    ![List of stories that were noted prior to converting to group](../image/verify-stories.png)

5.  Review the sprint burndown for the sprint that was noted prior to conversion.

    It must be same as it was prior to conversion.

    1.  Open the rm\_srpint table \(rm\_sprint.list\), or open the assignment group.
    2.  Click the current sprint.
    3.  Mark any WIP story as complete.
    4.  Review the sprint burndown that is to be updated with the completed story.
    ![Review the sprint burndown for the same sprint that was noted prior to conversion](../image/sprint-burndown.png) ![Burndown chart prior to conversion](../image/sprint-burndown-chart.png) ![Burndown chart progress displaying the story completed after conversion](../image/sprint-burndown-chartafter.png)

6.  Once the story is complete, the release burndown must also be updated correctly.

    For example, in the following screenshot, the burndown is updated correctly for the current release.

    ![Burndown is updated correctly for the current release](../image/burndownchart-release2.png) ![How to navigate to a release](../image/agiledevelopment-scrumreleases.png) ![Release burndown chart after conversion when one of the stories is completed](../image/agiledevelopment-releaseburndown.png)

7.  For Group Velocity:

    1.  Navigate to **Agile Development** &gt; **Groups**.
    2.  Review the velocity of the group. It must be same as it did prior to conversion.
    3.  Complete the current sprint. It must display the velocity of group for the completed sprint in addition to the sprints that were completed before conversion.
    ![How to navigate to groups](../image/agiledevelopment-groups.png)

    ![Use the Group velocity related link](../image/agiledevelopment-groupvelocity.png) ![View the group velocity chart](../image/velocitychart-agile.png)

8.  Once you verify the steps for one group, it is confirmed that the migration has completed successfully.

    You can repeat this procedure for all other teams one by one. This is a synchronous process, hence, you should perform these steps on one team at a time.


**Parent Topic:**[Convert Agile Development 1.0 teams to Agile Development 2.0 groups](convert-teams-groups.md)


---
title: Convert Agile Development 1.0 teams to Agile Development 2.0 groups
description: Complete most of the migration steps by converting teams in Agile Development 1.0 to groups in Agile Development 2.0.
locale: en-US
release: xanadu
product: Agile Development
classification: agile-development
topic_type: task
last_updated: "2025-10-23"
reading_time_minutes: 2
breadcrumb: [Migration from Agile Development 1.0 to Agile Development 2.0, Configure, Agile Development 2.0, Strategic Portfolio Management]
---

# Convert Agile Development 1.0 teams to Agile Development 2.0 groups

Complete most of the migration steps by converting teams in Agile Development 1.0 to groups in Agile Development 2.0.

## Before you begin

Complete the procedure given in [Complete the prerequisites for converting teams to Agile Development 2.0 groups](steps-prior-conversion.md).

Role required: admin

## About this task

**Important:** Agile Development 1.0 and its features such as Sprint burndown chart and release burndown chart are deprecated and no longer available. [Agile Development 2.0](../reference/agile-landing-page.md) provides the latest experience for supporting your Agile work methodology.

## Procedure

1.  Navigate to **All** &gt; **Agile Development** &gt; **Groups**.

    ![How to nàvigate to groups](../image/create-sprints.png)

    An empty list is displayed because there are no assignment groups with the type Agile Team. If there are any groups with the type Agile Team, a list of groups are displayed.

2.  Click the **Convert Release Teams to Groups** related link.

    The list of all release teams \(scrum\_pp\_team\) table that you had defined in the Agile Development plugin is displayed. If you have been defining teams for each release, multiple records are displayed for the team \(team with the same name\), one for each release. In the following screenshot, four records are displayed for the team Facilities Software Team, one for each release.

    ![Image displaying four records for the team Facilities Software Team, one for each release.](../image/teams.png)

3.  [Complete the prerequisites for converting teams to groups](steps-prior-conversion.md).

    Since migration is performed on a non-production instance first, convert one team to a group, verify if the migration is done successfully for the team, and then perform the same procedure for rest of the teams.

    In the preceding example, all the four records for the Facilities Software Team can be selected at once. Consider the Facilities Software Team team as a sample team.

4.  Select all records of the sample team and click **Convert to Group**.

    All the teams are converted to an assignment group. If an assignment group exists with the same name, a new group is not created, but other migration activities are carried out for the group, for example, updating the group reference to the sprint and story table. Perform the following steps manually:

    -   Update the group type to Agile Team.
    -   If release team members and group members are different, synchronize the members between group and team.

-   **[Complete the prerequisites for converting teams to Agile Development 2.0 groups](steps-prior-conversion.md)**  
Perform prerequisite steps to later ensure that the conversion of teams to Agile Development 2.0 groups is successful.
-   **[Verify the conversion of Agile Development 1.0 teams to Agile Development 2.0 groups](verify-after-conversion.md)**  
Perform verification steps to ensure that the conversion of a team to an assignment group is successful.

**Parent Topic:**[Migration from Agile Development 1.0 to Agile Development 2.0](../concept/migrate-agile.md)


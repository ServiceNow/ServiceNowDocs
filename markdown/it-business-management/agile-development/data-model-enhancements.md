---
title: Data model enhancements from Agile Development 1.0 to Agile Development 2.0
description: Agile Development 2.0 offers a few data model enhancements over Agile Development 1.0.
locale: en-US
release: xanadu
product: Agile Development
classification: agile-development
topic_type: reference
last_updated: "2025-10-23"
reading_time_minutes: 3
breadcrumb: [Agile Development 2.0 enhancements over Agile Development 1.0, Migration from Agile Development 1.0 to Agile Development 2.0, Configure, Agile Development 2.0, Strategic Portfolio Management]
---

# Data model enhancements from Agile Development 1.0 to Agile Development 2.0

Agile Development 2.0 offers a few data model enhancements over Agile Development 1.0.

**Important:** Agile Development 1.0 and its features such as Sprint burndown chart and release burndown chart are deprecated and no longer available. [Agile Development 2.0](agile-landing-page.md) provides the latest experience for supporting your Agile work methodology.

## Use of the common platform construct — Assignment Group

To map an agile team \(scrum team\), Agile Development 1.0 uses a separate entity called the Release Team table \( scrum\_pp\_team\). This entity is associated to a release entity as displayed in the following screen shot.

![Teams within a release](../image/scrum-release-view1.png "Scrum release")

All other tasks on platform such as incidents, problems, changes, projects rely on the assignment group entity to make assignments to a group. Group managers can run reports on an assignment group to gain insight into the work assigned to their groups.

To standardize the use of a group across platform even for scrum work such as stories and tasks, the standard construct Assignment Group is used as opposed to the standalone entity Release Team. Agile Development 2.0 uses assignment groups to map agile teams. An assignment group of type Agile Team is used for defining an agile team.

![Use of Assignment Groups in Agile Development 2.0](../image/assignmentgroups-agile2.png "Groups")

## Agile team \(group\) need not be created for each release

With Agile Development 1.0, teams are to be created for each release and the teams are to be associated to each release. For example, if a scrum team called Team — Alpha works on multiple quarterly releases. You cannot create the team for one time and associate the team to any release, or release over release. Each time a new release is created, you must create a team with the same name and associate team to the release.

With Agile Development 2.0, groups are created independent of releases, and you can work on stories from multiple releases without recreating the group for every release.

![Teams within a release](../image/scrum-release3.png "Scrum release") ![Same team is created four times, one for each release](../image/teams3.png "Scrum release")

## Sprints can be created without a release

With Agile Development 1.0, creating a release is mandatory for creating sprints. Sprints cannot be created for a team independently. Agile Development 1.0 mandates the creation of a release for story execution via sprints. If there is no release, sprint cannot be populated on a story record.

![Sprints created in the context of a release](../image/scrum-release4.png "Sprints")

In Agile Development 2.0, sprints are associated with Assignment Groups. ![Sprints are associated with Assignment Groups](../image/group4.png)

## Team backlog can be maintained independent of release

Typically, a team can have an ongoing team backlog release after release, it can pull stories from its backlog, and execute them through sprints in the release.

With Agile Development 1.0, a team cannot be defined without defining a release. Hence, team backlog cannot be maintained independent of a release.

With Agile Development 2.0, an assignment group is not created within a release. It can be associated to the release, but not created within a release. Hence, an assignment group can maintain its own backlog.

![Group backlog with Agile Development 2.0](../image/stories1.png "Group backlog with Agile Development 2.0")

## Association between Release and Group

As there is no direct relation between a release and a group in Agile Development 2.0 \(groups are independent and do not have to create groups for each release\), the m2m\_release\_group\_list table has been introduced. This table stores the association of a group with a release. This association is not used for sprint generation, but is used to derive the capacity of a release.

Specify the number of sprints for which the group works in a release. From the capacity of the team, the capacity of the release is derived.

|Team|Start Sprint|End Sprint|Points \(each sprint\)|Total Group Capacity For Release|
|----|------------|----------|----------------------|--------------------------------|
|A|A\_Sprint 1|A\_Sprint 3|30|90 \(3\*30\)|
|B|B\_Sprint 1|B\_Sprint 4|40|160 \(4\*40\)|

Total Release Capacity = 90+ 160 = 250 points

![Release — Group association in Agile Development 2.0](../image/scrum-release5.png)

**Parent Topic:**[Agile Development 2.0 enhancements over Agile Development 1.0](../concept/appendix.md)


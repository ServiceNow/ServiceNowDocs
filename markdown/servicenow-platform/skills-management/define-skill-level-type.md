---
title: Define a skill level type
description: Define skill levels \(for example, beginner, intermediate, advanced\) for different skill level types \(for example, a language or an IT certification\) so you can associate skill levels to users and define skill levels and types required for tasks.
locale: en-US
release: australia
product: Skills Management
classification: skills-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Skills Management, Skills Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Define a skill level type

Define skill levels \(for example, beginner, intermediate, advanced\) for different skill level types \(for example, a language or an IT certification\) so you can associate skill levels to users and define skill levels and types required for tasks.

## Before you begin

Role required: skill\_admin or admin

## Procedure

1.  Identify skill level types.

    You can group skills that belong to the same category into a skill level type. For example, you could use language as the skill level type if Japanese and French are defined as skills. Take an inventory of every type of skill your organization needs.

2.  Add skill level types, define skill levels, and associate them with a skill level type.

    After you add a skill level type, you can define different levels for that type of skill. For example, if you add language as a type of skill, you can associate familiar, proficient, and expert as skill levels. When you select French, for example, as a skill for a user, you will be able to define the user's skill level for French as either familiar, proficient, or expert.

    1.  Navigate to **Skills** &gt; **Skill Level Types**.

    2.  Click **New**.

    3.  Enter a name and description for the skill level type, and then right-click the form and click **Save**.

    4.  Associate skill levels with this skill type.

        By default, skill level types are associated with the **Default** skill level and have a value of 1. You can change the name and value for this default skill level. The value is used to measure skill gaps. For example, if you give a value of 10 for a skill level defined as proficient and a value of 25 for a skill level defined as expert, when you create a skill report to measure gaps, you will see a value of 15 as a measure for the skill gap.

3.  Click **Submit**.


## Example

This example shows a system administrator creating the skill level type Language, adding the skill level Proficient to that type, and associating a value for the level.

![Skill Level Type](../images/skill-level-type-new-york.gif)


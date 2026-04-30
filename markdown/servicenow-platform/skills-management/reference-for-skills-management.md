---
title: Reference for Skills Management
description: Validate that Skills Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: yokohama
product: Skills Management
classification: skills-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Skills Management, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Reference for Skills Management

Validate that Skills Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

Skills Management quick start tests require activating the Skills Management plugin \(com.snc.skills\_management\).

|Test|Description|Release version|
|----|-----------|---------------|
|Skills MGMT: User skill level inheritance when user is part of multiple groups|Verify that the user is assigned the highest skill level when the user belongs to multiple groups that have been assigned the same skills with different skill levels.|New York|
|Skills MGMT: Add skills to lowest level category|Verify that skills can be added to the lowest level category.|New York|
|Skills MGMT: Create a child category under a parent category|Verify that a lower-level category can be created when the flag for **Add skills** is unchecked in the parent category.|New York|
|Skills MGMT: Create a skill category|Verify that a skill category can be created on the skill category form.|New York|
|Skills MGMT: Create skill level type and skill levels|Define the skill level type and different skill levels for the type.|New York|
|Skill MGMT: Skill level inheritance from group to user|Verify that skill levels can be inherited from a group to the users of the group and that the **Inherited** and **Skill level inherited** fields are set to true.|New York|
|Skills MGMT: Create a skill from Manage IT Skills user interface.|Verify that you can create a skill from the Manage IT Skills user interface.|Orlando|
|Skills MGMT: Add skills and skill levels to users in the Manage IT Skills user interface.|Verify that you can add skills and associated skill levels to users in the Manage IT Skills user interface.|Orlando|
|Skills MGMT: Select a skill and add users to the skill in the Manage IT Skills user interface.|Verify that you can select a skill and add the skill and associated skill levels to one or more users in the Manage IT Skills user interface.|Orlando|
|Skills MGMT: Select a skill that does not have a skill level and add users to that skill in the Manage IT Skills user interface.|Verify that you can select a skill that does not have a skill level and add the skill to one or more users in the Manage IT skills user interface.|Orlando|


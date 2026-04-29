---
title: Configure the leader role to identify crew leaders
description: Identify a crew leader if one isn’t specified by the dispatcher by adding skills to the leader role.
locale: en-US
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Crew Operations, Set up workforce, Configure, Field Service Management]
---

# Configure the leader role to identify crew leaders

Identify a crew leader if one isn’t specified by the dispatcher by adding skills to the leader role.

## Before you begin

Role required: wm\_admin

## About this task

All crews must have a leader. Dispatchers can assign a leader to a crew or use the resource requirements to designate a skill the crew leader must have in order to be assigned as the crew leader.

If the dispatcher doesn’t assign the leader to a crew or indicate a required leader skill in the resource requirements, the skills included in the leader role are used to determine the crew leader. The skills are matched with the skills of the available agents.

For more information on adding resource requirements to a task, see [Add resource requirements for a work order task](add-resource-requirement-wot.md).

## Procedure

1.  Navigate to **All** &gt; **Skills** &gt; **All Skills**.

2.  Capture the sys\_id of the skill that you want to add to the leader role.

    1.  Right-click the name of the skill and select **Copy sys\_id**.

    2.  Paste the ID into a scratch file.

    3.  Add more than one skill to the leader role by repeating this step.

3.  Select **All** and enter `sys_properties_list.do` in the filter navigator.

    1.  In the **Name** column, search for the leader role `sn_fsm_crew.crew.leader.skill`.

    2.  Select the role name.

    **Note:** Select **here** if you see a message about editing the Global application.

4.  In the **Value** field, enter a comma after the last value and paste the skill sys\_id you copied.

5.  Select **Update**.



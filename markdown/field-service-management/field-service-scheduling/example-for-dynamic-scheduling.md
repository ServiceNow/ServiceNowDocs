---
title: Example - Dynamic Scheduling
description: Explore how Dynamic Scheduling prioritizes the best agent for a task, focusing on key matching criteria.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Dynamic Scheduling, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Example - Dynamic Scheduling

Explore how Dynamic Scheduling prioritizes the best agent for a task, focusing on key matching criteria.

Consider a scenario in which all field agents work in the same region. Since all agents are always going to be the same relative distance from a task, availability to perform a task is the most important criteria, followed by matching part requirements.

The following infographic helps you to understand how dynamic scheduling use weighting to determine the best agent to assign to a task.![An infographic that demonstrates the process and formulas of calculating an agent rank based on the matching criteria.](../image/dynamic_scheduling.png)

## Consider distance from task in addition to matching criteria

Consider how the calculation would change if the field agents weren’t all in the same, small region. When distance matters, the **Current Distance From Task** or **Distance From Task** matching criteria can be used. These distance from task criteria are unlike the other criteria because the closer the field agent is to the task, the better. Therefore, unlike the other criteria, a lower number here’s better than a higher number. The less is better adjustment is necessary to make a true comparison of the resulting scores. An adjustment is made by subtracting the score from one \(1\) for any criterion using the ranking method Less is better.

**Note:** **Distance From Task** calculation occurs in the **LocationFromTask** Script Includes and **Current Distance From Task** calculation occurs in the **CurrentLocationFromTask** Script Includes. This calculation takes the task latitude and longitude and compares it to the agent's latitude and longitude, as expressed in miles.

**Related topics**  


[Configure dynamic scheduling](../task/create-dynamic-scheduling-config.md)


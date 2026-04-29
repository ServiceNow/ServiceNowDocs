---
title: Configuring Intelligent Task Recommendations
description: Efficiently recommend tasks to agents using Intelligent Task Recommendations, a feature that aligns tasks with agents based on predefined policies and filtering conditions. Determine the applications through which you can access task recommendations.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configuring Intelligent Task Recommendations

Efficiently recommend tasks to agents using Intelligent Task Recommendations, a feature that aligns tasks with agents based on predefined policies and filtering conditions. Determine the applications through which you can access task recommendations.

## Configuration overview

The steps to set up Intelligent Task Recommendations are:

1.  Create a policy: Define a policy that governs whether a task should be recommended to a selected agent. This policy is essential for confirming that the right tasks are matched with the right agents. For more information, see [Create Task Recommendation Policies](../task/create-task-recommendation-policies.md).
2.  Map the policy to applications: Associate your policy with specific applications to enable dispatchers or agents to utilize the task recommendation feature within those applications. This association confirms that recommendations are accessible where they’re most needed. For more information, see [Map applications to Intelligent Task Recommendation policies](../task/create-task-recommendation-applicability.md).
3.  Define optional recommendation criteria: Enhance the accuracy of task recommendations by defining additional criteria. These criteria are divided into two categories. For more information, see [Predefined recommendation criteria](../reference/fsm-task-recommendation-components.md#).
    -   -   Filtering constraints filter out tasks that don’t meet the defined constraints.
-   Ranking criteria rate the tasks and apply an appropriate score.
    -   Define optional recommendation criteria: Enhance the accuracy of task recommendations by defining additional criteria. These criteria are divided into two categories:

        **Note:** Custom recommendation criteria are defined by script includes. For more information, see [Providing a script for custom task recommendation criteria](../reference/script-guidelines-recommendation-criteria.md).


**Related topics**  


[Intelligent Task Recommendation](fsm-task-recommendation.md)

[Assign work order tasks to agents using Intelligent Task Recommendation](manage-work-order-tasks-dw.md#)

[Assign tasks to yourself based on Intelligent Task Recommendation](../task/recommend-task-fsm-mobile.md)

[Intelligent Task Recommendations components](../reference/fsm-task-recommendation-components.md#)


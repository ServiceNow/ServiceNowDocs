---
title: Setting up Intelligent Task Recommendations
description: Efficiently recommend tasks to agents using Intelligent Task Recommendations, a feature that aligns tasks with agents based on predefined policies and filtering conditions. Determine the applications through which you can access task recommendations.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Setting up Intelligent Task Recommendations

Efficiently recommend tasks to agents using Intelligent Task Recommendations, a feature that aligns tasks with agents based on predefined policies and filtering conditions. Determine the applications through which you can access task recommendations.

## Configuration overview

The steps to set up Intelligent Task Recommendations are:

1.  Create a policy: Define a policy that governs whether a task should be recommended to a selected agent. This policy is essential for ensuring that the right tasks are matched with the right agents. For more information, see [Create Task Recommendation Policies](../task/create-task-recommendation-policies.md).
2.  Map the policy to applications: Associate your policy with specific applications to allow dispatchers or agents to utilize the task recommendation feature within those applications. This ensures that recommendations are accessible where they are most needed. For more information, see [Map applications to Intelligent Task Recommendation policies](../task/create-task-recommendation-applicability.md).
3.  Define optional recommendation criteria: Enhance the accuracy of task recommendations by defining additional criteria. These criteria are divided into two categories:. See [Create custom recommendation criteria](../task/create-recommendation-criteria.md) for more information.
4.  
**Note:**

-   Enhance the accuracy of task recommendations by defining additional criteria. These criteria are divided into two categories: For more information, see [Predefined recommendation criteria](../reference/fsm-task-recommendation-components.md#).
    -   Filtering constraints filter out tasks that do not meet the defined constraints.
    -   Ranking criteria rate the tasks and apply an appropriate score.
-   Custom recommendation criteria are defined by script includes. For more information, see [Providing a script for custom task recommendation criteria](../reference/script-guidelines-recommendation-criteria.md).

-   **[Activate Intelligent Task Recommendation](../task/activate-intelligent-task-recommendation.md)**  
Activate the Intelligent Task Recommendation plugin \(com.snc\_task\_recommendations\)\) for Field Service Management if you have the admin role.
-   **[Create Task Recommendation Policies](../task/create-task-recommendation-policies.md)**  
Create policies to recommend the best available work order tasks for agents based on the specified rules and conditions.
-   **[Map applications to Intelligent Task Recommendation policies](../task/create-task-recommendation-applicability.md)**  
Map applications to task recommendation policies. Provide access to these policies within those applications.
-   **[Create custom recommendation criteria](../task/create-recommendation-criteria.md)**  
Define recommendation criteria that policies can use to rank or evaluate tasks for agents.
-   **[Providing a script for custom task recommendation criteria](../reference/script-guidelines-recommendation-criteria.md)**  
Guidelines for creating scripts in recommendation criteria for an Intelligent Task Recommendation policy.

**Parent Topic:**[Setting up a Field Service scheduling method](setting-up-scheduling-methods.md)


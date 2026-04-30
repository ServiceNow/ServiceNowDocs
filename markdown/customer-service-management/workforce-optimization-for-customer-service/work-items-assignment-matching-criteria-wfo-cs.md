---
title: Matching criteria for work items in Work scheduler
description: The assignment workbench uses configurable matching criteria, such as skills and availability, to evaluate the agents in a selected group and provide an overall ranking.
locale: en-US
release: zurich
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Create a criteria for a matching rule in Work scheduler, Assigning work using Work Scheduler in Workforce Optimization for Customer Service, Using Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Matching criteria for work items in Work scheduler

The assignment workbench uses configurable matching criteria, such as skills and availability, to evaluate the agents in a selected group and provide an overall ranking.

There are three types of matching criteria:

-   **Simple Match**: creates one-to-one matching, such as matching the time zone of an agent with the time zone of a task location.
-   **Aggregate**: uses a simple query and returns an aggregate result. For an aggregate type, select a table and create a filter, and then select an aggregate field such as the **Assigned to** field. This type of query returns a set of users.
-   **Scripted**: uses a scripted query which returns a list of users.

Several matching criteria are provided with the assignment workbench:

-   **Availability Today**: Availability is calculated based on the agent's work schedule, assigned work, and personal time off. The more availability an agent has, the higher the contribution to the agent's overall rank.
-   **Matching Skills**: The number of agent skills that match the skills required for the incident. The more skills that match, the higher the contribution to the agent's overall rank.
-   **Matching Skills - Mandatory Skills Support** Calculates the number of agent skills that match the mandatory skills. It does this by filtering out all agents who do not have the mandatory skills and ranks the remaining agents. The more skills that match, the higher the contribution to the agent's overall rank.

    **Note:** If using the mandatory skills feature, use the **Matching Skills - Mandatory Skills Support** criterion to match agents with the [Configuring Mandatory Skills](../../customer-service-management/concept/configure-mandatory-skills-feature.md) identified for an incident.

-   **Assigned Incidents**: The number of incidents already assigned to this agent. The more incidents assigned, the lower the contribution to the agent's overall rank.
-   **Last Assigned**: For the sake of balancing assigned work, prioritized the agent based on the last assigned work.

To create matching criteria, select the type and use the fields related to that type to build the query. After creating matching criteria, you can create a configuration for the assignment workbench by creating a matching rule of the type **Selection criteria** and selecting the desired matching criteria.

As part of selecting the matching criteria for the workbench configuration, you can specify the following settings for each individual criterion:

-   ranking and display usage
-   ranking method
-   ranking weight
-   threshold
-   active/inactive

## Ranking and display usage

In the **Use for** field, specify how you want that matching criterion to be used:

-   Ranking and display: uses the criterion to determine agent ranking and displays it in a column on the workbench.
-   Display only: displays the criterion in a column on the workbench but does not use it to determine agent ranking.
-   Ranking only: uses the criterion to determine agent ranking but does not display it on the workbench.

## Ranking method

There are two ranking methods:

-   More is better: for example, more availability is better when determining the agent ranking.
-   Less is better: for example, fewer assigned incidents are better when determining agent ranking.

## Weight

Each matching criterion has an assigned weight. By default, the matching criteria has an assigned weight of 10. You can assign a higher weight to the criteria that's more important.

## Threshold

A threshold sets a minimum requirement for a criterion. For example, set the threshold of the Matching Skills criterion to 3 if you want to see only those agents who have at least three of the required skills for a task. For availability, set the threshold to the desired number of hours to display only those agents who have that minimum number of work hours available. You can set the threshold in the **Select Criteria** related list on the Matching Rule form. If necessary, personalize the list and add the **Threshold** column.

## Active/Inactive

There can be several matching criteria associated with the matching rule that determines the assignment workbench configuration. Each individual criterion can be set to active or inactive. Changing this setting has an immediate impact on the agent ranking. You can make this change in the **Select Criteria** related list on the Matching Rule form. If necessary, personalize the list and add the **Active** column.

## Calculating the agent ranking

The assignment workbench adds the values of the matching criteria and their respective weights and uses these values to determine the overall agent ranking.

1.  Calculate a number for each criterion.
2.  Multiply that number by the criterion weight.
3.  Divide the result by the total of all criterion.
4.  Repeat for each criterion and add the results.

The following example shows how the ranking is determined for an agent with these matching criteria values:

-   Matching Skills with Mandatory Skills Support: 5/6
-   Availability Today: 7 hours
-   Assigned Incidents: 2

Calculations:

-   **Matching Skills**: `2 / 3 = 0.666` \(with 3 being the maximum number of skills\)
-   **Availability Today**: `7 / 8 = 0.875` \(with 8 being the maximum number of hours\)
-   **Assigned Incidents**: `2 / 26 = 0.0769` \(with 26 being the total number of tasks in the table\)
-   **Weight**: each matching criteria has an equal weight of 10

```
((0.666 x 10) / Total of criterion weight (10+10+10)) + ((0.875 x 10) / Total of criterion weight (10+10+10)) + ((0.0769 x 10) / Total of criterion weight (10+10+10))
```

```
(6.66 / 30) + (8.75 / 30) + (0.769 / 30)
```

```
0.222 + 0.291 + 0.0256 = 0.53
```

This calculation is performed for each agent in the assignment group. Agents are ranked based on the value of this calculation, with the highest number earning the highest ranking.

**Parent Topic:**[Create a criteria for a matching rule in Work scheduler](../task/assignment-rules-work-scheduler-wfo-cs.md)


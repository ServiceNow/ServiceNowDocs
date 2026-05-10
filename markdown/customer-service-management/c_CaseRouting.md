---
title: Routing and assigning customer service cases
description: The case routing feature uses matching rules and assignment rules to identify customer service cases that meet certain conditions and then route those cases to customer service agents.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer, Customer Service Management]
---

# Routing and assigning customer service cases

The case routing feature uses matching rules and assignment rules to identify customer service cases that meet certain conditions and then route those cases to customer service agents.

This video covers various aspects of configuration for routing and assignment including creating assignment rules, the assignment workbench and advanced work assignment.

## Overview

Create one or more matching rules that establish specific conditions that a case must meet before it can be routed to an agent. Then use an assignment rule to route those cases to agents based on product knowledge and availability. You can also invoke the MatchingRuleProcessor API to execute the matching rules and return a list of users \(sys\_ids\).

## Matching Rules

Matching rules are based on two defined sets of conditions, one that identifies specific case attributes and another that identifies the agent resources best suited to handle cases with these attributes. Matching rules are created using the Matching Rule form.

To identify case attributes, select a table that stores the task type \(for example, the Case table\) and then use a condition builder to create one or more conditions that a case must meet before being routed. For example, you can build conditions for a specific account and product or for a specific product and priority level.

To identify an agent resource, use one of the following resource matching methods:

-   **Simple**: Select the resource name from a list of users.
-   **Advanced**: Build conditions that filter the available agent resources. These conditions can be based on user role, agent group, specific skills, work load, or agent availability.
-   **Scripted**: Create a customized script to identify agent resources.

Another resource matching method, Selection Criteria, can be used to create a matching rule with selected matching criteria for use with the assignment workbench.

## Assignment Rules

Use assignment rules to automatically assign task to users and groups. Create an assignment rule for a matching rule by selecting the **Create assignment rule** related link on the Matching Rule form. When the matching rule conditions are met, a case can be routed to a user or a group using the assignment rule. The assignment rule is applied only if the task isn’t already assigned to another user or group.

**Note:** Matching rules and assignment rules are independent records with no synchronization. If you change the **Applies to** component of the matching rule, it isn’t reflected in the assignment rule.

When you create an assignment rule, you select the following:

-   The table for the task type and the conditions that must be met before the task is assigned.
-   The user or the group to which the task is assigned.

Alternately, you can create a script to further customize the assignment rule.

-   **[Invoke the MatchingRuleProcessor API](../task/t_InvokeMatchingRuleAPI.md)**  
After you create one or more matching rules, you can invoke the MatchingRuleProcessor API and run the rules.
-   **[Reverse matching](../task/t_ReverseMatching.md)**  
Reverse matching uses the same matching rules to match tasks to a resource rather than resources to a task.

**Parent Topic:**[Customer Service Management](c_CustomerServiceManagement.md)

**Related topics**  


[Assignment rules module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_AssignmentRulesModule.md)


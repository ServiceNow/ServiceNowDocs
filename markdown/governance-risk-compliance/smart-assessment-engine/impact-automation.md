---
title: Post-assessment automations
description: Post-assessment automations, also known as post-assessment actions, in Smart Assessment Engine are actions that happen automatically after an assessment is complete. These actions use the responses from an assessment to automate tasks. Using action sets, automated actions, trigger conditions, and evaluation criteria, post-assessment actions can help your assessments be efficient, consistent, accurate, and scalable.
locale: en-US
release: yokohama
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Post-assessment automations

Post-assessment automations, also known as post-assessment actions, in Smart Assessment Engine are actions that happen automatically after an assessment is complete. These actions use the responses from an assessment to automate tasks. Using action sets, automated actions, trigger conditions, and evaluation criteria, post-assessment actions can help your assessments be efficient, consistent, accurate, and scalable.

## Post-assessment actions overview

Post-assessment actions help automate decision-making processes. You can configure them to execute rules based on specific conditions or to run automatically without any conditions. It provides a structured and user-friendly interface to set up these rules without requiring technical expertise.

Using post-assessment actions, the template designer can complete actions like updating fields, creating follow-up assessments, or generating other records automatically after an assessment is submitted. Post-assessment automation involves the following key components:

-   Action sets
-   Automated actions
-   Trigger conditions
-   Evaluation criteria

## Action sets

Action sets help you automate tasks by setting conditions and corresponding actions. By using action sets, you can confirm that the most important criteria are checked first. You can add multiple action sets in a single automation. You can also edit or delete an action set that is no longer needed. There are the following types of action sets:

-   **Conditional action set**

    Checks conditions from the **If** field in order and stops when it finds the first true condition. Then, it executes the corresponding action from the **Then** field and doesn't check the rest of the conditions.

-   **Standalone action set**

    Executes actions that happen without any specific conditions. You can add multiple actions in a single standalone action set.


## Automated actions

Automated actions, also known as subflows, are predefined sequences of actions or processes that can be executed automatically based on certain conditions. The subflows are mapped to an action category, and the action category is mapped to a template assessment category. During the runtime of the subflow, the conditions are evaluated, and the corresponding subflows are executed. For example, if a response to a question meets a defined condition, a subflow can be triggered to create or update records, send notifications, or perform other automated tasks.

## Trigger conditions

Trigger conditions are user-defined condition sets based on the assessment responses. When the condition sets are met, the automated actions are triggered. For example, if a response to a question meets a set condition defined as high risk, it might trigger an action.

## Evaluation criteria

The configured post-assessment actions are executed when the assessment is submitted.

## Benefits of post-assessment actions

-   **Efficiency**

    Post-assessment actions automate routine tasks, enabling you to focus on more strategic activities.

-   **Consistency**

    Predefined rules help ensure that actions are carried out uniformly across all assessments, maintaining standardization.

-   **Accuracy**

    Automation reduces the risk of errors that can occur during manual processing.

-   **Scalability**

    The system can handle a large volume of assessments and actions without manual intervention.



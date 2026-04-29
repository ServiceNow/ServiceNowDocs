---
title: Types of flows and when to use them
description: A decision matrix and basic definitions help you determine what type of flows to create.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Types of flows and when to use them

A decision matrix and basic definitions help you determine what type of flows to create.

## Types of flows

-   **Flow**

    A flow consists of a trigger and one or more actions.

-   **Subflow**

    A subflow consists of properties, one or more inputs, one or more outputs, a sequence of actions, and the data collected or created.


Contrary to the name, Dynamic Flow is a type of flow logic, not a type of flow.

## When to use different flows

|If...|Then create...|
|-----|--------------|
|You need a constant input to initiate a set of actions|A flow|
|You need a variable input to initiate a set of actions|A subflow|
|You want to start a flow by calling it from another flow or script|A subflow|
|You want to reuse a set actions in other flows|A subflow|
|You want to configure different types of inputs for each call|A subflow|
|You want to specify the inputs available to a subflow when it starts|A subflow|
|You want to specify the outputs available to a parent flow after a subflow ends|A subflow|
|You have a large flow with 25 or more actions and want to improve its performance and readability|Subflows|
|There are interrelated outputs or some action must be taken when all are available|Parallel subflows|
|There are not interrelated outputs or some action must be taken when all are available|Multiple flows triggered by a single event|
|You want to correct certain errors in your record data automatically|A subflow|
|You want to avoid the limit of 10 items in the error-handling-process|A subflow|
|You want to use subflow outputs to trigger automation in other flows|A subflow|

**Parent Topic:**[Flows, subflows, and actions reference](flow-designer-reference.md)


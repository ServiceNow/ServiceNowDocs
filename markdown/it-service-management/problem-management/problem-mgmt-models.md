---
title: Problem Management models
description: You can use Problem Management models to tailor processes for specific use cases.
locale: en-US
release: zurich
product: Problem Management
classification: problem-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Problem Management, IT Service Management]
---

# Problem Management models

You can use Problem Management models to tailor processes for specific use cases.

Problem Management models enable you to define:

-   States for specific use cases
-   State transitions
-   State transition conditions

The following default models are provided to replicate the non-model versions included as part of the base problem life cycle.

**Note:** The base problem life cycle is included with the Problem Management  Best Practice - Madrid - State Model \(com.snc.best\_practice.problem.madrid.state\_model\) plugin. Use the Problem Management Migration Utility [store application](https://store.servicenow.com/sn_appstore_store.do#!/store/application/d03b7539dbbb3300f21e7ffdbf9619a8) to enable this plugin and migrate your records to the base problem life cycle.

|Model|Description|
|-----|-----------|
|General|Problem process equivalent to the non-model base problem life cycle.|

|Model|Description|
|-----|-----------|
|Root cause analysis|Task process equivalent to the non-model base problem life cycle.|
|General|Task process equivalent to the non-model base problem life cycle.|

## Creating Problem Management models

You can create custom models for problems and problem tasks to extend their default models without compromising on existing capabilities. Test Problem Management models in a non-production instance first. If you have changed the base problem life cycle or life cycle actions, you must make the equivalent changes to your custom models.

To begin working with custom models, see the following topics:

-   [Create a problem model](../task/create-problem-model.md)
-   [Create a problem task model](../task/create-problem-task-model.md)
-   [Enable Problem Management models](../task/enable-problem-mgmt-models.md) \(Required only for customers upgrading to Yokohama.\)

**Note:** Any problems or problem tasks that were created before you enable Problem Management models will continue to use the non-model life cycle.

## Considerations for Problem Management models and Service Operations Workspace

The **com.snc.problem\_management.models.enabled** system property is enabled by default for new customers starting from the Yokohama release.

Upgrade customers must enable the **com.snc.problem\_management.models.enabled** system property introduced in the Xanadu release.

Before disabling Problem Management models, you must apply any additional features you have added through custom Problem Management models to your non-model life cycle.

Service Operations Workspace 6.x is based on the Xanadu release and it supports Problem Management models.

Service Operations Workspace 5.x is based on the Washington DC release and it doesn't support Problem Management models.

If you are using Service Operations Workspace 5.x and you enable Problem Management models, you will manage problems and problem tasks in the classic UI16 experience, rather than in Service Operations Workspace.

**Parent Topic:**[Exploring Problem Management](exploring-problem-management.md)


---
title: Problem Management models in Service Operations Workspace
description: You can use Problem Management models to tailor processes for specific use cases.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Problem Management in Service Operations Workspace, Manage, Service Operations Workspace for ITSM, IT Service Management]
---

# Problem Management models in Service Operations Workspace

You can use Problem Management models to tailor processes for specific use cases.

You can create custom models for problems and problem tasks to extend their default models without compromising on existing capabilities. To use these capabilities, enable the **com.snc.problem\_management.models.enabled** system property introduced in the Xanadu release. Enabling Problem Management models is optional.

Problem Management models enable you to define:

-   States for specific use cases
-   State transitions
-   State transition conditions

The following default models are provided to replicate the non-model versions included as part of the base problem life cycle. The base problem life cycle is included with the Problem Management  Best Practice - Madrid - State Model \(com.snc.best\_practice.problem.madrid.state\_model\) plugin. Use the Problem Management Migration Utility [store application](https://store.servicenow.com/sn_appstore_store.do#!/store/application/d03b7539dbbb3300f21e7ffdbf9619a8) to enable this plugin and migrate your records to the base problem life cycle.

|Model|Description|
|-----|-----------|
|General|Problem process equivalent to the non-model base problem life cycle.|

|Model|Description|
|-----|-----------|
|Root cause analysis|Problem task process equivalent to the non-model base problem life cycle.|
|General|Problem task process equivalent to the non-model base problem life cycle.|

## Enabling Problem Management models

Test Problem Management models in a non-production instance first. If you have changed the base problem life cycle or life cycle actions, you must make the equivalent changes to your custom models.

To begin working with custom models, see the following topics:

-   [Enable Problem Management models in Service Operations Workspace](../task/enable-problem-mgmt-models-sow.md)
-   [Create a problem model in Service Operations Workspace](../task/create-problem-model-sow.md)
-   [Create a problem task model in Service Operations Workspace](../task/create-problem-task-model-sow.md)

**Note:** Any problems or problem tasks that were created before you enable Problem Management models will continue to use the non-model life cycle.

## Disabling Problem Management models

Before disabling Problem Management models, you must apply any additional features you have added through custom Problem Management models to your non-model life cycle.

## Considerations for Problem Management models and Service Operations Workspace

Service Operations Workspace 6.x is based on the Xanadu release and it supports Problem Management models.

Service Operations Workspace 5.x is based on the Washington DC release and it doesn't support Problem Management models.

If you are using Service Operations Workspace 5.x and you enable Problem Management models, you will manage problems and problem tasks in the classic UI16 experience, rather than in Service Operations Workspace.

**Parent Topic:**[Problem Management in Service Operations Workspace](problem-sow.md)

**Related topics**  


[Create a problem in Service Operations Workspace](../task/create-problem-sow.md)

[Work on a problem in Service Operations Workspace](../task/work-on-problem-sow.md)

[Create a problem task in Service Operations Workspace](../task/create-problem-task-sow.md)

[Work on a problem task in Service Operations Workspace](../task/work-on-problem-task-sow.md)

[Problem Management in Service Operations Workspace reference](reference-problem-management-sow.md)


---
title: Workflow engine operation order
description: The workflow engine runs in a predefined order relative to business rules and database operations. It caches commonly-used published workflows to improve performance.The workflow engine caches commonly-used published workflows to improve performance.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow concepts, Classic Workflow, Build workflows]
---

# Workflow engine operation order

The workflow engine runs in a predefined order relative to business rules and database operations. It caches commonly-used published workflows to improve performance.

The **Run after bus. rules run** workflow property defines if a workflow is **Default** or **Deferred**.

The diagram below shows the workflow engine order of operations and when Default and Deferred flows are executed. For a more general overview of engine operation order, see Execution order of scripts and engines.

![](../image/WFEngineOrderDiagram.png "Workflow engine order diagram")

## Workflow caching

The workflow engine caches commonly-used published workflows to improve performance.

Caching significantly reduces the number of database queries per workflow. By default, the engine caches up to 300 unique workflow versions. Caching very large workflows may reduce this number as the cache size cannot exceed the Java Virtual Machine \(JVM\) heap size.

To change the maximum number of cached workflow versions, navigate to **Workflow** &gt; **Administration** &gt; **Properties** and modify the value of the **The max number of models that will be concurrently held in the LRU cache** \(**glide.workflow.model.cache.max**\) property. You must restart the instance to apply this change.


---
title: Execution Plans
description: An execution plan describes how a catalog item is procured, configured, and installed.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Catalog request fulfillment, Service Catalog configuration, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Execution Plans

An execution plan describes how a catalog item is procured, configured, and installed.

Execution plans enable you to describe simple, linear processes. Each execution plan contains one or more tasks. For example, an organization could create an execution plan for delivering a corporate standard PC that contains these tasks:

1.  Procure the PC from a supplier.
2.  Configure the PC according to requester specifications.
3.  Deliver the PC to the requester.

An execution plan is not specific to any one catalog item. There could be many different models of PC that a user can order, all using the same execution plan. It is not necessary to create a new execution plan for each individual catalog item in a mature service catalog.

**Note:** Execution plans are not as powerful or flexible as workflows, and cannot be designed using a graphical editor. Execution plans are useful in some circumstances, for example, if you want to build your processes programmatically or through imports. ServiceNow recommends using workflows for request fulfillment processes.

-   **[Create an execution plan](../task/t_CreateAnExecutionPlan.md#)**  
Administrators and catalog administrators can create and manage execution plans and the associated variable tasks.
-   **[Execution plan tasks](c_ExecutionPlanTasks.md#)**  
An execution plan contains one or more execution plan tasks, such as for obtaining approval. Execution plan tasks are assigned to a fulfillment group.
-   **[Creating execution plan tasks](c_CreatingExecutionPlanTasks.md#)**  
An execution plan contains one or more task templates. Each task template defines work that can be completed by a specific fulfillment group.
-   **[Service catalog execution plans](c_UsingExecutionPlans.md#)**  
Service catalog enables you to associate execution plans with catalog items.

**Parent Topic:**[Service Catalog request fulfillment](request-fulfillment.md)


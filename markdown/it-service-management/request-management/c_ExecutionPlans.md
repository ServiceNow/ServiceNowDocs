---
title: Execution Plans
description: An execution plan describes how a catalog item is procured, configured, and installed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/request-management/c\_ExecutionPlans.html
release: brazil
product: Request Management
classification: request-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Service Catalog request fulfillment, Configure, Request Management, IT Service Management]
---

# Execution Plans

An execution plan describes how a catalog item is procured, configured, and installed.

Execution plans enable you to describe simple, linear processes. Each execution plan contains one or more tasks. For example, an organization could create an execution plan for delivering a corporate standard PC that contains these tasks:

1.  Procure the PC from a supplier.
2.  Configure the PC according to requester specifications.
3.  Deliver the PC to the requester.

An execution plan is not specific to any one catalog item. There could be many different models of PC that a user can order, all using the same execution plan. It is not necessary to create a new execution plan for each individual catalog item in a mature service catalog.

**Note:** Execution plans are not as powerful or flexible as workflows, and cannot be designed using a graphical editor. Execution plans are useful in some circumstances, for example, if you want to build your processes programmatically or through imports. ServiceNow recommends using workflows for request fulfillment processes.

-   **[Create an execution plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/request-management/t_CreateAnExecutionPlan.md)**  
Administrators and catalog administrators can create and manage execution plans and the associated variable tasks.
-   **[Execution plan tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/request-management/c_ExecutionPlanTasks.md)**  
An execution plan contains one or more execution plan tasks, such as for obtaining approval. Execution plan tasks are assigned to a fulfillment group.
-   **[Creating execution plan tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/request-management/c_CreatingExecutionPlanTasks.md)**  
An execution plan contains one or more task templates. Each task template defines work that can be completed by a specific fulfillment group.
-   **[Service catalog execution plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/request-management/c_UsingExecutionPlans.md)**  
Service catalog enables you to associate execution plans with catalog items.
-   **[Using Service Catalog execution plans scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/request-management/c_ScptblAsmtExctnPlns.md)**  
Each Service Catalog catalog item has an associated execution plan, used whenever an item of that type is ordered; if no plan is specified, the default plan is used. This default is effective for most organizations, but your execution plan may need to vary based on additional criteria.

**Parent Topic:**[Service Catalog request fulfillment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/request-management/request-fulfillment.md)


---
title: Cost models
description: A cost model is a set of rules, methods, and metrics that tell the application how to allocate expenses to the accounts in the hierarchy.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Cost models

A cost model is a set of rules, methods, and metrics that tell the application how to allocate expenses to the accounts in the hierarchy.

Cost models are associated with allocations and reports. If you own an ITBM analyst license, then you can create several cost models and choose the one you want to run the allocation engine against.

Cost models have the following attributes which give you more control over your expense allocation:

-   **User Group**: Associate a cost model to a user group of type ITFM. Anyone with the appropriate financial model role can access the cost model \(with the associated user group\), provided the user is also part of the user group. With this association, you can restrict users who can access the cost model.
-   **Fiscal Period**: Associate a cost model to a fiscal unit. The **Fiscal Period** field in the Data Definition stage of the financial modeling is set based on the fiscal unit that you have selected in the cost model. Hence, you can perform financial model activities for different fiscal periods \(month, quarter, or a period\).
-   **Data Source**: Define the staged lines source for the cost model. Optionally, you can opt not to define a data source, in which case you can create groomed lines directly or enter the amount directly into the buckets.

If you own an ITBM analyst license you can use the prescribed cost models that the base system provides, other than the cost models that you can create. See [prescriptive cost models for shared services and business applications](preconfigured-prescriptive-cost-models.md), and [prescriptive cost models for business services and business capabilities](preconfigured-prescriptive-cost-models-two.md) for the following cost models:

-   Level 1 Costing — Shared Services
-   Level 2 Costing — Business Applications
-   Level 2 Costing — Business Services
-   Level 3 Costing — Business Capabilities

If you are using Enterprise Architecture \(formerly Application Portfolio Management\) or Service Portfolio Management \(SPM\), then you can use one of the following cost models that depends on the application that you use:

-   [Business Application Costing](financial-management-apm.md)
-   [Service Offering Costing](financial-management-spm.md)

-   **[Create a cost model from Cost Model form](../task/t_CreateACostModel.md)**  
You can create multiple cost models to process allocations. Use the Cost Model form to configure all possible settings available to the cost model.
-   **[Choose a cost model](../task/t_ChooseACostModel.md)**  
You can choose one cost model that you want to use in the workbench as you pass through all the stages.
-   **[Cost model hierarchy](c_SegmentHierarchy.md)**  
All the accounts belong to segments, which are structured in a cost model hierarchy.

**Parent Topic:**[Financial Modeling](cost-transparency-setup.md)


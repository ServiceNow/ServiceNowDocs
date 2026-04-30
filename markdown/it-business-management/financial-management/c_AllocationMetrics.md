---
title: Allocation metrics - Legacy
description: Allocation metrics contain additional instructions that the application uses to allocate expenses based on a weighted calculation or on a script. Allocation methods use metrics to perform the allocation.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Allocation metrics - Legacy

Allocation metrics contain additional instructions that the application uses to allocate expenses based on a weighted calculation or on a script. Allocation methods use metrics to perform the allocation.

Following are the types of metrics that are available:

-   **Weighted metrics** are calculations based on an aggregate value from a segment. Use weighted metrics to influence how much of an expense is allocated to a segment based on other records in the instance, such as the number of servers used by a segment or the value of depreciation on an asset. Users with the Finance Administrator role can create weighted metrics.
-   **Scripted weighted metrics** are weighted metrics in script form.
-   Scripted methods are calculations based on customizable scripts that use the allocation method API. These metrics were formerly called as scripted metrics.
-   **System metrics** are metrics that the application creates automatically when you use the workbench. These metrics are read-only and accessible by users with the Finance Administrator role. See the Using the Workbench topics for more information.

**Note:** When you use the workbench to assign expenses to accounts and segments, it creates all the rules, methods, conditions, and so on automatically. Using the workbench is the preferred method of setting up allocations, rather than using lists and forms.

Starting with the Geneva release, [fiscal periods](../task/t_ViewFiscalPeriods.md) are supported in metrics.

-   **[View, modify, and validate fiscal periods - Legacy](../task/t_ViewFiscalPeriods.md)**  
After you generate a fiscal calendar, you can view fiscal period records, modify the start and end date, deactivate a fiscal period if necessary, and validate.
-   **[Create weighted allocation metrics - Legacy](../task/t_CreateWeightedAllocationMetrics.md)**  
You can create weighted metrics using an enhanced form or a standard form.
-   **[Preview weight map - Legacy](../task/preview-weight-map.md)**  
You can preview a weight map to give you visibility of the generated metric weight map because it displays the accounts for the selected metric and the selected fiscal period with the percentage split for each account.
-   **[Create scripted allocation metrics - Legacy](../task/t_CreateScriptedAllocationMetrics.md)**  
You can create scripted metrics and methods using the standard Cost Allocation Metric form.

**Parent Topic:**[Financial Modeling - Legacy](cost-transparency-setup.md)


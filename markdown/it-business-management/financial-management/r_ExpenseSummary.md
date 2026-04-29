---
title: Expense summary - Legacy
description: The Data Definition stage of the workbench shows a summary of the expenses in the application. Icons for each type of expense and for each fiscal period shows you the state of allocation records.
locale: en-US
release: australia
product: Financial Management
classification: financial-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [The Data Definition stage - Legacy, Financial Management workbench - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Expense summary - Legacy

The Data Definition stage of the workbench shows a summary of the expenses in the application. Icons for each type of expense and for each fiscal period shows you the state of allocation records.

|Icon|Description|
|----|-----------|
|![The X icon](../image/x_icon.png)|Records do not exist.|
|![The checkmark icon](../image/checkmark.png)|Record lines exist.|
|![An empty exclamation point icon](../image/empty_exlamation_point.png)|Records changed since allocations were last generated.|
|![Filled exclamation point](../image/filled_exlamation_point.png)|Errors occurred when the application was running allocations. If you see this icon, verify all your settings in the workbench and run the allocations again.|

|Label|Description|
|-----|-----------|
|**Period**|Each period in the fiscal calendar.|
|**Staged**|If records are in the General Ledger Staged Data \[itfm\_gl\_data\_staged\] table.|
|**Cleansed**|If records are in the General Ledger Cleansed Data \[itfm\_gl\_data\_cleansed\] table.|
|**Groomed**|If records are in the Groomed General Ledger Data \[itfm\_gl\_data\_groomed\] table.|
|**Lines**|If records are in the Cost Allocation \[itfm\_cost\_allocation\] table.|

**Parent Topic:**[The Data Definition stage - Legacy](../concept/c_TheDataDefinitionStage.md)

**Related topics**  


[Choose a working set - Legacy](../task/t_ChooseAWorkingSet.md)

[Clone a cost model in the workbench - Legacy](../task/t_CreateACostModelSimple.md)


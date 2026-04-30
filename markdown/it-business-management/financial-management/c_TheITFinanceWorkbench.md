---
title: Financial Management workbench
description: The Financial Management workbench provides financial administrators with a graphical interface to allocate expenses.
locale: en-US
release: xanadu
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Financial Modeling, Financial Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Financial Management workbench

The Financial Management workbench provides financial administrators with a graphical interface to allocate expenses.

Access the workbench through the **Financial Modeling** &gt; **Workbench** module.

When you use the workbench to allocate expenses, you pass through the following stages:

![Workbench stages](../image/workbench_stages_Geneva.png "Workbench stages")

**Note:**

The data cleansing stage will not be available in the Workbench stages if you do not select a data source in the Financial Model form, as there is no financial data source to pull the expense lines from. In this case, you can enter the groomed lines directly in the sub-buckets.

## The Workbench tab

-   **Data Definition**: Select a fiscal period and cost model to work with. See [The Data Definition stage](c_TheDataDefinitionStage.md).
-   **Data Cleansing**: Remove unnecessary financial expenses and put similar expenses in the same segment. This cleansing stage gives you the opportunity to tidy up expenses in the general ledger. See [The Data Cleansing stage](c_TheDataCleansingStage.md).
-   **Bucketing**: Group related expenses into customizable buckets. See [The Bucketing stage](c_TheDataBucketingStage.md).
-   **Allocation Setup**: Assign the buckets to accounts and segments that comprise the hierarchy of accounts, and create rules that govern how segments relate to each other. See [Allocation Setup stage](c_TheAllocationSetupStage.md).
-   **Review**: Review the expense assignments you made, and then run the allocation engine to allocate expenses. See [The Allocation Review stage](c_TheAllocationReviewStage.md).

## The Cost Models tab

All cost models in the application. You can create a basic cost model from this tab and open, modify, or delete existing cost models. See [The Cost Models tab](c_TheCostModelsTab.md).

## The Configuration tab

General configuration settings, such as currency, the fiscal calendar, the main Financial Management report, and advanced actions that allow you to delete financial data. See [The Configuration tab](c_TheConfigurationTab.md).

## Threshold value for number of accounts

If you are a non-analyst licensed customer, when the number of accounts in a segment or cost model exceeds the threshold value, the **Basic Allocation Setup** option is enabled automatically.

|Parameter|Threshold value|
|---------|---------------|
|Maximum number of accounts allowed in a segment|4000|
|Total number of accounts allowed in a cost model|12000|

**Note:** Running Allocation Expenses does not work when the number of accounts exceeds the threshold value.

## Browser requirements

If you are using Internet Explorer, use version 11 or later to use the workbench. You can also use any of the other generally supported web browsers.

-   **[The Data Definition stage](c_TheDataDefinitionStage.md)**  
The Data Definition stage provides you with settings to set up the application, before you start to allocate expenses.
-   **[The Data Cleansing stage](c_TheDataCleansingStage.md)**  
The Data Cleansing stage allows you to clean up the expenses that you imported into the application.
-   **[The Bucketing stage](c_TheDataBucketingStage.md)**  
The Bucketing stage allows you to assign expenses to groups called buckets.
-   **[Allocation Setup stage](c_TheAllocationSetupStage.md)**  
The Allocate Setup stage enables you to assign expenses to accounts and segments.
-   **[The Allocation Review stage](c_TheAllocationReviewStage.md)**  
The Allocation Review stage allows you to review the allocation setup before you process the allocations.
-   **[The Cost Models tab](c_TheCostModelsTab.md)**  
The **Cost Models** tab enables you to view all the existing cost models, clone a cost model from the existing cost models, and delete cost models that you do not need.
-   **[The Configuration tab](c_TheConfigurationTab.md)**  
The Configuration tab provides you with additional settings.
-   **[Missing money logs factoring tips](../reference/error-logs-troubleshooting-tips.md)**  
The error type and the possible causes and resolution tips help you to troubleshoot the errors easily.

**Parent Topic:**[Financial Modeling](cost-transparency-setup.md)


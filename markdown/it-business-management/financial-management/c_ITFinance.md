---
title: Financial Management - Legacy
description: Use the ServiceNow Financial Management application to allocate, track, and report on expenses in your organization.
locale: en-US
release: australia
product: Financial Management
classification: financial-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Project Portfolio Management, Strategic Portfolio Management]
---

# Financial Management - Legacy

Use the ServiceNow® Financial Management application to allocate, track, and report on expenses in your organization.

**Important:**

Starting March 2021, Financial Modeling is no longer available for activation.

-   New customers: If you do not currently have the entitlement to Financial Modeling but are interested to use it, reach out to one of the Partner Store Apps. Your ServiceNow implementation partner could help you with the Partner Store App details.
-   Existing customers:
    -   If you own the entitlement to Financial Modeling but have not implemented it, reach out to one of the Partner Store Apps. Your ServiceNow implementation partner could help you with the Partner Store App details.
    -   If you own the entitlement to Financial Modeling and have already implemented it, you can continue using it. The ServiceNow Support team would continue to support you with the application, in the way that you have implemented it.

        Enhancements to the application in the future would be done only on the performance but not to the functionality.


Starting with May 2026 refresh, Financial Management documentation will no longer be published.

Watch this five-minute video to learn more about financial planning, actual expenses, and budgeting.Information about financial planning, actual expenses, and budgeting in financial management

The application provides a workbench, which is a visual tool that you can use to extract expenses from your general ledger. You can also use it to process the expenses, and map them to the functions used by IT. Various reports are also available to help you know exactly how much of your expenditures are related to IT.

The Financial Management application is available starting with the Fuji release. The modules in the Financial Management application prior to the Fuji release are included with IT Cost Management.

## How Financial Management Works

The Financial Management application uses these components:

-   The general ledger: A list of your organizational expenses.
-   The fiscal period: The time frame during which expenses were incurred. You can work with only one fiscal period at a time.
-   The cost models: The underlying records that tell the application how to allocate expenses to the accounts in the hierarchy of segments.
-   The allocation engine: The core of the application that uses your cost model to calculate expenses and determine how to allocate expenses.
-   Financial reports and dashboards: Graphical representations of the expense allocations that show you where your expenses are coming from.

With the workbench, you can choose the fiscal period, build your cost model, and run the allocation engine.

There are specific dashboards for Business Application Costing cost model that you can use to track key data relevant to your business applications.

## Requirements

The following are required to use Financial Management:

-   For all financial overview and dashboard reports to function properly, activate Report Charting v2 on your instance.
-   If you are using Internet Explorer, use version 11 or later. You can also use any of the other generally supported web browsers.

-   **[Installed with Financial Management - Legacy](../reference/r_InstalledWithITFinance.md)**  
Several components are installed with the Financial Management application.
-   **[Read-only roles for Financial Management - Legacy](../reference/user-roles-fm-apm.md)**  
You can restrict the level of access of your users with a read-only role that enables them to view the Financial Management \(FM\) dashboards. Users with the read-only role can view FM reports and the underlying tables that provide data.
-   **[Domain separation and Financial Management - Legacy](domain-separation-financial-management.md)**  
Domain separation is unsupported in Financial Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Financial Management for licensed APM users - Legacy](financial-management-apm.md)**  
If you are an Enterprise Architecture \(formerly Application Portfolio Management\) licensed user and using Financial Management, then the base system provides you with a Business Application Costing cost model that you can use to evaluate the cost of your business applications along with its prescribed metrics.
-   **[Financial Management for licensed SPM users - Legacy](financial-management-spm.md)**  
If you are a Strategic Portfolio Management \(SPM\) user and have activated Financial Management, then the base system provides you with a Service Offering Costing cost model. Use this cost model to evaluate the amount spent at each level of service. Financial Modeling allocates expenses and generates cost lines based on the level of service for a defined price.
-   **[Financial Modeling - Legacy](cost-transparency-setup.md)**  
With Financial Modeling, you can determine the allocation rules and run them automatically for all data in the future. There are several other components that you must set up before you can use the workbench to allocate expenses.
-   **[Financial Charging - Legacy](financial-reporting.md)**  
Financial charging is an integral part of financial management that helps in reporting the financial aspects of a business service to various stakeholders in the organization that consume the service such as the business unit heads, department heads, or account heads.
-   **[Quick start test for Financial Management - Legacy](../../../administer/atf-quick-start-tests/reference/quick-start-tests-itfm.md)**  
Validate that Financial Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
-   **[Financial Management Platform Analytics Solutions - Legacy](../../../use/dashboards/application-content-packs/financial-content-pack.md)**  
Platform Analytics Solutions contain preconfigured dashboards. These dashboards contain actionable data visualizations that help you improve your business processes and practices.

**Parent Topic:**[Project Portfolio Management](../../project-portfolio-suite/concept/c_ProjectPortfolioSuite.md)


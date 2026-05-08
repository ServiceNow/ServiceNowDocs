---
title: Enterprise Architecture \(EA\) and the CSDM framework
description: Use Enterprise Architecture to gain a comprehensive understanding of your organization's applications so you can identify redundancies and decrease budgetary costs. The goal of this product view is to help you to understand how Enterprise Architecture key entities work with the core CSDM framework.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Enterprise Architecture \(EA\) and the CSDM framework

Use Enterprise Architecture to gain a comprehensive understanding of your organization's applications so you can identify redundancies and decrease budgetary costs. The goal of this product view is to help you to understand how Enterprise Architecture key entities work with the core CSDM framework.

**Note:** If you do not use CSDM 5.0 or later versions, see the Rome documentation for CSDM. For implementing CSDM framework, see Implementing the CSDM framework in stages.

## Enterprise Architecture home page

**Important:**

Starting with the Xanadu release, the legacy Enterprise Architecture \(formerly Application Portfolio Management\) Home page has been deprecated. However, if you are an existing user of Enterprise Architecture \(formerly Application Portfolio Management\), you can still view the legacy Home page. If you are a new activation user, the legacy Home page is not available.

You can leverage the same features provided by the Application Portfolio Management Home page by using the Enterprise Architecture Workspace Home page. To learn more about Enterprise Architecture Workspace, see [Enterprise Architecture Workspace](../ea-workspace.md).

The Enterprise Architecture home page organizes many of the CSDM tables used by Enterprise Architecture.

-   **Business Portfolio**

    View the number of defined business capabilities that have been or will be assessed, and the number of business applications that support capabilities but are at-risk.

    For more information about using capability mapping to establish a configuration item \(CI\) relationship between the business capability and the business applications, see [Exploring a business portfolio](../manage-business-portfolio.md).

-   **Information Portfolio**

    Capture the asset information as information objects. You can connect the information object to your business applications to create an application portfolio that you can use at any time.

    The information portfolio links to the following data:

    -   Data Domains: Total number of records in the Data Domain table \[sn\_apm\_data\_domain\].
    -   Information Objects: Total number of records in the Information Object table \[cmdb\_ci\_information\_object\].
    -   Database Instances: Total number of records in the Database Instance table \[cmdb\_ci\_db\_instance\].
    -   Database Catalogs: Total number of records in the Database Catalog table \[cmdb\_ci\_db\_catalog\].
    For more information about the information portfolio and the information portfolio model, see \[product\].

-   **Application Portfolio**

    Track the applications that support your business capabilities and effectively manage them to meet the goals of your organization. The portfolio provides a list of applications with information such as their category, manufacturer, and type. Select **Applications** to navigate to the list view of business applications in your organization.

    For more information about measuring the usability, cost, quality, performance, and risk of applications, see \[product\].

-   **Technology Portfolio**

    Use metrics to measure the usability, cost, quality, performance, and risk of applications.

    For more information about technology portfolio management and how it relates to business applications, see [Manage the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace](eaw-tpm.md).


-   **[Enterprise Architecture and CSDM tables](../../reference/eaw-reference/apm-use-case.md)**  
Enterprise Architecture manages and uses CSDM tables. Several ServiceNow products benefit from and add value to Enterprise Architecture.
-   **[Enterprise Architecture use case](apm-use-case-example.md)**  
Enterprise Architecture lets you define a single, version-agnostic entity that represents all instances, technologies, and data used for planning and reporting.
-   **[Enterprise Architecture considerations](apm-use-case-trouble.md)**  
Consider these points while implementing the CSDM framework.

**Parent Topic:**[Configuring Enterprise Architecture Workspace](configure-eaw.md)

**Related topics**  


[bundle-platcap.csdm-content-frame-exploring]


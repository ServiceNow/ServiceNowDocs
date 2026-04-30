---
title: Install Sourcing and Procurement Operations
description: Install Sourcing and Procurement Operations and its dependent applications from the ServiceNow Store.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Sourcing and Procurement Operations]
breadcrumb: [Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Install Sourcing and Procurement Operations

Install Sourcing and Procurement Operations and its dependent applications from the ServiceNow Store.

## Before you begin

Role required: admin

## About this task

Install the following applications in the suggested sequence to get started with Sourcing and Procurement Operations:

1.  Finance Common Architecture \[sn\_fin\]
2.  ERP Integration Framework \[sn\_fcms\_intg\]
3.  Common Service Delivery \[sn\_spend\_sdc\]
4.  Procurement Case Management \[sn\_spend\_psd\]
5.  Source-to-Pay Workspace \[sn\_spend\_workspace\]
6.  Source-to-Pay Common Architecture \[sn\_shop\]
7.  Sourcing and Purchasing Automation \[sn\_pr\]

    **Note:** If you want to leverage the demo data, you must repair the Sourcing and Purchasing Automation plugin. You can repair it now or after you have completed installing all the plugins.

8.  Shopping Hub \[sn\_spend\_uib\]
9.  Shopping Hub Mobile \[sn\_shop\_mobile\]
10. Playbooks for Sourcing and Procurement Operations \[sn\_spend\_cp\]
11. Virtual Agent for Sourcing and Procurement Operations \[sn\_shop\_va\]
12. Natural Language Understanding Models for Sourcing and Procurement Operations \[sn\_spend\_nlu\]
13. Source-to-Pay Integration Framework \[sn\_spend\_intg\]
14. Procurement File Transfer Framework \[sn\_spend\_ftp\_intg\]
15. Performance Analytics for Sourcing and Procurement Operations \[sn\_spend\_pa\]
16. Risk Assessments Integration for Sourcing and Procurement Operations \[sn\_spend\_vrm\]
17. Project Costing for Sourcing and Procurement Operations \[sn\_spend\_ppm\]
18. Source-to-Pay Operations with Contract Management Pro \[sn\_spend\_clm\]
19. Now Assist for Sourcing and Procurement Operations \(SPO\) \[sn\_spend\_gen\_ai\]
20. Advanced Work Assignment for Source-to-Pay Operations \[sn\_spend\_awa\]
21. Process Mining for Source-to-Pay Operations \[sn\_s2p\_mining\]
22. Primary Data Integration with SAP \[sn\_sap\_data\_int\]
23. Sourcing and Procurement Operations Integration with SAP \[sn\_psm\_sap\_int\]
24. Procurement for Field Service Management

    **Note:** This application is owned by the Field Service Management team.


For more information on these applications and their dependencies, see [Application plugin installation sequence in Sourcing and Procurement Operations](../reference/application-plugin-list.md).

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  In the search bar, use the filter criteria to find the application.

    You can search for the application by its name or ID. If you can't find an application, you can request it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Select **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    If your application requires other applications, you must install them first if they are not already installed.

    If the dependent applications or plugins are not installed already, installing your application automatically installs them.

5.  Select **Load demo data** if demo data is available and you want to install it.

    Some applications include demo data, which are sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

6.  Select **Install**.


## What to do next

Review the various components installed with these installations. For details, see:

-   [Components installed with Sourcing and Procurement Operations](../reference/installed-with-FSC.md)
-   [Components installed with ERP Integration Framework](../reference/installed-with-FSC-ERP.md)
-   [Components installed with Finance Common Architecture](../reference/installed-with-finance-common.md)
-   [Properties installed with Finance Common Architecture](../reference/properties-for-finance-common.md)

-   **[Components installed with Sourcing and Procurement Operations](../reference/installed-with-FSC.md)**  
Several types of components are installed with the activation of Sourcing and Procurement Operations, including tables, user roles, and scheduled jobs.
-   **[Properties installed with Finance Common Architecture](../reference/properties-for-finance-common.md)**  
Use these properties to configure various settings in the Sourcing and Procurement Operations application.
-   **[Application plugin installation sequence in Sourcing and Procurement Operations](../reference/application-plugin-list.md)**  
The following table lists the Sourcing and Procurement Operations \(SPO\) plugins, their installation sequence, high-level descriptions, and dependencies.

**Parent Topic:**[Configure Sourcing and Procurement Operations](../concept/configuring-spo.md)

**Related topics**  


[Setting up primary data for ShoppingHub](../reference/set-up-master-data-shopping-hub.md)

[Configure punchout for third-party site purchases](configure-supplier-punchout.md)

[Configuring work prioritization](../concept/configuring-work-prioritization.md)

[Add a new button in Shopping Hub](add-new-button-shoppinghub.md)

[Customize your top suppliers on Shopping Hub](customize-top-suppliers.md)

[Configure conditions for merging purchase requisitions](config-pr-merge.md)

[Service portal configuration for ShoppingHub](../concept/service-portal-configuration-for-shoppinghub.md)

[Install ShoppingHub Mobile](install-shoppinghub-mobile.md)

[Advanced Work Assignment for Source-to-Pay Operations](../concept/awa-spo.md)


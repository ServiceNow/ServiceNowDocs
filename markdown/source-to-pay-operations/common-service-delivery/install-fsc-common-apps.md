---
title: Install the Finance and Supply Chain common applications
description: Install Finance and Supply Chain common applications and its dependent plugins from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/source-to-pay-operations/common-service-delivery/install-fsc-common-apps.html
release: yokohama
product: Common Service Delivery
classification: common-service-delivery
topic_type: task
last_updated: "2025-03-05"
reading_time_minutes: 4
breadcrumb: [Configuring FSC common applications, Finance and Supply Chain common applications, Finance and Supply Chain applications, Finance and Supply Chain]
---

# Install the Finance and Supply Chain common applications

Install Finance and Supply Chain common applications and its dependent plugins from the ServiceNow Store.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with the FSC common applications:

-   Roles
-   Tables

For more information, see [Components installed with Finance Common Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/common-service-delivery/installed-with-finance-common.md), [Components installed with Source-to-Pay Common Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/common-service-delivery/components-installed-with-source-to-pay-common-architecture.md), and [Components installed with ERP Integration Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/common-service-delivery/installed-with-FSC-ERP.md).

**Note:** Installing the SPO, SLO, or APO application also automatically installs the FSC common applications as dependent applications or plugins if they are not installed already.

Install the following applications:

-   Install Sourcing and Procurement Operations. For more information on installation, see [Install Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/activate-finance-spend-central.md) and [Install ShoppingHub Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/install-shoppinghub-mobile.md).

    For more information on the required sequence for installing application plugins, see [Application plugin installation sequence in Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/application-plugin-list.md).

-   Install Supplier Lifecycle Operations. For more information on installation, see [Install Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/supplier-lifecycle-operations/install-supp-mgmt.md) and [Install Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/supplier-lifecycle-operations/install-supp-central.md).

    For more information on the required sequence for installing application plugins, see [Application plugin installation sequence in Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/supplier-lifecycle-operations/slm-plugin-list.md).

-   Install Accounts Payable Operations. For more information on installation, see [Install Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/accounts-payable-operations/install-acc-pay-mgmt.md), [Install Invoice Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/accounts-payable-operations/install-invoice-case-mgmt.md) and [Install Accounts Payable Operations integration with Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/accounts-payable-operations/apm-integration-docintel.md).

    For more information on the required sequence for installing application plugins, see [Application plugin installation sequence in Accounts Payable Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/accounts-payable-operations/application-plugin-installation-sequence-apo.md).


## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


-   **[Components installed with Finance Common Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/common-service-delivery/installed-with-finance-common.md)**  
Several types of components are installed with the installation of the Finance Common Architecture application, including tables and user roles.
-   **[Components installed with Source-to-Pay Common Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/common-service-delivery/components-installed-with-source-to-pay-common-architecture.md)**  
Several types of components are installed with the installation of the Source-to-Pay Common Architecture application, including tables and user roles.
-   **[Components installed with ERP Integration Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/common-service-delivery/installed-with-FSC-ERP.md)**  
Several types of components are installed with the installation of the ERP Integration Framework application, including tables and user roles.

**Parent Topic:**[Configuring FSC common applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/common-service-delivery/config-fsc-common-apps.md)


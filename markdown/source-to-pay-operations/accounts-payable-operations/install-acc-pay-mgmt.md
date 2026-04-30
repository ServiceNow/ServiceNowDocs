---
title: Install Accounts Payable Invoice Processing
description: You can install the Accounts Payable Invoice Processing \(com.sn\_ap\_apm\) application if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Install Accounts Payable Invoice Processing

You can install the Accounts Payable Invoice Processing \(com.sn\_ap\_apm\) application if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the Accounts Payable Invoice Processing application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   The Accounts Payable Invoice Processing \(com.sn\_ap\_apm\) application installs the following dependent plugins:
    -   Invoice Case Management \(com.sn\_ap\_cm\)
    -   Accounts Payable Operations integration with Document Intelligence \(com.sn\_ap\_ic\)

Role required: admin

## About this task

The following items are installed with Accounts Payable Operations:

-   Plugins
-   Roles
-   Flows
-   Tables

For more information, see [Components installed with Accounts Payable Invoice Processing](../reference/installed-with-acc-pay-mgmt.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Accounts Payable Operations application \(com.sn\_ap\_apm\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


-   **[Components installed with Accounts Payable Invoice Processing](../reference/installed-with-acc-pay-mgmt.md)**  
Several types of components are installed with activation of the Accounts Payable Invoice Processing plugin, including user roles, flows, and tables.

**Parent Topic:**[Configuring Accounts Payable Operations](../concept/config-acc-pay-mgmt.md)

**Related topics**  


[Install Invoice Case Management](install-invoice-case-mgmt.md)

[Install Accounts Payable Operations integration with Document Intelligence](../concept/apm-integration-docintel.md)

[Domain separation and Accounts Payable Operations](../concept/apm-domain-separation.md)


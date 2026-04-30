---
title: Install Supplier Case Management
description: You can install the Supplier Case Management application \(com.snc.sn\_supplier\_mgmt\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Install Supplier Case Management

You can install the Supplier Case Management application \(com.snc.sn\_supplier\_mgmt\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

**Important:** Check your entitlements to determine whether you have access to Supplier Case Management.

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Supplier Case Management](https://store.servicenow.com/sn_appstore_store.do#!/store/application/2516c903c33030103622aaafc840ddfc) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   The Supplier Case Management application \(com.snc.sn\_supplier\_mgmt\) installs the following dependent plugins.
    -   Supplier Common Architecture \(com.snc.sn\_slm\)
    -   Source-to-Pay Workspace \(com.sn\_spend\_workspace\)

Role required: admin

## About this task

The following items are installed with Supplier Case Management:

-   Plugins
-   Store applications
-   Roles
-   Tables

For more information, see [Components installed with Supplier Case Management](../reference/installed-with-supp-mgmt.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Supplier Case Management application \(sn\_supplier\_mgmt\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


-   **[Components installed with Supplier Case Management](../reference/installed-with-supp-mgmt.md)**  
Several types of components are installed with activation of Supplier Case Management, including tables and user roles.
-   **[Explicit Roles in Supplier Case Management](../concept/slo-explicit-roles-plugin.md)**  
You can grant access to your instance to both internal and external users. However, it is important to differentiate their access levels for added security. To achieve this, every user must have at least one role, allowing the instance to distinguish between internal and external users.
-   **[Application plugin installation sequence in Supplier Case Management](../reference/slm-plugin-list.md)**  
The following table provides the list of plugins for Supplier Case Management, a high-level description of each plugin, and the dependencies that are required before installing each plugin.
-   **[Prerequisites for upgrading Supplier Case Management to Washington DC or later releases](../concept/smw-upgrade.md)**  
Starting with the Washington DC release, Supplier Manager Workspace is being prepared for future deprecation. It will be hidden from the navigation and no longer be activated on new instances but will continue to be supported. Source-to-Pay Workspace provides the latest experience for this functionality.
-   **[Configure properties for Supplier Case Management](../reference/config-prop-supp-mgmt.md)**  
Use these properties to configure settings for the Supplier Case Management application from the Properties page.
-   **[Post-upgrade tasks for Supplier Case Management](../concept/post-upgrade-tasks-slo.md)**  
After you upgrade to Washington DC, you must review all the post-upgrade tasks and complete them as needed.

**Parent Topic:**[Configure Supplier Lifecycle Operations](../concept/config-supp-mgmt.md)

**Related topics**  


[Install Supplier Collaboration Portal](install-supp-central.md)

[Install Supplier Operations](install-supplier-ops.md)

[Install Supplier Payment Optimization](install-supp-payment-opt.md)

[Supplier Document Management](../concept/supp-doc-mgmt-overview.md)

[Configure the document template for the Sign document action type for supplier task](configure-pdf-template-sign-doc-task.md)

[Advanced Work Assignment for Supplier Lifecycle Operations](../concept/supplier-awa.md)

[Enable M2M mapping between supplier contact and suppliers](enable-m2m-supplier-contacts.md)

[Configure Supplier Relationship and Performance Management](../concept/configuring-supplier-performance-mgmt.md)

[Install Universal Request for SLO](install-universal-request.md)

[Configure smart assessments](../concept/configure-smart-assessments.md)

[Components installed with Supplier Case Management](../reference/installed-with-supp-mgmt.md)

[Application plugin installation sequence in Supplier Case Management](../reference/slm-plugin-list.md)


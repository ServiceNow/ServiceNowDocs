---
title: Install Purchase Order Management
description: If you have the admin role, install the Purchase Order Management application \(com.snc.sn\_poem\_core\). The application includes demo data and installs related ServiceNow Store applications and plugins if they aren’t already installed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [install POM application, Install Purchase Order Management, how to install Purchase order management]
breadcrumb: [Configure, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Install Purchase Order Management

If you have the admin role, install the Purchase Order Management application \(com.snc.sn\_poem\_core\). The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren’t already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the Purchase Order Management listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Install Sourcing and Purchasing Automation plugin \(com.snc.sn\_pr\) before installing Purchase Order Management.
-   Select **Load demo data** option when you install Sourcing and Purchasing Automation.

Role required: admin

## About this task

The following items are installed with Purchase Order Management:

-   Roles
-   Tables

## Procedure

1.  Navigate to **Admin** &gt; **Application Manager**.

2.  Find the Purchase Order Management application \(com.snc.sn\_poem\_core\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.


-   **[Components installed with Purchase Order Management](../reference/installed-with-purch-ord-mgmt.md)**  
Several types of components are installed with the activation of the Purchase Order Management plugin, including roles and tables.
-   **[Application plugin installation sequence in Purchase Order Management](../reference/app-plugin-install-seq-purch-ord-mgmt.md)**  
View the consolidated list of plugins, high-level description of each plugin, and the dependencies that are required before installing each plugin in Purchase Order Management.

**Parent Topic:**[Configure Purchase Order Management](../concept/configure-purch-order-mgmt.md)

**Related topics**  


[Assigning priority to a purchase order](../concept/assigning-priority-to-po.md)

[Assigning purchase order exceptions to buyers](../concept/assigning-po-exceptions-to-buyers.md)

[Domain separation and Purchase Order Management](../concept/domain-separation-pom.md)


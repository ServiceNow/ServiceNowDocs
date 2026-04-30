---
title: Install Finance Case Management
description: Install the Finance Case Management application \(sn\_fin\_ops\) if you have the admin role. The application includes demo data and installs related ServiceNow Store Store applications and plugins if they are not already installed.
locale: en-US
release: zurich
product: Finance Case Management
classification: finance-case-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Finance Case Management, Finance and Supply Chain applications, Finance and Supply Chain]
---

# Install Finance Case Management

Install the Finance Case Management application \(sn\_fin\_ops\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store Store applications and plugins if they are not already installed.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the Finance Case Management listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with Finance Case Management:

-   Plugins
-   Roles
-   Tables

The Finance Case Management application \(sn\_fin\_ops\) installs the following dependent plugins:

-   Finance Operations Workspace \(sn\_fin\_ops\_ws\)
-   Common Service Delivery \(sn\_spend\_sdc\)

## Procedure

1.  Navigate to **Admin** &gt; **Application Manager**.

    ![Menu path to Application Manager](../image/fin-case-mgmt-installation.png)

2.  Find the Finance Case Management application \(sn\_fin\_ops\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.

    Select the **Installed** tab and see the installed application and dependent plugins.![List of installed application and dependent plugins](../image/fin-case-mgmt-installed-apps.png)


-   **[Components installed with Finance Case Management](../reference/installed-with-fin-ops.md)**  
Several types of components are installed with the activation of the Finance Case Management plugin, including roles, flows, and tables.

**Parent Topic:**[Configure Finance Case Management](../concept/config-fin-case-mgmt.md)

**Related topics**  


[Configure Finance Operations Workspace](../concept/configuring-fin-ops-ws.md)


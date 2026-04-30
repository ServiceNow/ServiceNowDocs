---
title: Install Planned Work Management
description: You can install the Planned Work Management application \(com.snc.fsm\_planned\_work\_management\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Planned Work Management, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Install Planned Work Management

You can install the Planned Work Management application \(com.snc.fsm\_planned\_work\_management\) if you have the admin role.The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Activation of Planned Work Management activates the following plugins if not already active.
    -   **Required ServiceNow plugins**
        -   **Template Management for Field Service \(com.snc.fsm\_template\_management\)**

            Enables you to configure and manage the work order templates to dynamically create work orders. For more information, see [Activate Template Management for Field Service](activate-template-management.md).

        -   **Planned Maintenance \(com.snc.planned\_maintenance\)**

            Enables you to manage the regular preventive maintenance of assets. For more information, see [Activate Planned Maintenance](https://www.servicenow.com/docs/access?context=t_ActivatePlanMaint&version=yokohama&pubname=yokohama-service-management-for-the-enterprise&ft:locale=en-US).

        -   **Field Service Management \(com.snc.work\_management\)**

            Enables you to manage work requests that are performed on location by field service agents. For more information, see [Activate Field Service Management](../../planning-and-policy/task/t_ActivateFieldServiceManagement.md).

        -   **CSM and FSM Configurable Workspace Foundation \(com.snc.uib.cwf\_workspace\)**

            Enables you to access and manage Planned Work Management home page and Planning calendar.


Role required: admin

## About this task

The following items are installed with Planned Work Management:

-   Plugins
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Planned Work Management Components](../reference/planned-work-components.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Planned Work Management application \(com.snc.fsm\_planned\_work\_management\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.



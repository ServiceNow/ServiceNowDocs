---
title: Install Order Management
description: You can install the Order Management application \(sn\_ind\_tmt\_orm\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Order management, Configure, Sales Customer Relationship Management]
---

# Install Order Management

You can install the Order Management application \(sn\_ind\_tmt\_orm\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Order Management](https://store.servicenow.com/store/app/813bab2a1b246a50a85b16db234bcb8e) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with Order Management:

-   Roles
-   Tables

For more information, see [Components installed with Order Management](../reference/components-installed-with-order-management.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Order Management application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    -   Order Management \(sn\_ind\_tmt\_orm\): Select this app to install the Order Management application.
    -   Order Management for Telecommunications, Media, and Technology \(sn\_om\_tmt\): Select this app if you have a Telecommunications Service Management subscription. This installs the Order Management application, and the Telecommunication Open APIs \(sn\_tmf\_api\) for the TM Forum API REST specifications: Product Catalog, Service Catalog, Product Order, Service Order, Product Inventory, and Technical Service Qualification.
    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Parent Topic:**[Configuring Order Management](../concept/order-mgt-configuring.md)


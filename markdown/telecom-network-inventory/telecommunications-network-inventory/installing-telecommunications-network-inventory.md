---
title: Install Telecommunications Network Inventory
description: If you have the admin role, you can install the Telecommunications Network Inventory application. The application includes the demo data and installations that are related ServiceNow Store applications and plugins, if they aren’t already installed.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Telecommunications Network Inventory]
---

# Install Telecommunications Network Inventory

If you have the admin role, you can install the Telecommunications Network Inventory application. The application includes the demo data and installations that are related ServiceNow® Store applications and plugins, if they aren’t already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Ensure to install the demo data of Telecommunications Network Inventory. On installing the demo data, the flows and subflows are triggered. The demo data enables you to understand the flow of OMT-TNI integration. As part of the demo data along with the required attributes, the following are also created:

    1.  Order- Includes an order request for installation of fiber broadband demo data
    2.  Order task- An order task is created automatically when an order is created
    3.  OMT task- order management tasks that are created under an order task
    4.  Change request- this includes the change request details for the installation of fiber broadband
    5.  Change task- multiple tasks are created to fulfill the order
    **Note:** On successful installation of demo data, the demo data for GPON broadband and design assign link aggregation group is automatically added.

-   Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent, sn\_ni\_core.inventory\_template\_manager, sn\_ni\_core.telco\_inventory\_catalog\_manager


## About this task

The following items are installed with Telecommunications Network Inventory:

-   Plugins
-   Store applications
-   Roles
-   Tables

For more information on viewing components that are installed with an application, see Find components installed with an application.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Telecommunications Network Inventory application \(sn\_ni\_adv\) using the filter criteria and search bar.

    **Note:** Installation of TNI Advanced leads to automatic installation of TNI Core without its demo data. You need to manually load or install the demo data for TNI Core demo data.

    You can search for the application by its name \(Network Inventory\) or ID. If you can't find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications appear if they’re yet to be installed, are currently installed, or must be installed. If any plugins or applications require installation, you must install them before you can install Telecommunications Network Inventory.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


**Parent Topic:**[Configuring Telecommunications Network Inventory](../concept/configuring-telecom-network-inventory.md)


---
title: Install Opportunity Management
description: If you have the admin role, you can install the Opportunity Management application. The application includes the demo data and installations that are related ServiceNow Store applications and plugins.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Install and configure Opportunity Management, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Install Opportunity Management

If you have the admin role, you can install the Opportunity Management application. The application includes the demo data and installations that are related ServiceNow® Store applications and plugins.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Depending on your entitlements, you may have to install demo data after installation. Demo data comprises the sample records that describe application features for the common use cases.

Role required: admin

## About this task

The following items are installed with [Opportunity Management](../concept/opportunity-management.md):

-   Plugins
-   Store applications
-   Roles
-   Tables

For more information on viewing components that are installed with an application, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the [Opportunity Management](../concept/opportunity-management.md) application \(sn\_opty\_mgmt\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications appear if they’re installed, or are currently installed, or must be installed. If any plugins or applications require installation, you must install them before you can install [Opportunity Management](../concept/opportunity-management.md).

4.  If you want to install demo data, do one of the following depending on your entitlements.

<table id="choicetable_t11_3lj_21c"><thead><tr><th align="left" id="d34104e220">

Demo data install task

</th><th align="left" id="d34104e223">

Description

</th></tr></thead><tbody><tr><td id="d34104e229">

**If demo data is available and you want to install it**

</td><td>

1.  Select the **Load Demo Data** option.
2.  Select **Install**.
 **Important:** If you don't load the demo data during installation, it's unavailable to load later.

</td></tr><tr><td id="d34104e259">

**If the Load Demo Data option isn’t available but you want demo data**

</td><td>

Load the demo data after installing [Opportunity Management](../concept/opportunity-management.md).1.  Install [Opportunity Management](../concept/opportunity-management.md).
2.  Navigate to the **All** and in the Filter, type `v_plugin.list`.
3.  In the **System Plugin** list, search for Opportunity Management data model \(sn\_l2c\_opportunity\_mgmt\_data\_model\) plugin.
4.  In the System **Plugin Opportunity Management data model** window, under Related Links, select **Install Demo Data Only**.


</td></tr></tbody>
</table>

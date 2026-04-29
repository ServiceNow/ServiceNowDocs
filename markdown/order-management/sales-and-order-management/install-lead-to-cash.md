---
title: Install Lead to Cash Core
description: If you have the admin role, you can install the Lead to Cash Core application. The application includes the demo data and installations that are related ServiceNow Store applications and plugins.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Install and configure Lead to Cash Core, Lead-to-cash foundation apps, Configure, Sales and Order Management]
---

# Install Lead to Cash Core

If you have the admin role, you can install the Lead to Cash Core application. The application includes the demo data and installations that are related ServiceNow® Store applications and plugins.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Depending on your entitlements, you may have to install demo data after installation. Demo data comprises the sample records that describe application features for the common use cases.

Role required: admin

## About this task

The following items are installed with Lead to cash core application:

-   Plugins
-   Store applications
-   Roles
-   Tables

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Lead to Cash Core application \(com.snc.l2c\_core\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications appear if they’re installed, or are currently installed, or must be installed. If any plugins or applications require installation, you must install them before you can install the Lead to Cash Core application.

4.  If you want to install demo data, do one of the following depending on your entitlements.

<table id="choicetable_t11_3lj_21c"><thead><tr><th align="left" id="d54404e154">

Demo data install task

</th><th align="left" id="d54404e157">

Description

</th></tr></thead><tbody><tr><td id="d54404e163">

**If demo data is available and you want to install it**

</td><td>

1.  Select the **Load Demo Data** option.
2.  Select **Install**.
 **Important:** If you don't load the demo data during installation, it's unavailable to load later.

</td></tr><tr><td id="d54404e193">

**If the Load Demo Data option isn’t available but you want demo data**

</td><td>

Load the demo data after installing the Lead to Cash Core application.1.  Install Lead to Cash Core \(com.snc.l2c\_core\).
2.  Navigate to the **All** and in the Filter, type `v_plugin.list`.
3.  In the related Links, select **Install Demo Data Only**.


</td></tr></tbody>
</table>

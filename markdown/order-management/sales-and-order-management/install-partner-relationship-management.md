---
title: Install Partner Relationship Management
description: Install the Partner Relationship Management plugin \(com.snc.partner\_relationship\_management\), along with the demo data and installations that are related to ServiceNow Store applications and plugins.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Install Partner Relationship Management

Install the Partner Relationship Management plugin \(com.snc.partner\_relationship\_management\), along with the demo data and installations that are related to ServiceNow Store applications and plugins.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Depending on your entitlements, you must install demo data after installation. Demo data comprises the sample records that describe application features for the common use cases.

Role required: admin

## About this task

The following items are installed with Partner Relationship Management:

-   Plugins
-   Store applications
-   Roles
-   Tables

For more information on viewing components that are installed with an application, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Partner Relationship Management application \(com.snc.partner\_relationship\_management\) using the filter criteria and search bar.

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications appear if they’re installed, or are currently installed, or must be installed. If any plugins or applications require installation, you must install them before you can install Partner Relationship Management.

4.  If you want to install demo data, do one of the following depending on your entitlements.

<table id="choicetable_t11_3lj_21c"><thead><tr><th align="left" id="d141729e144">

Demo data install task

</th><th align="left" id="d141729e147">

Description

</th></tr></thead><tbody><tr><td id="d141729e153">

**If demo data is available and you want to install it**

</td><td>

1.  Select the **Load Demo Data** option.
2.  Select **Install**.
 **Important:** If you don't load the demo data during installation, it's unavailable to load later.

</td></tr><tr><td id="d141729e183">

**If the Load Demo Data option isn’t available but you want demo data**

</td><td>

Load the demo data after installing Partner Relationship Management.1.  Install Partner Relationship Management \(com.snc.partner\_relationship\_management\).
2.  Navigate to the **All** and in the Filter, type `v_plugin.list`.
3.  In the **System Plugin** list, search for Partner Relationship Management plugin.
4.  In the System **Plugin Partner Relationship Management data model** window, under Related Links, select **Install Demo Data Only**.


</td></tr></tbody>
</table>
## Result

You have successfully installed the Partner Relationship Management application.

**Parent Topic:**[Configure Partner Relationship Management](../concept/configure-partner-relationship-management.md)

**Related topics**  


[Roles and components of Partner Relationship Management](../concept/roles-and-components-of-partner-relationship-management.md)

[Data model for Partner Relationship Management](../concept/data-model-for-partner-relationship-management.md)


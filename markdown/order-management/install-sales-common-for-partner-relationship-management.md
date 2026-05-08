---
title: Install Sales Common for Partner Relationship Management
description: Install the Sales Common for Channel Partners plugin \(com.snc.partner\_relationship\_management\_sales\_common\), along with the demo data and installations that are related to ServiceNow Store applications and plugins.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 2
breadcrumb: [Configure Partner Relationship Management, Configure, Sales Customer Relationship Management]
---

# Install Sales Common for Partner Relationship Management

Install the Sales Common for Channel Partners plugin \(com.snc.partner\_relationship\_management\_sales\_common\), along with the demo data and installations that are related to ServiceNow® Store applications and plugins.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Depending on your entitlements, you must install demo data after installation. Demo data comprises the sample records that describe application features for the common use cases.

Role required: admin

## About this task

The Sales Common for Channel Partners plugin acts a parent plugin for all the Lead to Cash Core workflows.

The following items are installed with the Sales Common for Channel Partners \(com.snc.partner\_relationship\_management\_sales\_common\) plugin:

-   Plugins
-   Store applications
-   Roles
-   Tables

For more information on viewing components that are installed with an application, see Find components installed with an application.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Sales Common for Channel Partners application \(com.snc.partner\_relationship\_management\_sales\_common\) using the filter criteria and search bar.

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications appear if they’re installed, or are currently installed, or must be installed. If any plugins or applications require installation, you must install them before you can install the Sales Common for Channel Partners application.

4.  If you want to install demo data, do one of the following depending on your entitlements.

<table id="choicetable_t11_3lj_21c"><thead><tr><th align="left" id="d68500e137">

Demo data install task

</th><th align="left" id="d68500e140">

Description

</th></tr></thead><tbody><tr><td id="d68500e146">

**If demo data is available and you want to install it**

</td><td>

1.  Select the **Load Demo Data** option.
2.  Select **Install**.
 **Important:** If you don't load the demo data during installation, it's unavailable to load later.

</td></tr><tr><td id="d68500e176">

**If the Load Demo Data option isn’t available but you want demo data**

</td><td>

Load the demo data after installing the Sales Common plugin.1.  Install Sales Common for Channel Partners \(com.snc.partner\_relationship\_management\_sales\_common\) application.
2.  Navigate to the **All** and in the Filter, type `v_plugin.list`.
3.  In the **System Plugin** list, search for the Sales Common plugin.
4.  In the System **Plugin Sales Common for Channel Partners data model** window, under Related Links, select **Install Demo Data Only**.


</td></tr></tbody>
</table>
## Result

You have successfully installed the Sales Common for Channel Partners \(com.snc.partner\_relationship\_management\_sales\_common\) application.

-   **[Roles and components of Sales Common](../concept/roles-and-components-of-sales-common.md)**  
The Sales Common for Channel Partners plugin \(com.snc.partner\_relationship\_management\_sales\_common\) application uses roles to provide access to information, identify internal and external users, and maintain data security.

**Parent Topic:**[Configure Partner Relationship Management](../concept/configure-partner-relationship-management.md)


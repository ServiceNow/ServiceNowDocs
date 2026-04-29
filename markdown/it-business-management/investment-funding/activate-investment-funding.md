---
title: Install Investment Funding
description: You can install the Investment Funding application \(sn\_invst\_pln\_v2\) from ServiceNow Store if you have the admin role.
locale: en-US
release: australia
product: Investment Funding
classification: investment-funding
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Investment Funding, Strategic Portfolio Management]
---

# Install Investment Funding

You can install the Investment Funding application \(sn\_invst\_pln\_v2\) from ServiceNow Store if you have the admin role.

## Before you begin

Ensure that the application and all of its associated store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

Investment Funding activates these related plugins if they are not already active.

<table id="table_vk1_ws5_vgb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Fiscal Calendar \[com.snc.fiscal\_calendar\]

</td><td>

Enables you to generate and manage different kinds of fiscal calendars that are used in various financial applications.

</td></tr><tr><td>

Widgets\[com.snc.app.widgets\]

</td><td>

Enables widgets on the dashboard pages.

</td></tr><tr><td>

Ag-Grid Components Plugin\[com.snc.app.grid\]

</td><td>

Enables grid view.

</td></tr><tr><td>

Planned Task\_v2\[com.snc.planned\_task\_v2\]

</td><td>

Enables task entities.

</td></tr></tbody>
</table>If the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin is also installed, you can use the Investment Funding features to request or allocate funds for your projects and demands.

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Investment Funding application using the filter criteria and search bar.

    You can search for the application by its name or ID \(sn\_invst\_pln\_v2\). If you cannot find an application, you may have to request it from ServiceNow store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release note information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    If your application requires other applications, install them first if they are not already installed.

    Installing your application also automatically installs the dependent applications or plugins if they are not installed already.

5.  Click **Install**.


## Result

The following components are installed with installation of the Investment Funding application:

-   Roles
-   Tables

See [Components installed with Investment Funding](../reference/installed-with-investment-funding.md) for more information.

-   **[Components installed with Investment Funding](../reference/installed-with-investment-funding.md)**  
Several types of components are installed with activation of the Investment Funding \(sn\_invst\_pln\) plugin, including tables and user roles.

**Parent Topic:**[Investment Funding](../concept/investment-funding-overview.md)


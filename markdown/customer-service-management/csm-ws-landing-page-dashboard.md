---
title: Dashboard landing pages
description: Enable your users to display, customize, and share dashboards in CSM Configurable Workspace and use these dashboards as landing pages.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Landing pages, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Dashboard landing pages

Enable your users to display, customize, and share dashboards in CSM Configurable Workspace and use these dashboards as landing pages.

Workspace dashboards enable users such as agents and managers to configure and customize their own metrics. These users can switch between available dashboards and modify dashboard lists and metrics to track important information. They can also share dashboards with coworkers and across teams.

To display workspace dashboards, system administrators activate the [CSM Dashboards](csm-ws-landing-page-dashboard.md#section_bhb_2n4_4xb) landing page variant and configure user privileges. When configured, users included in the page audience see the Dashboard Overview landing page in CSM Configurable Workspace and the [default dashboards](csm-ws-landing-page-dashboard.md#section_vny_jwb_4xb) included with that page.

The dashboards are represented by tiles on the Dashboard Overview landing page. The individual tiles show the title, the creator, whether the dashboard is certified, and an indication that the logged in user has bookmarked the dashboard.

## Benefits of dashboard landing pages

Using a dashboard as a landing page gives your users more flexibility. Being able to easily customize a dashboard makes the page much more usable. Users can create their own lists and metrics to display the information they need and then share these dashboards with other users. As an example, teams can share a single dashboard or new agents can modify a shared dashboard to create their own. It is much faster to create dashboards because they do not require configuration by a system administrator.

## Application information

The **CSM Dashboards** landing page variant is included with the CSM and FSM Configurable Workspace Foundation plugin \(com.snc.uib.cwf\_workspace\).

The CSM Configurable Workspace application, which includes the CSM and FSM Configurable Workspace plugin, is available from the ServiceNow® Store.

The default dashboards available with this landing page variant are available depending on [user role](csm-ws-landing-page-dashboard.md#section_qk3_nm4_4xb). Some of these dashboards require additional plugins to see all of the dashboard information. These plugins include:

-   Performance Analytics - Content Pack - Customer Service \(com.snc.pa.customer\_service\)
-   Performance Analytics – Content Pack – Customer Service Management – Advanced \(com.snc.pa.customer\_service\_advanced\)
-   Performance Analytics Premium for Customer Service \(com.snc.pa.premium.cs\)
-   Performance Analytics - Content Pack – Advanced Work Assignment \(com.snc.pa.awa\)

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Activating the CSM Dashboards landing page variant

The **CSM Dashboards** landing page variant is an optional page variant for the **CSM/FSM Configurable Workspace experience**. By default, this page variant is marked as inactive and has an order value of 0. When activated and set to the lowest order number, the system uses the **CSM Dashboards** landing page in place of the default [CSM Landing Page](csm-ws-landing-page-original.md) for the users included in the page audience.

**Note:** The default landing page, Dashboard Overview, and the [default dashboards](csm-ws-landing-page-dashboard.md#section_vny_jwb_4xb) included with that page are available in read-only mode and are provided as examples. It is recommended that you create and customize duplicates of the landing page and dashboards.

For more information about activating a page variant and setting the order, see [Set record page order](../task/config-csm-ws-set-record-page-order.md).

## User roles for the Dashboard Overview landing page

By default, the Dashboard Overview landing page is available to users with the following roles:

-   admin
-   sn\_customerservice\_agent
-   sn\_customerservice.consumer\_agent
-   sn\_customerservice\_manager

**Note:** Users with other roles, such as location agents or relationship agents, continue to see the **CSM Landing Page**.

The system administrator can change these default roles by configuring the page audience. For more information, see the following topics:

-   [Learn about audiences](https://www.servicenow.com/docs/access?context=add-audiences&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Add an audience to your UI Builder page](https://www.servicenow.com/docs/access?context=configure-audiences&version=australia&pubname=australia-application-development&ft:locale=en-US)

Roles determine view access for the dashboards available with the Dashboard Overview landing page. For details, see [Default dashboards](csm-ws-landing-page-dashboard.md#section_vny_jwb_4xb).

The service management agent role \(sn\_esm\_agent\) contains the data visualizations creator role \(viz\_creator\), which is a role associated with the Visualization Designer and Visualization Library. Users with the viz\_creator role can create visualizations. The customer service agent \(sn\_customerservice\_agent\) and consumer service agent \(sn\_customerservice.consumer\_agent\) roles contain the sn\_esm\_agent role. For more information, see [Data visualizations in Platform Analytics](https://www.servicenow.com/docs/access?context=analytics-center-data-visualizations&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

## Dashboard Overview landing page default dashboards

Four dashboards are available with the Dashboard Overview landing page. These dashboards are available in read-only mode for all users, including the admin role. Users can duplicate these dashboards and make the desired changes to the duplicate dashboards.

**Note:** These dashboards are also available from [Platform Analytics experience](https://www.servicenow.com/docs/access?context=par-workspace&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

The Dashboard Overview landing page includes the following dashboards for agents.

-   Customer Service Agent
-   Customer Service Agent – Advanced

The Dashboard Overview landing page includes the following dashboards for managers and admins.

-   Customer Service Agent
-   Customer Service Agent – Advanced
-   Customer Service Manager
-   Customer Service Manager – Advanced

<table id="dup_hpw_mxb"><thead><tr><th>

Landing page

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Customer Service Agent

</td><td>

Available with the CSM Configurable Workspace \(com.snc.uib.csm\_agent\_workspace\) plugin.

 Out of box, the Customer Service Agent dashboard includes the widgets on the **My Work** tab.

**Note:** The tab is not visible because it is the only tab on the dashboard.

 Activating the Performance Analytics - Content Pack - Customer Service \(com.snc.pa.customer\_service\) plugin provides the complete Customer Service Agent dashboard with all tabs.

</td></tr><tr><td>

Customer Service Agent - Advanced

</td><td>

Available with the following plugins:-   CSM Configurable Workspace \(com.snc.uib.csm\_agent\_workspace\)
-   Performance Analytics – Content Pack – Customer Service Management – Advanced \(com.snc.pa.customer\_service\_advanced\)

Activating the Performance Analytics - Content Pack – Advanced Work Assignment \(com.snc.pa.awa\) plugin adds two additional widgets to the Organizational Trends tab:

-   My Cases with Problems
-   My KBs Created

</td></tr><tr><td>

Customer Service Manager

</td><td>

Available with the following plugins:-   CSM Configurable Workspace \(com.snc.uib.csm\_agent\_workspace\)
-   Performance Analytics - Content Pack - Customer Service \(com.snc.pa.customer\_service\)

Activating the Performance Analytics - Content Pack - Customer Service \(com.snc.pa.customer\_service\) plugin provides the complete Customer Service Manager dashboard with all tabs.

</td></tr><tr><td>

Customer Service Manager - Advanced

</td><td>

Available with the following plugins:

-   CSM Configurable Workspace \(com.snc.uib.csm\_agent\_workspace\)
-   Performance Analytics – Content Pack – Customer Service Management – Advanced \(com.snc.pa.customer\_service\_advanced\)

 Activating the Performance Analytics - Content Pack – Advanced Work Assignment \(com.snc.pa.awa\) plugin adds the Work Assignment Analytics tab to the Customer Service Manager - Advanced dashboard.

</td></tr></tbody>
</table>## Certifying a dashboard

Users with the admin role can certify a dashboard to indicate that it is company-approved and recommended for use. The default dashboards available from the Dashboard Overview landing page are certified and admins cannot change this setting. Admins can only certify new dashboards. For more information, see [Certify a Platform Analytics dashboard](https://www.servicenow.com/docs/access?context=certify-db-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

## Working with dashboards

Agents can create their own dashboards and share those dashboards with other agents or assignment groups. For example, agents can create dashboards with metrics and lists that support specific assignments, such as a temporary weekend assignment.

From the Dashboard Overview landing page, managers and agents can do the following:

-   View the default dashboards available for their role.
-   Filter the available dashboards.
-   Select a dashboard tile to display the dashboard in a new tab. If more than one dashboard is available, the user can switch between the available dashboards by making a selection from the dashboard picker.
-   Duplicate and customize the default dashboards.
-   View dashboard details such as the dashboard name, description, and visibility.
-   Edit dashboards using a configuration panel.
-   Share dashboards with other users or groups and grant edit or view-only rights.
-   Create new dashboards.
-   Create and share visualization elements from the [Platform Analytics Workspace](https://www.servicenow.com/docs/access?context=par-workspace&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

See the task descriptions in the following table for more information.

<table id="table_fkf_c5v_4xb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

View the default dashboards available for your role

</td><td>

1.  Select **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

The Dashboard Overview landing page displays the available dashboards.

2.  Select a dashboard tile to display the dashboard in a new tab.

</td></tr><tr><td>

View dashboard details

</td><td>

Select a dashboard to open the Details panel.

</td></tr><tr><td>

Filter dashboards

</td><td>

Several filter options are available on the Dashboard Overview landing page. Users can filter the available dashboards in the following ways:-   By name or owner \(in the search bar\)
-   Recent: shows recently created dashboards
-   Bookmarked: shows only your bookmarked dashboards.
-   Certified: shows only the dashboards that have been certified by an administrator.
-   Created by me: shows only the dashboards that you have created.
-   Shared with me: shows only the dashboards that have been shared with you.
-   All: shows all dashboards that you have access to.

</td></tr><tr><td>

Duplicate a dashboard

</td><td>

1.  Select the More actions menu \(![More actions icon](../image/csm-ws-dashboards-more-actions-icon.png)\).
2.  Select **Duplicate**.
3.  In the Duplicating dashboard pop-up window, enter a **New name** and a **Description**.
4.  Select **Duplicate** on the pop-up window.
5.  To access the duplicated dashboard:
    -   Select **Open it** in the information message.
    -   Select the dashboard tile on the Dashboard Overview landing page.

 For more information, see [Duplicate a Platform Analytics dashboard](https://www.servicenow.com/docs/access?context=duplicate-db&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td></tr><tr><td>

Edit a dashboard

</td><td>

1.  Select **Edit**.
2.  Select the desired dashboard tab.
3.  Edit an existing element or add a new element. For more information about these tasks, see [Edit Platform Analytics dashboards](https://www.servicenow.com/docs/access?context=edit-db-in-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td></tr><tr><td>

Share a dashboard

</td><td>

1.  Select the More actions menu \(![More actions icon](../image/csm-ws-dashboards-more-actions-icon.png)\).
2.  Select **Share**.
3.  In the Share Dashboard pop-up window, add users, groups, or roles in the **Grant access to** field.
4.  If desired, enable the check box that enables permissions for the dashboard.
5.  Select either **Add as viewer** or **Add as editor**.
6.  The selected users, groups, or roles are added to the Manage Access section. From here, you can change the permissions.
7.  Click **Confirm**.

 For more information, see [Share a Platform Analytics dashboard](https://www.servicenow.com/docs/access?context=share-db-in-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td></tr><tr><td>

Create a dashboard

</td><td>

1.  From the Dashboard Overview landing page, select **Create new dashboard**.
2.  From the New dashboard pop-up window, select **In-line editor**.
3.  Provide a **Name** and a **Description** and select **Create new dashboard**. The new dashboard opens in the editing mode.
4.  Add new elements to the dashboard. For more information about this step, see see [Create a dashboard with the in-line editor](https://www.servicenow.com/docs/access?context=create-db-in-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

 When you create a dashboard with the in-line editor, several elements are available to help you organize and populate the information on your dashboard. For more information, see [Exploring Platform Analytics dashboards](https://www.servicenow.com/docs/access?context=ac-elements&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td></tr><tr><td>

Print a dashboard

</td><td>

1.  Select the More actions menu \(![More actions icon](../image/csm-ws-dashboards-more-actions-icon.png)\).
2.  Select **Printer friendly**.

 For more information, see [Print a Platform Analytics dashboard](https://www.servicenow.com/docs/access?context=printer-friendly-db-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td></tr><tr><td>

Bookmark a dashboard

</td><td>

1.  Select the More actions menu \(![More actions icon](../image/csm-ws-dashboards-more-actions-icon.png)\).
2.  Select **Add to bookmarks**.

 For more information, see [Bookmark a Platform Analytics dashboard](https://www.servicenow.com/docs/access?context=bookmark-dashboard-ac&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

</td></tr></tbody>
</table>
---
title: Install Content library portal for Software Asset Management
description: Install the Content library portal store application to view the data stored in the Software Asset Management Content Service.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Install Content library portal for Software Asset Management

Install the Content library portal store application to view the data stored in the Software Asset Management Content Service.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   The Content library portal application requires the following plugins. Ensure that these plugins are activated before you install the Content library portal application.
    -   **Required ServiceNow plugins**
        -   **Activate Software Asset Management Professional Master Workspace \(com.sn\_samp\_master\_ws\) plugin**

            This plugin will internally activate the Software Asset Management Professional \(com.sn\_samp\_master\) plugin and Software Asset Workspace \(sn\_sam\_workspace\) store application.

            -   The Software Asset Management Professional \(com.sn\_samp\_master\) plugin loads the following Software Asset Management Professional plugins in one step:

                -   Software Asset Management Professional \(com.snc.samp\) plugin
                -   All publisher pack add-on plugins
                -   Software Asset Management UI Components \(com.sn\_samp\_workbench\)
                To enable SaaS License Management, you must request the Software Asset Management — SaaS License Management Integrations \(sn\_sam\_saas\_int\) plugin separately from the ServiceNow Store.

            -   The Software Asset Workspace \(sn\_sam\_workspace\) store application is required to use the Software Asset Workspace, the new user interface of the Software Asset Management application.
        -   **AI Search plugin \(com.glide.ais\)**

            Activates AI search functionality.


**Note:** If you have installed Software Asset Management Professional \(com.sn\_samp\_master\) plugin, you can view data stored in the Software Asset Management Content service. If you have installed both Software Asset Management Professional \(com.sn\_samp\_master\) and Hardware Asset Management Professional \(com.sn\_hamp\) plugins, you can view both Software Asset Management and Hardware Asset Management data stored in the Content service. For more information about installing Content lookup portal for Hardware Asset Management, see [Install Content lookup to view Hardware Asset Management data](../../hardware-asset-management/concept/content-lookup-ham.md#).

Role required: sam\_admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Content library portal application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install the Content library portal application.

4.  Select **Install**.


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)


---
title: Install Software Asset Management Guided Experiences
description: Install the Software Asset Management Guided Experiences \(com.sn\_sam\_playbook\) application for step-by-step guidance for completing tasks in your daily software management activities.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they aren’t already installed.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Install Software Asset Management Guided Experiences

Install the Software Asset Management Guided Experiences \(com.sn\_sam\_playbook\) application for step-by-step guidance for completing tasks in your daily software management activities.The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren’t already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Activate Software Asset Management Professional Master Workspace \(com.sn\_samp\_master\_ws\) plugin. This plugin will internally activate the Software Asset Management Professional \(com.sn\_samp\_master\) plugin and Software Asset Workspace \(sn\_sam\_workspace\) store application.

Role required: sam\_admin or sam\_user

## About this task

The following items are installed with the Software Asset Management Guided Experiences application:

-   Plugins
    -   Software Asset Management Professional \(com.snc.samp\)
    -   com.glide.playbook\_experience.config
-   Store applications:
    -   Playbook Experience \(sn\_playbook\_exp\)
    -   Playbook Experience Components \(now\_playbook\_exp\)
    -   Software Asset Workspace \(sn\_sam\_workspace\)
-   Tables

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Software Asset Management Guided Experiences \(com.sn\_sam\_playbook\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they’ll be installed, are currently installed, or must be installed. If any plugins or applications must be installed, you must install them before you can install the Software Asset Management Guided Experiences application.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)


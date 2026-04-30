---
title: Install Universal Task
description: You can install the Universal Task application \(sn\_uni\_task\) if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: xanadu
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up and configuring Universal Task, Universal Task, Employee Service Management]
---

# Install Universal Task

You can install the Universal Task application \(sn\_uni\_task\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

The required Roles and Tables are installed with Universal Task. Ensure that the glide.enforce\_security\_scope.sn\_uni\_task property is set to true in Global scope.

For more information, see [Components installed with Universal Task](../reference/installed-with-uni-task.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Universal Task application \(sn\_uni\_task\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Universal Task.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


-   **[Components installed with Universal Task](../reference/installed-with-uni-task.md)**  
Several types of components are installed with activation of the Universal Task application, including tables, user roles, and scheduled jobs.

**Parent Topic:**[Setting up and configuring Universal Task](../concept/set-up-universal-task.md)


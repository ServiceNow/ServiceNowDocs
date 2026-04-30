---
title: Install Service Operations Workspace for ITOM application
description: You can install the AIOps Experience \[sn\_sow\_aiops\] application to get Service Operations Workspace for ITOM if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications if they are not already installed.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Install Service Operations Workspace for ITOM application

You can install the AIOps Experience \[sn\_sow\_aiops\] application to get Service Operations Workspace for ITOM if you have the admin role.The application includes demo data and installs related ServiceNow® Store applications if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [AIOps Experience](https://store.servicenow.com/sn_appstore_store.do#!/store/application/38f8f09e68752110f87762d826aeb7f4/24.2.3?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3DAIOps%2520Experience&sl=sh) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Service Operations Workspace supports domain separation. For details, see [Domain separation and Event Management](../../event-management/concept/domain-separation-event-management.md).

Role required: admin

## About this task

The following items are installed with AIOps Experience \[sn\_sow\_aiops\] plugin.

-   Roles
-   Plugins

For more information, see [Components installed with AIOps Experience](../reference/components-installed-with-sow-itom.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the AIOps Experience \[sn\_sow\_aiops\] using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.



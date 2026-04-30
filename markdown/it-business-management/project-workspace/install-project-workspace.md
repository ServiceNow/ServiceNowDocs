---
title: Install Project Workspace
description: You can install the Project Workspace application \(sn\_pw\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: yokohama
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring projects with Project Workspace, Configure, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Install Project Workspace

You can install the Project Workspace application \(sn\_pw\) if you have the admin role.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Project Workspace](https://store.servicenow.com/sn_appstore_store.do#!/store/application/47e2b69f533f201016f6ddeeff7b12fa) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Starting with Yokohama release, installing the PPM Standard plugin also installs the Project Workspace application.
-   Ensure you have activated the PPM Standard plugin \(com.snc.financial\_planning\_pmo\).

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Project Workspace application \(sn\_pw\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


## Result

Planning attributes dependency plug-in is installed along with Project Workspace.

**Parent Topic:**[Configuring projects with Project Workspace](../../pw-resource-management/concept/configure-projects-pw.md)


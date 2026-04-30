---
title: Install Cloud Workspace
description: You can install the Cloud Workspace application \(sn\_itom\_cam\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up Cloud Account Management in Cloud Workspace, Configure, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Install Cloud Workspace

You can install the Cloud Workspace application \(sn\_itom\_cam\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Cloud Account Management](https://store.servicenow.com/sn_appstore_store.do#!/store/application/7c1f002e4309c210ec552887eab8f294/2.0.0) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

[Roles](../reference/components-installed-with-cam.md) are installed with Cloud Workspace.

For more information, see [Plugins installed in Cloud Account Management](../../itom-cloud-accelerate/reference/plugin-app-cloud-accelerate.md#section_v5j_yxm_cbc).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Cloud Workspace application \(sn\_itom\_cam\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the available versions are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.



---
title: Install Workflow Data Fabric Home store applications
description: You can install Workflow Data Fabric store applications if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Install Workflow Data Fabric Home store applications

You can install Workflow Data Fabric store applications if you have the admin role.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the Workflow Data Fabric Home application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

Roles are installed with the Workflow Data Fabric Home store applications. For more information, see [Workflow Data Fabric Home roles](../reference/installed-with-workflow-data-fabric.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Connect Hub \(sn\_wdf\_connect\_hub\) Home store applications using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    |Name|App ID|
    |----|------|
    |WDF Unified Hub|sn\_wdf\_unified\_hub|
    |Now Assist for Workflow Data Fabric \(WDF\)|sn\_nowassist\_wdf|

    A list of the versions available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.



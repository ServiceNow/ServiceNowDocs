---
title: Install Microsoft Endpoint Configuration Manager for Investigation
description: You can install the Microsoft Endpoint Configuration Manager for Investigation \(sn\_mecm\_adapter\) application if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they aren’t already installed.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation, Setting up Investigation Framework in Service Operations Workspace, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Install Microsoft Endpoint Configuration Manager for Investigation

You can install the Microsoft Endpoint Configuration Manager for Investigation \(sn\_mecm\_adapter\) application if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren’t already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Service Operations Workspace ITSM Applications](https://tpp.servicenow.com/sn_appstore_store.do#!/tpp/application/editapplication/213afe191b860dd029bd1f03b24bcbd1?st=appdetail) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The Microsoft Endpoint Configuration Manager for Investigation \(sn\_mecm\_adapter\) application enables you to retrieve and display the CI metrics information for the affected CIs with the ci\_computer or ci\_server class on the **Investigation** tab of the Incident record. You can configure the display of the CI metrics data using the Investigate Framework module, which is installed along with this application. The CI metrics information of the affected CIs helps you to analyze and resolve the issue.

The following items are installed with Microsoft Endpoint Configuration Manager for Investigation \(sn\_mecm\_adapter\) application:

-   Store applications
-   Roles

For more information, see [Components installed with Microsoft Endpoint Configuration Manager for Investigation](../reference/components-installed-mecm-adapter.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Microsoft Endpoint Configuration Manager for Investigation \(sn\_mecm\_adapter\) application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Parent Topic:**[Setting up investigation framework using Microsoft Endpoint Configuration Manager for Investigation](../concept/set-up-investigate-fw-mecm.md)


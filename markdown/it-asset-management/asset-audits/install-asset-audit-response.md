---
title: Install Asset Audit Response
description: You can install the Asset Audit Response application \(com.sn\_audit\_response\) if you have the admin role. The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: Asset Audits
classification: asset-audits
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Asset Audit Response, IT Asset Management]
---

# Install Asset Audit Response

You can install the Asset Audit Response application \(com.sn\_audit\_response\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Asset Audit Response](https://store.servicenow.com/sn_appstore_store.do#!/store/application/9664697a7fd7121015742fab1d866566/1.0.1) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Ensure that at least one of the following applications is already installed on your ServiceNow instance:
    -   The ServiceNow® Software Asset Management application — For instructions on how to install this application, see [Request Software Asset Management](../../software-asset-management2/task/t_RequSoftwareAssetMgmt.md).
    -   The ServiceNow® Hardware Asset Management application — For instructions on how to install this application, see [Install Hardware Asset Management](../../hardware-asset-management/task/install-ham.md).

Role required: admin

## About this task

The following items are installed with Asset Audit Response:

-   Store applications
-   Roles
-   Tables

For more information, see [Installed with Asset Audit Response](../reference/installed-with-asset-audit-response.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Asset Audit Response application \(com.sn\_audit\_response\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    A list of the versions available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Parent Topic:**[Configuring Asset Audit Response](../concept/configuring-asset-audit-response.md)


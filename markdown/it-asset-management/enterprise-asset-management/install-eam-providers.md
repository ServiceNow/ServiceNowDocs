---
title: Install Enterprise Asset Management for Providers
description: You can install the Enterprise Asset Management for Providers application \(com.sn\_eam\_provider\) if you have the admin role. The application installs related ServiceNow Store applications if they are not already installed.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Enterprise Asset Management for Providers, Industry-specific EAM solutions, Enterprise Asset Management, IT Asset Management]
---

# Install Enterprise Asset Management for Providers

You can install the Enterprise Asset Management for Providers application \(com.sn\_eam\_provider\) if you have the admin role. The application installs related ServiceNow® Store applications if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Enterprise Asset Management for Providers](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c20fc42fffb62210883dffffffffffd7/1.0.0) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Install the Enterprise Asset Management \(com.sn\_eam\) application or one of the following Enterprise Asset Management-dependent applications on your ServiceNow instance:

    **Note:** For instructions on how to install the Enterprise Asset Management application, see [Install Enterprise Asset Management](request-enterprise-asset-management.md).

    -   OT Asset Management \(com.sn\_otam\)

        For instructions on how to install this application, see [Install OT Asset Management](install-otam.md).

    -   Enterprise Asset Management for Healthcare \(com.sn\_eamhc\)

        For instructions on how to install this application, see [Install Enterprise Asset Management for healthcare](install-eam-for-healthcare.md).

    -   Enterprise Asset Management for Facilities \(com.sn\_eamfam\)
    -   Enterprise Asset Management for Data Center and Network Asset Management \(com.sn\_eam\_dcnam\)

        For instructions on how to install this application, see [Install Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)](install-eam-dcnam.md).


Role required: admin

## About this task

The following items are installed with Enterprise Asset Management for Providers:

-   Roles
-   Store applications
-   Tables

For more information, see [Components installed with Enterprise Asset Management for Providers](../reference/installed-with-eam-providers.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Enterprise Asset Management for Providers application \(com.sn\_eam\_provider\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    A list of the versions available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select **Install**.


**Parent Topic:**[Enterprise Asset Management for Providers](../concept/eam-providers.md)


---
title: Install Public Sector Digital Services Core
description: You can install the Public Sector Digital Services Core application \(sn\_gsm\) if you have an admin role. The application includes demo data.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Activate Public Sector Core, Getting Started with Public Sector, Set up your environment, Configure, Public Sector Digital Services \(PSDS\)]
---

# Install Public Sector Digital Services Core

You can install the Public Sector Digital Services Core application \(sn\_gsm\) if you have an admin role. The application includes demo data.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the Public Sector Digital Services Core application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

    The Public Sector Digital Services Core application requires a subscription.


Role required: admin

## About this task

For more information, see [Components and Roles installed with Public Sector Digital Services Core](../reference/installed-with-public-sector-digital-services-core.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Public Sector Digital Services Core application \(sn\_gsm\) by using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


## What to do next

Use [guided setup](../concept/configure-psds-foundation-data.md#) to configure the Public Sector Digital Services Core application. If you're not using guided setup, you can customize the Government Service Portal and configure the CSM Configurable Workspace for public sector use by following the [optional configuration steps for Public Sector Digital Services Core](../concept/psds-optional-config-steps.md).


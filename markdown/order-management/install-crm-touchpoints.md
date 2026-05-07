---
title: Install CRM Touchpoints
description: You can install the CRM Touchpoints application \(com.sn\_crm\_touchpoint\) if you have the admin role. The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activity Management, Lead and opportunity management apps, Configure, Sales Customer Relationship Management]
---

# Install CRM Touchpoints

You can install the CRM Touchpoints application \(com.sn\_crm\_touchpoint\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [CRM Touchpoint](https://store.servicenow.com/sn_appstore_store.do#!/store/application/b8e19037ff19f210ab96ffffffffff59) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with CRM Touchpoints:

-   Roles
-   Tables

For more information, see [Components installed with CRM Touchpoints](../reference/components-installed-crm-touchpoints.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the CRM Touchpoints application \(sn\_crm\_touchpoint\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    A list of the versions available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


## What to do next

[Create custom touchpoint types](create-custom-touchpoint-types.md)


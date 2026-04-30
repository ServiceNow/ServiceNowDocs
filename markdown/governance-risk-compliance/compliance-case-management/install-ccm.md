---
title: Install Compliance Case Management
description: You can install the GRC: Compliance Case Management application \(sn\_comp\_case\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes the demo data and related ServiceNow Store applications and plugins if they aren’t already installed.
locale: en-US
release: yokohama
product: Compliance Case Management
classification: compliance-case-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Compliance Case Management, Compliance Case Management, Governance, Risk, and Compliance]
---

# Install Compliance Case Management

You can install the GRC: Compliance Case Management application \(sn\_comp\_case\) if you have the admin role.The application includes the demo data and related ServiceNow® Store applications and plugins if they aren’t already installed.

## Before you begin

Role required: admin

Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

## About this task

The following items are installed with Compliance Case Management:

-   Plugins
-   Store applications
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Tables installed with Compliance Case Management](../reference/tables-compliance-case-management.md) and [Roles installed with Compliance Case Management](../reference/roles-compliance-case-management.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Compliance Case Management application \(sn\_comp\_case\) by using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Parent Topic:**[Configuring Compliance Case Management](../concept/configure-compliance-case-management.md)


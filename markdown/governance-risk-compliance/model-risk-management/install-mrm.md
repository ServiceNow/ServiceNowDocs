---
title: Install Model Risk Management
description: Install the Model Risk Management application \(sn\_model\_risk\_mgmt\). The application installs related ServiceNow Store applications and plugins if they aren’t already installed.
locale: en-US
release: yokohama
product: Model Risk Management
classification: model-risk-management
topic_type: task
last_updated: "2025-08-09"
reading_time_minutes: 1
breadcrumb: [Configure, Model Risk Management, Governance, Risk, and Compliance]
---

# Install Model Risk Management

Install the Model Risk Management application \(sn\_model\_risk\_mgmt\). The application installs related ServiceNow® Store applications and plugins if they aren’t already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the Model Risk Management application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Check your entitlements to determine whether you have access to Model Risk Management.

Role required: sn\_model\_risk\_mgmt.admin

## About this task

The following items are installed with Model Risk Management:

-   Plugins
-   Store applications
-   Roles
-   Tables
-   Properties

For more information, see [Model Risk Management reference](../concept/mrm-reference.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Model Risk Management application \(sn\_model\_risk\_mgmt\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you’re displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.



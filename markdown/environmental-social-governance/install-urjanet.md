---
title: Install Urjanet ESG integration
description: You can install the Urjanet ESG integration application \(sn\_esg\_urjanet\) if you have the admin role. The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management with Urjanet, Integrating ESG Management with other applications, Environmental, Social, and Governance Management]
---

# Install Urjanet ESG integration

You can install the Urjanet ESG integration application \(sn\_esg\_urjanet\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Ensure that you create an Urjanet account and obtain the login credentials.

Role required: sn\_esg.admin

## About this task

The following items are installed with Urjanet ESG integration:

-   Plugins
-   Store applications
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with ESG Management](../reference/components-installed-with-esg.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Urjanet ESG integration application \(sn\_esg\_urjanet\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Parent Topic:**[Integrating ESG Management with Urjanet](../concept/integrating-esg-management-with-urjanet.md)


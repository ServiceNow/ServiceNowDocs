---
title: Install Operational Sustainability Integration with Workday
description: You can install the Operational Sustainability Integration with Workday application \(sn\_esg\_workday\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence: The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management \(formerly ESG\) with Workday, Integrating ESG Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Install Operational Sustainability Integration with Workday

You can install the Operational Sustainability Integration with Workday application \(sn\_esg\_workday\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Confirm that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Activate the ServiceNow IntegrationHub Enterprise Pack Installer \(com.glide.hub.integrations.enterprise\) plugin.

Role required: admin

## About this task

The following items are installed with Operational Sustainability Integration with Workday:

-   Plugins
-   Store applications
    -   Operational Sustainability Management
    -   GRC: Profiles Dependencies
    -   GRC: Policy and Compliance Management
    -   GRC: Metrics
    -   Goal Framework
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Operational Sustainability Management \(formerly ESG Management\)](../reference/components-installed-with-esg.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Operational Sustainability Integration with Workday application \(sn\_esg\_workday\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.



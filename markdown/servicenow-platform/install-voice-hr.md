---
title: Install ServiceNow Voice for HR
description: You can install ServiceNow Voice for HR if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrating ServiceNow Voice for HR, Integrating Voice with other applications, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Install ServiceNow Voice for HR

You can install ServiceNow Voice for HR if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow® Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Your organization must have purchased the Agent Workspace for HR Case Management \(sn\_hr\_agent\_ws\) subscription.
-   Ensure that Amazon Connect Integration with ServiceNow Voice \(sn\_cti\_amzn\_cct\) is installed. For more information, see [Install ServiceNow Voice applications](../../cloud-call-center/task/install-ccc-apps.md).

Role required: admin

## About this task

Follow the steps below to install these applications to use ServiceNow Voice for HR.

The following items are installed with ServiceNow Voice for HR:

-   Contact flows
-   Operation handlers

For more information, see [Components installed with ServiceNow Voice for HR Agent Workspace](../../cloud-call-center/reference/instld-with-hr-agent.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the ServiceNow Voice for HR Agent Workspace \(sn\_cti\_hr\_cnt\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


## What to do next

Follow these steps to [Integrate ServiceNow Voice with Amazon Connect](../../cloud-call-center/task/integrate-ccc-amazonconnect.md).

**Parent Topic:**[Integrating ServiceNow Voice for HR](../../cloud-call-center/concept/integrate-voice-hr-agent.md)


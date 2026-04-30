---
title: Cloud Migration Assessment configuration
description: Install Cloud Migration Assessment from ServiceNow Store.You can install the Cloud Migration Assessment application \(com.sn\_cloud\_migration\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Cloud Migration Assessment, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Migration Assessment configuration

Install Cloud Migration Assessment from ServiceNow Store.

## Install Cloud Migration Assessment

You can install the Cloud Migration Assessment application \(com.sn\_cloud\_migration\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

### Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

### About this task

Cloud Migration Assessment utilizes the ITOM Cloud Accelerate subscription.

The Cloud Migration Base application \(com.sn\_cloud\_mig\_base\) is automatically activated when you install the Cloud Migration Assessment application \(com.sn\_cloud\_migration\).

The following items are installed with Cloud Migration Assessment:

-   Plugins
-   Roles
-   Scheduled jobs
-   Tables
-   Properties

For more information, see [Components installed with Cloud Migration Assessment](../reference/components-installed-cloud-migration.md).

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Cloud Migration Assessment application \(com.sn\_cloud\_migration\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    See the available versions in the list next to the **Install** button.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Related topics**  


[Subscriptions for IT Operations Management](../../it-operations-management/concept/itom-license-module.md)


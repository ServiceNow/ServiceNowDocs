---
title: Install Health and Safety Environmental Management
description: You can install the Health and Safety Environmental Management if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they aren’t already installed.
locale: en-US
release: yokohama
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2025-11-27"
reading_time_minutes: 2
breadcrumb: [Configure settings, Health and Safety Environmental Management, Health and Safety, Employee Service Management]
---

# Install Health and Safety Environmental Management

You can install the Health and Safety Environmental Management if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they aren’t already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Health and Safety Environmental Management](https://store.servicenow.com/store/app/0810e27c4735fa9482f632c4f16d4360) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with Health and Safety Environmental Management:

-   Store applications
-   Plugins
-   Roles
-   Tables

For more information, see [Components installed with Health and Safety Environmental Management](../reference/hs-components-installed-environmental-management.md).

This table lists the optional applications that can be installed for additional features:

<table id="table_bmd_1m5_mhc"><thead><tr><th>

Plugins

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health and Safety Connector Core

 \[com.sn\_hs\_connector\_core\]

</td><td>

Enables installation of external connector plugins such as the **Spoke for 3E** plugin.

</td></tr><tr><td>

Spoke for 3E

 \[com.sn\_hs\_spoke\_3e\]

</td><td>

Enables integration with the 3E service provider to sync chemical, hazard, and related regulatory data into Health and Safety.

</td></tr><tr><td>

Health and Safety Chemical

 \[com.sn\_hs\_chm\]

</td><td>

Manages chemicals, requests, approvals, and regulatory information as part of the Health and Safety solution, including integration points to external providers like 3E.

</td></tr><tr><td>

Integrations professional

 \[com.glide.hub.integrations.professional:sys\]

</td><td>

Provides the IntegrationHub Professional capabilities required to connect to external systems such as 3E. This plugin is required to use the Spoke for 3E plugin.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Health and Safety Environmental Management application \(sn\_hs\_env\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you’re displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Parent Topic:**[Setting up Health and Safety Environmental Management](../concept/hs-setting-up-environmental-management.md)


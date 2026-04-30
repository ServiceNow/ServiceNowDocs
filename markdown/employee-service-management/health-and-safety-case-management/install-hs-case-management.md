---
title: Install Health and Safety Case Management
description: You can install the Health and Safety Case Management application \(sn\_hs\_cm\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: yokohama
product: Health and Safety Case Management
classification: health-and-safety-case-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure settings, Health and Safety Case Management, Health and Safety, Employee Service Management]
---

# Install Health and Safety Case Management

You can install the Health and Safety Case Management application \(sn\_hs\_cm\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Health and Safety Case Management](https://store.servicenow.com/sn_appstore_store.do#!/store/application/5dc2c861886d3210a2788bff7b5a4207) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with Health and Safety Case Management:

-   Plugins
-   Store applications
-   Roles
-   Tables

For more information, see [Components installed with Health and Safety Case Management](../reference/components-installed-with-hs-case-mgmt.md).

<table id="optional_apps_HSCM"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Health and Safety Incident Management\[sn\_hs\_im\_incident\]

</td><td>

Installs safety-related employee incidents and observations capability for Health and Safety Case Management. For more information, see [Install Health and Safety Incident Management](../../ohs-incident-management/task/install-hs-incident-mgmt.md).

</td></tr><tr><td>

Human Resources Scoped App: Core \[com.sn\_hr\_core\]

</td><td>

Installs Case and Knowledge Management for creating HR cases from injury and illness records in Health and Safety Incident Management.-   For more information on activating it, see [Activate Case and Knowledge Management](../../human-resources/task/activate-case-and-knowledge-management-scoped.md).
-   For information on creating HR cases from injury and illness records, see [Create an HR case from an injury or illness](../../ohs-incident-management/task/create-hr-case-injury-illness.md).

</td></tr><tr><td>

Universal Request\[com.snc.universal\_request\]

</td><td>

Installs Universal Request application that supports cross-departmental collaboration and unified employee experience. For more information, see [Universal Request for Health and Safety cases](../concept/universal-request-hs-case-mgmt.md).

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Health and Safety Case Management application \(sn\_hs\_cm\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Parent Topic:**[Configuring Health and Safety Case Management](../concept/hs-setting-up-case-management.md)

**Previous topic:**[Configuring Health and Safety Case Management](../concept/hs-setting-up-case-management.md)

**Next topic:**[Configure HR service for creating an HR case for an injury](hs-configure-hr-service-property-case-injury.md)


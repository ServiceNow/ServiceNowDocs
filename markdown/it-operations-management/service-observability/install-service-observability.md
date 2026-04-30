---
title: Install Service Observability
description: If you have the system admin role, you can install the Service Observability application \(sn\_sow\_svcobs\). The application installs related ServiceNow Store applications and plug-ins if they aren't already installed.
locale: en-US
release: xanadu
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Service Observability, Service Observability, ITOM Health, IT Operations Management]
---

# Install Service Observability

If you have the system admin role, you can install the Service Observability application \(`sn_sow_svcobs`\). The application installs related ServiceNow® Store applications and plug-ins if they aren't already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Service Observability](https://store.servicenow.com/sn_appstore_store.do#!/store/application/e6a7790afc524e6287c48745c5f7f107/1.5.0) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: system admin \[admin\]

## About this task

The following items are installed with Service Observability:

-   Plugins
-   Store applications
-   Roles
-   Tables

For more information, see [Components installed with Service Observability](../reference/components-installed-with-service-observability.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Service Observability application \(`sn_sow_svcobs`\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select **Install**.


**Parent Topic:**[Configuring Service Observability](../concept/configuring-service-observability.md)


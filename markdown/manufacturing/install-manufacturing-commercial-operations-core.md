---
title: Install Manufacturing Commercial Operations
description: Install the Manufacturing Commercial Operations Core application with the admin role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/install-manufacturing-commercial-operations-core.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Manufacturing Commercial Operations]
---

# Install Manufacturing Commercial Operations

Install the Manufacturing Commercial Operations Core application with the admin role.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

The following items are installed with Manufacturing Commercial Operations:

-   Roles
-   Tables
-   Plugins
-   ServiceNow Store applications

For details about the plugins, see [Plugins installed with Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/manufacturing-commercial-operations-plugins.md).

**Note:** Installing a plugin from the store also installs its dependent hidden store applications automatically. The MCO Integrations plugin is an exception: it doesn't install with the core apps. You must search for and install it separately.

## Procedure

1.  Navigate to **All** &gt; **System Application** &gt; **All Available Applications** &gt; **All**.

2.  Find the Manufacturing Commercial Operations application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

3.  Select **Install**.

    In the Application installation dialog box, review the application dependencies.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available, select the **Load demo data** check box to install it.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Related topics**  


[Assigning roles in Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/assign-mco-roles.md)


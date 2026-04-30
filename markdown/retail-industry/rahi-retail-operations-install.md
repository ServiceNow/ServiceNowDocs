---
title: Activate plugins
description: If you have the admin role, you can install the Retail applications.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Retail]
---

# Activate plugins

If you have the admin role, you can install the Retail applications.

## Before you begin

Confirm that the application and all of its associated ServiceNow® Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

The following items are installed with Retail:

-   Roles
-   Tables
-   Plugins
-   ServiceNow® Store applications
-   Related Party Configurations

For information about the components installed with each plugin, see respective associated links in [Components installed with plugins](../concept/rahi-retail-components-installed-with-plugins.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Retail plugin using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [Store release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  If you're prompted, follow the links to the ServiceNow® Store to get any additional entitlements for dependencies.

4.  Select **Install**.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the global domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed.



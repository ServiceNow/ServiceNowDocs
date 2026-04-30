---
title: Install Manufacturing Commercial Operations
description: Install the Manufacturing Commercial Operations Core application with the admin role. The application includes demo data Manufacturing Commercial Operations core and installs related ServiceNow store applications and plugins that aren’t already installed.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Getting started with Manufacturing Commercial Operations, Set up your environment, Configuring Manufacturing Commercial Operations, Manufacturing Commercial Operations]
---

# Install Manufacturing Commercial Operations

Install the Manufacturing Commercial Operations Core application with the admin role. The application includes demo data Manufacturing Commercial Operations core and installs related ServiceNow® store applications and plugins that aren’t already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

The following items are installed with Manufacturing Commercial Operations:

-   Roles
-   Tables
-   Plugins
-   ServiceNow Store applications

The Manufacturing Commercial Operations Core application is dependent on the Product Catalog Management Core, CIWF UI components, and Industry Core applications.

To review all the plugins that are activated by installing the Sales promotion management, Manufacturing recall management, and Manufacturing repair management, see [Plugins installed with Manufacturing Commercial Operations](manufacturing-commercial-operations-plugins.md).

For more information on the components, see [Components installed with Manufacturing Commercial Operations Core](../reference/mco-components-installed.md).

## Procedure

1.  Navigate to **All** &gt; **System Application** &gt; **All Available Applications &gt; All.**.

2.  Find the Manufacturing Commercial Operations Core application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    -   Sales promotion claim management \[sn\_sls\_prm\_clm\_mgt\]
    -   Manufacturing repair claim management \[sn\_repr\_claim\_mgmt\]
    -   Manufacturing recall claim management \[sn\_rcl\_claim\_mgmt\]
    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

4.  Select **Install**.



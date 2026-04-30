---
title: Install Service Bridge for Providers in Manufacturing Commercial Operations
description: If you have an admin role, you can install the Service Exchange for Providers \(sn\_sb\_pro\) application for use with Manufacturing Commercial Operations. The application includes the demo data and installations that are related to ServiceNow Store applications and plugins.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Installing and configuring Service Exchange for Providers, Configuring Manufacturing Commercial Operations, Manufacturing]
---

# Install Service Bridge for Providers in Manufacturing Commercial Operations

If you have an admin role, you can install the Service Exchange for Providers \(sn\_sb\_pro\) application for use with Manufacturing Commercial Operations. The application includes the demo data and installations that are related to ServiceNow® Store applications and plugins.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

The following plugins are automatically installed with the Service Exchange for Providers application in Manufacturing Commercial Operations:

-   sn\_req\_criteria
-   sn\_sb
-   sn\_sb\_rps
-   sn\_transport
-   com.glide.hub.process.sync
-   com.snc.ihub\_spoke\_util\_pack

Apart from these, several components including roles, business rules, tables, and flows are also installed. For more information about the components that are installed with this application, see[Components installed with Service Exchange for Providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-installed-components-provider&version=xanadu&pubname=xanadu-service-bridge&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Service Exchange for Providers application \(sn\_sb\_pro\) by using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the application installation dialog, review the application dependencies.

    This listing indicates, for each dependent plugin and application if it's being installed, is already installed, or must be installed. If any plugins or applications must be installed, you must install them before you can install Service Exchange for Providers.

4.  If demo data is available and you want to install it, click **Load demo data**.

    Demo data contains the sample records that describe the application features for common use cases. Load demo data when you first install the application on a development or test instance. If you don't load the demo data during installation, it's unavailable to load later.

5.  Select **Install**.



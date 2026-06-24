---
title: Install the Engagement Messenger application
description: Install the Engagement Messenger application from the ServiceNow Store if you have the admin role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/install-engagement-center-app.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up Engagement Messenger, Enable communication channels, Configure, Customer Service Management]
---

# Install the Engagement Messenger application

Install the Engagement Messenger application from the ServiceNow Store if you have the admin role.

## Before you begin

Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Engagement Messenger application \(sn\_csm\_ec\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they’ll be installed, are currently installed, or must be installed. If any plugins or applications must be installed, you must install them before you can install the Engagement Messenger application.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


## Result

The following items are installed with Engagement Messenger:

-   Plugins
-   Roles
-   Tables

For more information, see [Components installed with Engagement Messenger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/installed-with-engagement-messenger.md).

## What to do next

-   If you want to enable Virtual Agent chat support in the Engagement Messenger, activate the Glide Virtual Agent plugin \(com.glide.cs.chatbot\).

    For more information, see [Activate Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/virtual-agent/activate-virtual-agent.md).

-   Get started with Engagement Messenger. For more information on how to get started, see [Set up Engagement Messenger](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/setting-up-engagement-messenger.md).


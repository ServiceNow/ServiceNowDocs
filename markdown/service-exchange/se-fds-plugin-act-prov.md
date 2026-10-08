---
title: Activate Service Exchange FDS for provider
description: You can activate the Service Exchange Foundation Data Sync for Providers plugin \(sn\_fds\_pro\) for provider if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they aren't already installed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/service-exchange/se-fds-plugin-act-prov.html
release: brazil
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 1
breadcrumb: [Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Activate Service Exchange FDS for provider

You can activate the Service Exchange Foundation Data Sync for Providers plugin \(sn\_fds\_pro\) for provider if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren't already installed.

## Before you begin

Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

When you install Foundation Data Sync for Providers, Foundation Data Sync plugin \(sn\_fds\) is installed automatically.

Verify the Security Center plugin \(sn\_vsc\) is upgraded to the version 3.2.x or above to avoid any operational issues with FDS.

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Foundation Data Sync for Consumers application \(sn\_fds\_pro\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    All dependent plugins and applications that are included, or must be installed are listed in the dialog box.

4.  If demo data is available and you want to install it, select **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

5.  Select **Install**.



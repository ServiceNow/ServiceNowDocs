---
title: Install Service Test Management
description: Install the Service Test Management application so that you can define tests, group them, and record the results that they produce.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/install-service-test-management.html
release: australia
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 2
keywords: [install service test management, sn\_st\_mgmt]
breadcrumb: [Getting started with Service Test Management, Configure, Service Test Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Install Service Test Management

Install the Service Test Management application so that you can define tests, group them, and record the results that they produce.

## Before you begin

Verify that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Review the plugins that the application requires and the optional plugins that add characteristics, test decomposition, and conditional test groups. For more information, see [Plugins installed with Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-requirements.md).

Role required: admin

## About this task

The application activates the required plugins if they aren't already active. If you install Customer Service Problem Management \(CSPM\), Service Test Management is installed with it.

For more information about viewing the components that are installed with an application, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Service Test Management application \(sn\_st\_mgmt\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you might need to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications appear if they're yet to be installed, are currently installed, or must be installed. If any plugins or applications require installation, install them before you install Service Test Management.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

5.  Select **Install**.


## Result

The Service Test Management application and its required plugins are installed. A confirmation message appears after installation is complete.

## What to do next

Assign roles to your users. For more information, see [Roles installed with Service Test Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/stm-roles.md).


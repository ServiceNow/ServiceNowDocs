---
title: Install Digital End-User Experience
description: Install the Digital End-User Experience \(DEX\) application \(sn\_dex\) to start monitoring devices. Application and Device Health is included as a component of DEX.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/install-app-device-health.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [install application device health, device health plugin, install dex application, activate dex plugin]
breadcrumb: [Installing DEX on your local machine, Configure, Digital End-User Experience, IT Operations Management]
---

# Install Digital End-User Experience

Install the Digital End-User Experience \(DEX\) application \(sn\_dex\) to start monitoring devices. Application and Device Health is included as a component of DEX.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [DEX Application &amp; Device Health](https://store.servicenow.com/sn_appstore_store.do#!/store/application/0db59e3eade11d50f8777e45b2f98b72) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with Digital End-User Experience:

-   Roles
-   Tables

For a complete list of the installed components, see [Installed with DEX](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/components-installed-with-dex.md).

For information about DEX data migration, see the [KB1646364](https://support.servicenow.com/kb_view.do?sysparm_article=KB1646364) article in the Now Support Knowledge Base.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Digital End-User Experience application \[sn\_dex\] using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.

    **Warning:** Digital End-User Experience is installed with mutual Transport Layer Security \(mTLS\) automatically enabled on the ServiceNow instance. As an updated, more secure version of SSL, mTLS enhances security by encrypting data and verifying the identity of both the client and server before establishing a connection. If you have legacy security products on any other integrations with ServiceNow, they might break after DEX installation. Update these products to support TLS or mTLS.



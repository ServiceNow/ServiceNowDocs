---
title: Install Cloud Configuration Governance
description: You can install the Cloud Configuration Governance application \(com.sn.itom.ccg\) if you have the admin role. The application installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: yokohama
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Install Cloud Configuration Governance

You can install the Cloud Configuration Governance application \(com.sn.itom.ccg\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

Cloud Configuration Governance utilizes the ServiceNow® ITOM Cloud Accelerate subscription. When you install this application, it automatically installs several roles and the ServiceNow® Cloud Action Library application \(sn.itom.cal\).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Cloud Configuration Governance application \(com.sn.itom.ccg\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or must be installed. If any plugins or applications need to be installed, you must install them before you can install Cloud Configuration Governance.

4.  Select **Install**.


## What to do next

To access the base system contents such as policies, configuration collectors, remediations, and more, install the CCG Content Pack application. For more information, see [Install CCG Content Pack](install-ccg-content-pack.md).

**Parent Topic:**[Exploring Cloud Configuration Governance](../concept/exploring-cloud-configuration-governance.md)


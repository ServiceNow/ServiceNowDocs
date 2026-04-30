---
title: Install Employee Center
description: Install Employee Center to deliver a unified, engaging employee experience across departments and systems.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Migrate to Employee Center from Service Portal, Understanding Employee Center plugins, Configure, Employee Center, Employee Service Management]
---

# Install Employee Center

Install Employee Center to deliver a unified, engaging employee experience across departments and systems.

## Before you begin

The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

Employee Center \(sn\_ex\_sp\) installs the following dependent plugins:

-   **Employee Center Core \(sn\_hr\_sp\)**

    Activates a portal framework that allows administrators to build a mobile-friendly self-service experience for users.

-   **Employee experience taxonomy \(sn\_ect\)**

    Provides an employee content taxonomy for multi-department service delivery.

-   **Employee Experience Foundation \(sn\_ex\_emp\_fd\)**

    This plugin contains components such as best practice email layouts that improve employee experiences.


## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Employee Center application \(sn\_ex\_sp\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Employee Center.

4.  Check the **Load demo data** check-box to include the demo data along with your install or repair your install with demo data checked.

    **Note:** Dependent plugin demo data is not automatically installed. To use demo data, repair the plugins with demo data checked. See [Repair a ServiceNow application](https://www.servicenow.com/docs/access?context=repair-app&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

5.  Select **Install**.

6.  Run the fix script  **Set primary topics for Employee taxonomy ** to  index the  curated experiences  demo data into  search and recommended content  .

    For more information, see [Run fix scripts to update Employee Center](run_scripts_manually_config-search.md).


## What to do next

Check and allow all the RCA \(Requested Caller Access\) privileges requested by Employee Center. For more information on running a fix script for RCA approvals, see [Run fix-script for RCA approvals](install-rca-fix-script.md).

**Parent Topic:**[Migrate to Employee Center from Service Portal](migrate-sp-to-ec.md)


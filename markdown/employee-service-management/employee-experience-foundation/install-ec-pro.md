---
title: Install Employee Center Pro
description: Employee Center Pro extends the standard Employee Center capabilities and provides a platform for employees to communicate and be engaged.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Upgrading to Employee Center Pro, Admin configurations, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Install Employee Center Pro

Employee Center Pro extends the standard Employee Center capabilities and provides a platform for employees to communicate and be engaged.

## Before you begin

Employee Center Pro requires a separate subscription from the rest of the ServiceNow AI Platform. If you are already using Employee Center and want to upgrade to Employee Center Pro, contact your ServiceNow account manager to purchase the subscription.

**Note:** Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog. For more information, see [Request a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_RequestAPlugin.md).

The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Install the Enterprise Service Management Integrations Framework \(sn\_hr\_integ\_fw\) plugin to enable Employee Center Pro to integrate with third-party systems. See [Enterprise Service Management Integrations Framework](../../human-resources/concept/hr-integrations-framework.md).

Role required: admin

## About this task

Employee Center Pro installs the following dependent plugins:

-   **Employee Center application \(sn\_ex\_sp\)**

    Installs a customizable multi-department portal and framework to help administrators build a self-service portal that provides a great self-service experience for employees.

-   **Employee Center Core \(sn\_hr\_sp\)**

    Activates a portal framework that allows administrators to build a mobile-friendly self-service experience for users.

-   **Employee experience taxonomy \(sn\_ect\)**

    Provides an employee content taxonomy for multi-department service delivery.

-   **Employee Experience Foundation \(sn\_ex\_emp\_fd\)**

    This plugin contains components such as best practice email layouts that improve employee experiences.


For information on the roles, tables, and widgets installed with Employee Center Pro, see [Components installed with Employee Center Pro](../reference/components-installed-with-employee-center-pro-1.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Employee Center Pro application \(sn\_ex\_sp\_pro\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Employee Center Pro.

4.  Select the **Load demo data** check-box to include the demo data along with your install or repair your install with demo data checked.

    **Note:** Dependent plugin demo data is not automatically installed. To use demo data, repair the plugins with demo data checked. See [Repair a ServiceNow application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/repair-app.md).

5.  Select **Install**.

6.  Run the fix script  **Set primary topics for Employee taxonomy ** to  index the  curated experiences  demo data into  search and recommended content  .

    For more information, see [Run fix scripts to update Employee Center](run_scripts_manually_config-search.md).


## What to do next

-   Check and allow all the RCA \(Requested Caller Access\) privileges requested by Employee Center. For more information on running a fix script for RCA approvals, see [Run fix-script for RCA approvals](install-rca-fix-script.md).
-   Install plugins to extend Employee Center Pro capabilities:
    -   **Content Experiences \(sn\_ca\)**

        Package your content into a campaign using multiple channels to deliver the right message to the right audience at the right time. For more information to activate this plugin, see [Activate Content Experiences](activate-content-automation-plugin.md).

    -   **Content Publishing \(sn\_sd\)**

        Use Content Publishing to create different types of information you want to distribute to your employees. For more information to activate this plugin, see [Activate Content Publishing](activate-content-delivery-plugin.md).

    -   **Content Analytics \(sn\_cda\)**

        Content Analytics helps you decide when content is stale, needs refreshing, and how engaged your employees are with your communication. For more information to activate this plugin, see [Activate Content Analytics](activate-content-analytics-plugin.md).

    -   **Content Governance \(sn\_cg\)**

        Content Governance provides a streamlined way for employees to request content to be created, track the progress, preview the content, and approve it before it is published. For more information to activate this plugin, see [Activate Content Governance](ec-install-content-gov.md)


**Parent Topic:**[Upgrading to Employee Center Pro](../concept/upgrade-steps.md)

**Related topics**  


[Components installed with Employee Center Pro](../reference/components-installed-with-employee-center-pro-1.md)


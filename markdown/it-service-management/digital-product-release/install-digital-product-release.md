---
title: Install Digital Product Release
description: You can install the Digital Product Release application \(sn\_dpr\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Digital Product Release, IT Service Management]
---

# Install Digital Product Release

You can install the Digital Product Release application \(sn\_dpr\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the Digital Product Release application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with Digital Product Release:

-   Plugins:

    Global Ranking Application plugin \(com.snc.sdlc.ranking\)

-   Store applications:

    -   Digital Product Release Data Model \(sn\_dpr\_model\): Contains the core data model for Digital Product Release.
    -   Digital Product Release Workspace \(sn\_dpr\_workspace\): Provides a single location for the program managers to plan the releases for the digital products and services and the release managers to manage the release processes.
    -   Digital Product Release Policy Content Pack: Contains a set of policies and data collectors to enable automation of phase gate verification in your Digital Product Release.
    -   Release Timeline Component: Timeline component for Digital Product Release to visualize phases in releases.
    The following apps are also installed:

    -   Policy as Code Engine \(sn\_pace\)
    -   Policy as Code Engine UI \(sn\_pace\_builder\)
    -   CMDB CI Class Models \(sn\_cmdb\_ci\_class\)
    -   Roadmap UI Builder Component \(sn\_roadmap\)
    -   Playbook Experience \(sn\_playbook\_exp\)
    -   Playbook Experience Components \(now\_playbook\_exp\)
    -   DevOps \(sn\_devops\)
    -   DevOps Workspace \(sn\_devops\_ws\)
    -   DevOps Integrations \(sn\_devops\_ints\)
    -   Quick filter component \(sn\_quick\_filter\)
    -   Quick filter popover \(sn\_filter\_popover\)
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Digital Product Release](../reference/installed-with-dpr.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Digital Product Release application \(sn\_dpr\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.



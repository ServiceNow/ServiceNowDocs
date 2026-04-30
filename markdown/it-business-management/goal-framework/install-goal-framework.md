---
title: Install Goal Framework and Goal Framework for SPM
description: You can install the Goal Framework \(sn\_gf\) and Goal Framework for SPM \(sn\_gfa\) applications if you have the admin role.
locale: en-US
release: xanadu
product: Goal Framework
classification: goal-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Install Goal Framework and Goal Framework for SPM

You can install the Goal Framework \(sn\_gf\) and Goal Framework for SPM \(sn\_gfa\) applications if you have the admin role.

## Before you begin

Ensure that the applications and all associated store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

When you install the Goal Framework for SPM application, you get all the features of Goal Framework as well as the target automation feature.

Role required: admin

**Important:** You can install the Goal Framework for SPM application only when you own the Strategic Portfolio Management \(SPM\), formerly the \(ITBM\) Pro license.

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Goal Framework or Goal Framework for SPM application using the filter criteria and search bar.

    You can search for the application by its name or ID \(sn\_gf or sn\_gfa\). If you can’t find an application, you may have to request it from ServiceNow store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release note information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    If your application requires other applications, install them first if they aren’t already installed.

    Installing your application also automatically installs the dependent applications or plugins if they aren’t installed already.

5.  Click **Install**.


## Result

The following components are installed with installation of the Goal Framework or Goal Framework for SPM application:

-   Roles
-   Tables
-   Scheduled jobs
-   Target automation script for benefit plans \(installed with Goal Framework for SPM\)

As part of Goal Framework for SPM installation, components of both Goal Framework and Goal Framework for SPM are installed. See [Components installed with Goal Framework and Goal Framework for SPM](../reference/components-installed-with-goal-framework.md) for more information.

**Parent Topic:**[Configuring Goal Framework and Goal Framework for SPM](../concept/configuring-goal-framework.md)


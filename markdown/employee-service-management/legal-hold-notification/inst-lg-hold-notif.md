---
title: Install Legal Hold Notification
description: Install the Legal Hold Notification plugin to be able to create a legal hold notification matter, add custodians, issue the legal hold notice, and close the legal hold notification matter.
locale: en-US
release: australia
product: Legal Hold Notification
classification: legal-hold-notification
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Legal Hold Notification, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Install Legal Hold Notification

Install the Legal Hold Notification plugin to be able to create a legal hold notification matter, add custodians, issue the legal hold notice, and close the legal hold notification matter.

## Before you begin

To purchase a subscription, contact your ServiceNow account manager. When you purchase a subscription, certain plugins are activated automatically. If a paid plugin isn't activated automatically, you can manually activate it from the All Applications list in your instance.

**Note:**

Before purchasing a subscription, you can evaluate the feature on a non-production instance without charge by requesting it from the Now Support Service Catalog.

Role required: admin

## About this task

The following items are installed with Legal Hold Notification:

-   Dependent store applications
-   Roles
-   Tables

For more information, see [Components installed with Legal Hold Notification](../reference/comp-inst-lg-hold-notif.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Legal Hold Notification \(sn\_lg\_hold\) application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    The available versions are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

If the Legal Counsel Center application hasn’t been previously installed, you must install it to start using Legal Hold Notification. For more information, see [Install Legal Counsel Center Workspace](../../legal-request-management/concept/install-legal-counsel-center-workspace.md).

**Parent Topic:**[Configure Legal Hold Notification](../concept/config-lg-hold-notif.md)


---
title: Install Localization Workspace
description: You can install the Localization Workspace application \(sn\_lw\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence: The application installs related ServiceNow Store applications and plugins if they are not already installed. Demo data isn't available.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Install Localization Workspace

You can install the Localization Workspace application \(sn\_lw\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed. Demo data isn't available.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Localization Workspace](https://store.servicenow.com/sn_appstore_store.do#!/store/application/03226056b7125210a5e5911cde11a950) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Localization Workspace requires a Pro or Pro+ subscription.

Role required: admin

## About this task

The following items are installed with Localization Workspace:

-   Plugins
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Localization Workspace](../reference/lw-components-installed-with.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Localization Workspace application \(sn\_lw\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select **Install**.

6.  For more information about investigating installed components, see [Find components installed with an application](../../plugins/task/find-components.md).


## What to do next

Configure the dependencies including Localization Framework, then configure Localization Workspace. For more information see [Configuring Localization Workspace](../concept/configuring-localization-workspace.md).

**Parent Topic:**[Configuring Localization Workspace](../concept/configuring-localization-workspace.md)


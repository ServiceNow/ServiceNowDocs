---
title: Installation details
description: When you install or update applications or products, the Application Manager displays installation details for you to review. Use installation details to verify version and dependency details.
locale: en-US
release: australia
product: Application Manager
classification: application-manager
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [unavailable dependencies, dependency unavailable, dependency needs to be procured from store, inactive plugin dependency]
breadcrumb: [Installing apps, plugins, and products, Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Installation details

When you install or update applications or products, the Application Manager displays installation details for you to review. Use installation details to verify version and dependency details.

A pop-up window prompting you to review installation details is shown when you install or update an application, plugin, or product. Installation details include the following components:

<table id="table_bys_m5k_yfc"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Version selector

</td><td>

Enables you to choose a licensed application or product version compatible with your instance.

 If the latest version isn't available, you might need to procure it from the ServiceNow Store to sign updated terms and conditions. If you have already procured the latest version and don't see it as an option in the version selector, you might need to upgrade your instance to a compatible release version.

</td></tr><tr><td>

\(Optional\) Dependencies list

</td><td>

If the application or product has dependencies, the dependencies are listed in the following categories:

-   Needs to be procured from the store
-   Will be updated
-   Installed
-   Inactive plugins

</td></tr><tr><td>

Installation options

</td><td>

Enables you to choose to complete installation now or later. If you choose to install later, you can determine the date and time of installation.

</td></tr></tbody>
</table>![Installation details, with an alert message saying "Install all dependent applications before installing the application." The dependencies list shows that one application needs to be procured from the ServiceNow Store.](../image/app-mgr-installation-dets.png "Example: installation details")

## Dependencies that need to be procured from the ServiceNow Store

When installing or updating an application or product, you might have dependencies that need to be procured from the ServiceNow Store.

For more information about procuring applications and products from the ServiceNow Store, see [Getting apps and trials from the ServiceNow Store](../../servicenow-store/concept/getting-apps-trials.md).

## Inactive plugins in dependencies

Some plugins must be activated before they can be installed. Any plugins that must be activated before they can be installed are categorized as inactive plugins in the dependency list. Inactive plugins might not block installation of the plugin, application, or product that requires them, but could result in reduced functionality.

For more information about how to activate plugins, see [ServiceNow plugins](../../plugins/concept/c_ServiceNowPlugins.md).

**Parent Topic:**[Installing applications, plugins, and products](installing-apps-app-manager.md)


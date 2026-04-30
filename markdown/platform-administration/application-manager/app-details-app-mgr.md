---
title: Application Manager application details
description: The details page in the Application Manager displays key information about applications, plugins, or products that are installed or available to install.Application details include information about required dependencies, including whether each dependency is installed, available to install, or not yet licensed.
locale: en-US
release: zurich
product: Application Manager
classification: application-manager
topic_type: concept
last_updated: "2025-09-12"
reading_time_minutes: 1
breadcrumb: [Explore, Application Manager, Administering applications, Get started, Administer]
---

# Application Manager application details

The details page in the Application Manager displays key information about applications, plugins, or products that are installed or available to install.

When you select an application, plugin, or product the details page is displayed.

For an application, this page includes the following:

-   Application state indicators, if applicable
-   Application summary
-   Version selector
-   Compatibilities
-   Key features
-   Release notes
-   Technical details such as system requirements and dependencies

For a plugin or product, this page shows a summary of the plugin or product's function and its dependencies.

![Application Manager details page demonstrating uninstalled application dependencies that can be installed with the application that requires them. No application state indicators are present.](../image/app-mgr-app-details.png "Application details")

The application details page for Now Assist applications includes a Now Assist suite version selector instead of an application version selector. For more information about Now Assist suites, see [Now Assist suite versions in the Application Manager](now-assist-suites-app-mgr.md).

![Application details page for a Now Assist application, highlighting the Now Assist suite version selector.](../image/app-mgr-details-now-assist.png "Now Assist application details")

## Dependencies

Application details include information about required dependencies, including whether each dependency is installed, available to install, or not yet licensed.

Each application dependency in the technical details section is listed with a symbol. The symbol indicates a category that describes whether the dependency is already available, or must be procured. Dependencies use the following categories.

<table id="table_m42_35g_zcc"><thead><tr><th>

Symbol

</th><th>

Category

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Green check icon](../image/filled-circle-check.png)

</td><td>

Installed

</td><td>

This dependency is already installed on your instance

</td></tr><tr><td>

![Dotted circle outline icon](../image/dotted-circle.png)

</td><td>

Not installed

</td><td>

This dependency isn't installed yet, but is available for installation. It's automatically installed when you install the application that requires it.

</td></tr><tr><td>

![Red unavailable icon](../image/unavailable.png)

</td><td>

Not licensed

</td><td>

This dependency must be procured from the ServiceNow Store before it can be installed. Select the dependency and review any application state indicators for additional details.

 For more information about application state indicators, see [Application state indicators in Application Manager](../reference/app-mgr-state-indicators.md).

 For more information about procuring applications, see [Getting apps and trials from the ServiceNow Store](../../servicenow-store/concept/getting-apps-trials.md).

</td></tr></tbody>
</table>
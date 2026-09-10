---
title: Install an individual plugin from Product Hub
description: Use Product Hub to discover, review, and install an individual standalone plugin without requiring a full product bundle installation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ia-install-individual-plugin.html
release: australia
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 3
breadcrumb: [Plugin installation support, Administer, ServiceNow Otto for Setup, Get started, Administer the ServiceNow AI Platform]
---

# Install an individual plugin from Product Hub

Use Product Hub to discover, review, and install an individual standalone plugin without requiring a full product bundle installation.

## Before you begin

Before you begin:

-   Your organization must have active licensing for the plugin you want to install.
-   Your instance must have access to Product Hub and the plugin must be registered as available for individual installation.

Role required: admin

## About this task

Use this procedure to install a standalone plugin through Product Hub when you want to activate specific functionality without installing an entire product bundle. Individual plugin installation validates your entitlements, checks dependencies, and guides you through the installation process.

## Procedure

1.  Navigate to Product Hub.

    A list of available products, bundles, and individual plugins shows up.

2.  Locate and select the individual plugin you want to install.

    Individual plugins are displayed alongside bundled products in the Product Hub. Look for the plugin by name, description, or category. Each plugin displays its current status \(Not installed, Installed, Updates available\).

3.  Review the plugin details and dependencies in the expanded view.

    The plugin details pane displays the plugin's name, description, current status, and a "What's included" section listing all required dependencies \(other plugins, apps, or platform prerequisites\).

4.  Verify that your organization has valid licensing for the selected plugin.

    The system automatically validates your entitlements. If the plugin or any of its required dependencies lack appropriate licensing, an error message appears with guidance on what licensing is needed.

    **Note:** You can't proceed with installation until licensing is valid.

    The system displays either a green status indicator \(entitlements valid\) or a red status indicator with actionable error messaging \(licensing missing\).

    **Note:** If you receive a licensing error, contact your ServiceNow account team to purchase the required licenses. Once licensing is activated, refresh the Product Hub and retry this procedure.

5.  Select the install button to initiate the plugin installation.

    The system validates all dependencies, then submits the install request to App Manager.

    The installation begins immediately.

6.  Verify the item count before selecting Install.

    The install button displays a count of total items to be installed, including the selected plugin and all its required dependencies. The item count updates dynamically as the selection is finalized. The button remains enabled once all licensing validations pass.

7.  Monitor the installation progress in the Product Hub.

    The plugin status displays real-time installation progress, showing percentage complete and current phase.

    **Note:** Don't navigate away from this screen during installation. Installation typically completes within minutes depending on plugin size and instance performance.

    When installation completes successfully, the plugin status updates to "Installed" and a confirmation message is displayed. You may refresh the page or navigate away.

    If the installation fails, the system displays an error message explaining why \(for example, missing dependencies, entitlement validation failure, or network error\). Note the error details and complete the following:

    -   Verify that all listed dependencies have valid entitlements.
    -   Confirm that your instance has sufficient disk space for the plugin and its dependencies.
    -   Check your network connectivity to App Manager services.
    -   Contact your ServiceNow implementation team if issues persist.
8.  Verify that the plugin is active and accessible in your instance.

    After installation completes, the plugin is automatically activated. Depending on the plugin type, you may need to navigate to the corresponding module or menu to confirm the plugin is functioning. For example, a dashboard plugin might appear under a new dashboard category, or an app plugin might appear in the app launcher.


## Result

The individual plugin and all its required dependencies are successfully installed and activated on your instance. The plugin is now available for use by users with the appropriate roles. You can track the plugin's status in Product Hub going forward, including any available updates.

## What to do next

After the plugin installation completes, consider the following next steps:

-   Assign appropriate roles to team members who need to use the newly installed plugin.
-   Configure the plugin settings if required \(consult the plugin's documentation for configuration guidance\).
-   Test the plugin functionality in your instance to confirm it meets your needs.
-   Monitor Product Hub for any available plugin updates and plan upgrade windows as needed.
-   Refer to the [Individual plugin installation from Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-plugin-install.md) for more information about dependencies, entitlements, and considerations.

**Parent Topic:**[Individual plugin installation from Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-plugin-install.md)


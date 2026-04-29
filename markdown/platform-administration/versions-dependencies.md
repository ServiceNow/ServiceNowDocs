---
title: Evaluating version requirements and dependencies
description: Reviewing technical requirements when deciding to implement a new app, product, or integration is necessary to confirm that the software can work correctly in your environment. Verify version compatibility with your ServiceNow AI Platform instance and check dependencies to make sure that an app will be ready to install after procurement.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [servicenow store, store, app store, application store, app store user documentation, servicenow app store, auto-procurement, dependency, dependencies, application dependencies, application dependency, app dependencies, app dependency, app compatibility, compatibility, version compatibility, unresolved dependencies, can't install app]
breadcrumb: [Getting apps, ServiceNow Store, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Evaluating version requirements and dependencies

Reviewing technical requirements when deciding to implement a new app, product, or integration is necessary to confirm that the software can work correctly in your environment. Verify version compatibility with your ServiceNow AI Platform instance and check dependencies to make sure that an app will be ready to install after procurement.

## Version support

The ServiceNow Store supports up to two platform releases before the current platform release. For example, if the current platform release is Yokohama, the ServiceNow Store maintains app versions that are compatible with Yokohama, Xanadu, and Washington DC.

However, it can't be guaranteed that new apps are compatible with any platform releases before the most current one. Available apps might, for example, be compatible with only Yokohama or with only Yokohama and Xanadu.

If you find that your ServiceNow AI Platform release version is no longer supported in the ServiceNow Store, upgrade your instance to take advantage of recent features and improvements. For more information, see [Using ServiceNow AI Platform upgrade tools](../../general/concept/upgrade-now-platform.md).

## Checking version compatibility

The app you want to procure must be compatible with your instance's platform release version. If you can't procure an app, check whether it's compatible with your version.

Apps on the ServiceNow Store might be compatible with multiple ServiceNow AI Platform releases. Select **Version summary** from the navigation panel of the listing details or scroll to the version details section to determine platform release compatibility. You can select the platform release version that matches your instance by using the platform release drop-down menu.

![Version details of an app listing details page, showing the options available in the platform release drop-down menu.](../image/store-version-compatibility.png "Platform release compatibility in an app listing details")

Some apps and integrations are available in more than one version. Each of these versions might be compatible with a different major platform release. Use the app version drop-down menu to view release notes and decide which version is right for your instance.

![Version details of an app listing details page, showing the options available in the app version drop-down menu.](../image/store-other-app-versions.png "Accessing other app versions in app listing details")

## About dependencies

Dependencies are the additional apps, integrations, and plugins that an app might require to work correctly. Select **Dependencies** from the navigation panel of the listing details or scroll to the version details section to view an app's dependencies.

Any app on the ServiceNow Store might have application dependencies or system plugin dependencies.

-   **Application dependencies**

    Include apps and integrations that are required for the app you want to procure. App dependencies that don't require an additional purchase are procured automatically. Paid app dependencies can be purchased through the ServiceNow Store

-   **System plugin dependencies**

    Must be activated on your instance before an app can be installed and can’t be obtained from the ServiceNow Store. Instead, plugins must be obtained through your ServiceNow license and version upgrades. For more information about plugins, see [ServiceNow plugins](../../plugins/concept/c_ServiceNowPlugins.md).


Each application dependency is listed with a symbol. The symbol indicates a category that describes how you can acquire the app dependency. App dependencies use the following categories.

**Note:** You must be logged in to the ServiceNow Store to see the app dependency categories.

<table id="table_m42_35g_zcc"><thead><tr><th>

Symbol

</th><th>

Category

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Green check icon](../image/store-green-check.png)

</td><td>

Application is available to install or update

</td><td>

This dependency is already entitled on your instance and is available to install through the Application Manager when you install the app that requires it. For more information about the Application Manager, see [Application Manager](../../application-manager/concept/application-manager.md).

</td></tr><tr><td>

![Red X icon](../image/store-red-x.png)

</td><td>

Unavailable to install application in production

</td><td>

This app isn’t already entitled on your instance, and must be procured before it or the app that requires it can be installed.

 If this app requires purchase, procure it through its ServiceNow Store listing details, or contact you ServiceNow account manager to initiate procurement.

 If this app is available at no additional cost, it's automatically procured with the app that requires it in the following situations:

-   If the app doesn't have custom terms and conditions
-   If the app doesn't require approval from the provider

</td></tr></tbody>
</table>## Unresolved dependencies in procured apps

If you procured an app but it still can't be installed through the Application Manager, you might have unresolved dependencies. You can verify whether there are unresolved dependencies by logging in to the ServiceNow Store and returning to the app listing details. If an application dependency must be procured manually, a red x icon \(![Red X icon](../image/store-red-x.png)\) indicates that the app is unavailable to install in production.

The list of application dependencies contains links that direct you to the ServiceNow Store listing details for each app dependency. From the listing details, you can manually procure the required app.

Plugin dependencies can't be resolved from the ServiceNow Store. For more information about managing plugins, see [ServiceNow plugins](../../plugins/concept/c_ServiceNowPlugins.md).


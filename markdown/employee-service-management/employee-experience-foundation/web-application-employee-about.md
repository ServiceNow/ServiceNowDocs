---
title: App Launcher
description: App Launcher enables you to provide employees one-click access to all of their web business applications from Employee Center.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Setup task management, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# App Launcher

App Launcher enables you to provide employees one-click access to all of their web business applications from Employee Center.

Sync all your business applications from Azure AD and non-SSO, register the custom applications manually, and enable employees to access these applications. You can access the applications from the Employee Center home page widget in context from dynamic topic pages and through search.

App Launcher improves your employee productivity by reducing effort in discovering apps and eliminating the need for using the single-use case SSO dashboards. Using application launcher with the Employee Center Pro, you can manage the following types of applications:

-   **SSO Integrated Apps**: App Launcher offers pre-built integration with Azure AD. If you use Microsoft Entra ID as an identity and access management tool, you can automatically sync the registered applications in your Azure AD account to the App Launcher. Only applications to which the users have access in SSO, such as Microsoft Entra ID, are displayed on Employee Center. The App Launcher framework enables you to integrate with other SSO vendors and sync registered applications. See Integration Hub for the availability of the required spokes, actions, and the license requirements.
-   **Custom web applications \(Non-SSO\)**: Register the applications manually which are not registered in SSO. Register the apps in the Web Application table and define the user criteria to control the visibility.

## SSO and non-SSO app configuration

Configure both SSO integrated Apps and Custom registered apps on the Home page widget or topic page, manage the widget preferences, and associate applications to the topics. As an administrator, you can register applications, sync available applications, and give one-click access to the applications. You can associate topics to the applications to launch useful applications right from within Employee portal.

-   Create a unified application launcher that can increase employee productivity.
-   Configure the integration such as sync SSO-applications, register custom applications, and assign applications to users or groups.
-   Assign custom applications based on the role, location, business unit, team, and other criteria.
-   Define the visibility and access to applications based on the user, user group, and other criteria.
-   Integrate Azure AD and sync the registered applications from connected Azure AD account.
-   Associate application to topics for in-context app discovery.
-   Browse applications by **Favorite**, **Featured**, **categories**, and **Recent**.
-   Improve employee productivity and experience.
-   App launcher is an Employee Center Pro feature.

## My applications user experience and personalization

Organize applications on the App launcher for better app discovery and quick access. Enhance the user experience by simplified browsing experience using Featured, Recent, Categories, and Favorites groups. These features are enabled by default however admins can disable the option or adjust the display preferences.

-   **Categorization**: Admins can map the applications to a suitable category such as finance, IT, events and more. You can create categories and assign the app to one or many app categories.
-   **Featured**: Admins can use this option to promote new or important or seasonal applications for higher visibility. Tag important applications as featured for better visibility. Featured applications have visibility preferences and appear on the top of the page despite any filters or sorting.
-   **Favorites**: Employees can mark the applications as favorite for easy access. Bookmark the apps you use frequently for quicker access.
-   **Recently opened**: Employees can navigate to the recently opened apps from the recently open section.

## Application access and visibility

Enhance application discovery and navigation on the App launcher by configuring the access and visibility settings. Understand how access control can improve the app discovery for employees and find relevant apps that they have access to.

For more information, see [Configure application visibility and access](../task/applauncher-enable-availability.md).

## Application security directive changes

Enhance application security on the App launcher by configuring the following dictionary entries to **Strict Read Only** from **All** &gt; **Employee Center** &gt; **Web Applications** &gt; **Configure** &gt; **Dictionary**.

-   **Application ID**
-   **App source**
-   **Is record updated**

![dictionary field with strict read only](../images/applauncher-dictionary-sec.png "Dictionary entries")

For more information, see [Modify dictionary entries](https://www.servicenow.com/docs/access?context=t_ModifyADictionaryEntryFromAForm&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## App Launcher integration with AI search

Understand how AI Search is integrated with App launcher for better application discovery and access, see [Configure search navigation tabs](../task/config-search-nav-tabs.md).

Ensure you understand how to configure and enable AI search capabilities, see the following AI Search topics:

-   [Configuring AI Search](https://www.servicenow.com/docs/access?context=configuring-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
-   [Configuring navigation tabs in AI Search](https://www.servicenow.com/docs/access?context=config-nav-tabs-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
-   [Search sources](https://www.servicenow.com/docs/access?context=search-sources-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

**Related topics**  


[Register custom web applications with app launcher](../task/web-applications-custom.md)

[Assign topics to web applications](../task/web-applications-topic-assignment.md)

[Sync your applications from Microsoft Entra ID](../task/web-applications-azure.md)

[Modify app launcher widget display](../task/use-app-launcher.md)

[Access applications from App Launcher](web-application-employee.md)

[Configure application visibility and access](../task/applauncher-enable-availability.md)


---
title: ServiceNow Studio release notes
description: The ServiceNow ServiceNow Studio application provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and easily create custom apps. ServiceNow Studio was enhanced and updated in the Yokohama release.The ServiceNow ServiceNow Studio application provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and easily create custom apps. ServiceNow Studio was enhanced and updated in the Yokohama release.The ServiceNow ServiceNow Studio application provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and easily create custom apps. ServiceNow Studio was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# ServiceNow Studio release notes

The ServiceNow® ServiceNow Studio application provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and easily create custom apps. ServiceNow Studio was enhanced and updated in the Yokohama release.

## About ServiceNow Studio

-   Work in the best development environment for your task by using the experience switcher to switch between developing in Creator Studio, ServiceNow Studio, and ServiceNow IDE.
-   As of version 27.2.4, the ServiceNow Studio File Navigator performance has been improved for large applications.
-   As of version 27.2.4, you can easily identify apps created in Creator Studio or ServiceNow IDE by looking at the App Details page in ServiceNow Studio.
-   As of version 27.2.4, the file creation experience is now a full-page, guided process with built-in security checks. Admins see all application files, while delegated developers only see file types they have permission to create within the specified scope.
-   As of version 27.2.4, users with Write permission for an application description can use Now Assist for app summary generation to generate an app summary. The Summarize button is disabled for users without access to edit the app description, preventing failures after clicking.

See  for more information.

## Activation and other requirements

-   **Activation information**

    ServiceNow Studio is a ServiceNow AI Platform feature that is active by default.

-   **Upgrade information**

    ServiceNow Studio no longer has to be downloaded from the ServiceNow Store. It’s available on the ServiceNow AI Platform by default.


## Accessibility and localization

-   **Localization information**

    As of version 27.2.4, there is Right-to-Left language support for ServiceNow Studio.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/build-automate-rn-landing.md)

## May 2025

The ServiceNow® ServiceNow Studio application provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and easily create custom apps. ServiceNow Studio was enhanced and updated in the Yokohama release.

### What's new

-   **File Navigator performance has been improved for large applications**

    As of version 27.2.4, smaller apps load all files on open, while larger apps \(exceeding a configurable limit\) load a subset initially, with additional files available on demand. Search for files in larger apps will perform server-side calls to decrease load times. Contact your ServiceNow support team to change the app size limits.

-   ****

    As of version 27.2.4, use the new full-page, guided file creation experience to create any type of file for which you have permission.

-   ****

    As of version 27.2.4, the app details page for each app shows which development environment your app was created in. Use this information to switch between environments as needed in the course of app development and deployment.


### What's changed

-   ****

    As of version 27.2.4, the available options at the success page for creating an application changed from **Go to app dashboard** to **View App Details** and **Create File**.


## Yokohama

The ServiceNow® ServiceNow Studio application provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and easily create custom apps. ServiceNow Studio was enhanced and updated in the Yokohama release.

### What's new

-   ****

    Use the best tool for your app development by switching between Creator Studio, ServiceNow Studio, and ServiceNow IDE.

-   ****

    Help prevent duplicate app creation by summarizing the contents of an app using Now Assist app summary generation in ServiceNow Studio and using the summary if accurate as the app description.

-   ****

    Change settings or see related links for an app from the app details page. Refresh your app to load updated details.

-   ****

    In the November 2024 release, only admins could create apps in ServiceNow Studio. Now, users with Guided Application Creator \(GAC\) roles can also create applications.


### What's changed

-   ****

    The App settings icon in ServiceNow Studio used to open a small modal where only a few settings could be updated and the app could be deleted. In this release, the icon opens a Core UI view of all the app settings and related links for the app.



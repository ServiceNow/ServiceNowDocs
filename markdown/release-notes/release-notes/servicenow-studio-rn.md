---
title: ServiceNow Studio release notes
description: The ServiceNow ServiceNow Studio application provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and easily create custom apps. ServiceNow Studio was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
---

# ServiceNow Studio release notes

The ServiceNow® ServiceNow Studio application provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and easily create custom apps. ServiceNow Studio was enhanced and updated in the Yokohama release.

## ServiceNow Studio highlights for the Yokohama release

-   Work in the best development environment for your task by using the experience switcher to switch between developing in Creator Studio, ServiceNow Studio, and ServiceNow IDE.
-   As of version 27.2.4, the ServiceNow Studio File Navigator performance has been improved for large applications.
-   As of version 27.2.4, you can easily identify apps created in Creator Studio or ServiceNow IDE by looking at the App Details page in ServiceNow Studio.
-   As of version 27.2.4, the file creation experience is now a full-page, guided process with built-in security checks. Admins see all application files, while delegated developers only see file types they have permission to create within the specified scope.
-   As of version 27.2.4, users with Write permission for an application description can use Now Assist for app summary generation to generate an app summary. The Summarize button is disabled for users without access to edit the app description, preventing failures after clicking.

See [Building applications with ServiceNow Studio](https://www.servicenow.com/docs/access?context=servicenow-studio-landing&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) for more information.

## Important information for upgrading ServiceNow Studio to Yokohama

ServiceNow Studio no longer has to be downloaded from the ServiceNow Store. It’s available on the ServiceNow AI Platform by default.

## New in the Yokohama release

-   **[Change your development experience in ServiceNow Studio](https://www.servicenow.com/docs/access?context=change-your-development-experience&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Use the best tool for your app development by switching between Creator Studio, ServiceNow Studio, and ServiceNow IDE.

-   **[Summarize the contents of an app in ServiceNow Studio](https://www.servicenow.com/docs/access?context=summarize-an-app-in-servicenow-studio&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Help prevent duplicate app creation by summarizing the contents of an app using Now Assist app summary generation in ServiceNow Studio and using the summary if accurate as the app description.

-   **[Modify an app's settings in ServiceNow Studio](https://www.servicenow.com/docs/access?context=modify-an-apps-settings-in-servicenow-studio&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Change settings or see related links for an app from the app details page. Refresh your app to load updated details.

-   **[Create an application in ServiceNow Studio](https://www.servicenow.com/docs/access?context=create-an-application-in-servicenow-studio&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    In the November 2024 release, only admins could create apps in ServiceNow Studio. Now, users with Guided Application Creator \(GAC\) roles can also create applications.

-   **[File Navigator performance has been improved for large applications](https://www.servicenow.com/docs/access?context=configuring-servicenow-studio&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    As of version 27.2.4, smaller apps load all files on open, while larger apps \(exceeding a configurable limit\) load a subset initially, with additional files available on demand. Search for files in larger apps will perform server-side calls to decrease load times. Contact your ServiceNow support team to change the app size limits.

-   **[Create an app file in ServiceNow Studio](https://www.servicenow.com/docs/access?context=sn-studio-create-app-file&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    As of version 27.2.4, use the new full-page, guided file creation experience to create any type of file for which you have permission.

-   **[Viewing app origination information in ServiceNow Studio](https://www.servicenow.com/docs/access?context=viewing-app-origination-information-in-sns&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    As of version 27.2.4, the app details page for each app shows which development environment your app was created in. Use this information to switch between environments as needed in the course of app development and deployment.


## Changed in this release

-   **[Modify an app's settings in ServiceNow Studio](https://www.servicenow.com/docs/access?context=modify-an-apps-settings-in-servicenow-studio&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    The App settings icon in ServiceNow Studio used to open a small modal where only a few settings could be updated and the app could be deleted. In this release, the icon opens a Core UI view of all the app settings and related links for the app.

-   **[Create an application in ServiceNow Studio](https://www.servicenow.com/docs/access?context=create-an-application-in-servicenow-studio&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    As of version 27.2.4, the available options at the success page for creating an application changed from **Go to app dashboard** to **View App Details** and **Create File**.


## Activation information

ServiceNow Studio is a ServiceNow AI Platform feature that is active by default.

## Localization information

As of version 27.2.4, there is Right-to-Left language support for ServiceNow Studio.

## Related ServiceNow applications and features

-   **[Access Control](https://www.servicenow.com/docs/access?context=c_SNCAccessControl&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Work with access controls and roles for apps and files in ServiceNow Studio.

-   **[Catalog Builder](https://www.servicenow.com/docs/access?context=catalog-builder&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Create and edit catalog items directly in ServiceNow Studio.

-   **[Decision tables in Workflow Studio](https://www.servicenow.com/docs/access?context=decision-designer-overview&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Add decision rules and use decision tables to decouple decision logic from code.

-   **[Email notifications](https://www.servicenow.com/docs/access?context=c_EmailNotifications&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Create and edit email notifications that are automatically sent when a record is created or updated. Email notifications are also used as a reference in flows or can be triggered by an event.

-   **[Flows in Workflow Studio](https://www.servicenow.com/docs/access?context=flows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Create and edit flows, subflows, and actions directly in a Workflow Studio tab within ServiceNow Studio.

-   **[Integration Hub - Import](https://www.servicenow.com/docs/access?context=integrationhub-imports&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    Import data into existing tables in ServiceNow Studio.

-   **[Mobile App Builder](https://www.servicenow.com/docs/access?context=mab-concept&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)**

    Add mobile experiences in a Mobile App Builder within ServiceNow Studio.

-   **[Now Assist for app generation in ServiceNow Studio](https://www.servicenow.com/docs/access?context=sns-now-assist-app-gen-landing&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Create applications through a conversation with generative AI.

-   **[Playbooks in Workflow Studio](https://www.servicenow.com/docs/access?context=process-automation-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Edit cross-functional processes and consolidate them into automated task-oriented views.

-   **[Table Builder](https://www.servicenow.com/docs/access?context=tb-landing-page&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Work with data models in a tabular format in a tab within ServiceNow Studio.

-   **[UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    Create and edit experiences in a tab within ServiceNow Studio.

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience within ServiceNow Studio.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)


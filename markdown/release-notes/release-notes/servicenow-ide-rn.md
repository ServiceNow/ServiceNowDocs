---
title: ServiceNow IDE release notes
description: The ServiceNow integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform. ServiceNow IDE was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# ServiceNow IDE release notes

The ServiceNow® integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform. ServiceNow IDE was enhanced and updated in the Australia release.

## ServiceNow IDE highlights for the Australia release

Create or convert applications in the global scope with instances on the Australia release.

See ServiceNow IDE for more information.

**Important:** ServiceNow IDE is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading ServiceNow IDE to Australia

ServiceNow IDE version 3.2.3 is active by default on instances on the Australia release. Update to ServiceNow IDE version 4.0 or later to use the latest features. For information about updating ServiceNow IDE, see Install or update the ServiceNow IDE.

## New in the Australia release

-   **Create and convert global applications**

    Create and convert applications in the global scope that are accessible to other global applications with instances on the Australia release.

-   **Generated ServiceNow Fluent code organized in taxonomy-based directories**

    Configure a custom directory structure for metadata transformed into ServiceNow Fluent code with the `taxonomy` parameter in an application's `now.config.json` file. By default, generated ServiceNow Fluent files are organized in a taxonomy-based directory structure within the `fluent/generated` directory.


## UI changes

-   **Updated Activity Bar**

    The Activity Bar includes additional views for bookmarks and recent activity, and the Metadata Explorer view has been replaced with the File Categories and Apps views.


## Activation information

ServiceNow IDE is active by default and available for upgrade in the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

ServiceNow IDE uses the public npm registry \(`https://registry.npmjs.org`\) as its default package source. If your network blocks access to this registry, you must have access to an alternate registry to download packages and build applications in the ServiceNow IDE. If access to the public npm registry is blocked on your system, you must configure a private npm registry in your Package Manager user settings in the ServiceNow IDE. For more information, see Install an npm package from a private registry with the ServiceNow IDE.

## Localization information

The ServiceNow IDE is localized in all supported left-to-right languages and reflects the language preference selected by users for the instance. For information about how to activate a language on an instance, see Activate a language.

## Related ServiceNow applications and features

-   **ServiceNow SDK**

    The ServiceNow SDK is used in the background of the ServiceNow IDE as the application packaging service that builds applications and provides the ServiceNow Fluent APIs for developing applications in source code. Scoped applications created or converted with the ServiceNow IDE or ServiceNow SDK can be developed with either application.

-   **Build Agent**

    Use Build Agent, an autonomous AI agent, to help you create and edit applications from a chat panel in the ServiceNow IDE.

-   **Now Assist for Code**

    With Now Assist for Code, you can use the Code autocomplete skill to generate code suggestions for scripts in applications in the ServiceNow IDE.

-   **Developer Sandboxes**

    Developer Sandboxes provide admins and delegated developers the ability to request, access, and manage individual sandboxes on top of the same underlying development instance. Delegated Developers can write and merge code and configuration changes without the risk of their changes getting over-written on the instance mid-development.

-   **ReleaseOps**

    ReleaseOps automates deployment of changes across your pipeline, increases predictability and reliability of deployments, and reduces the risk of releasing changes to production.

-   **ServiceNow Studio**

    ServiceNow Studio provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and create custom apps with ease.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)


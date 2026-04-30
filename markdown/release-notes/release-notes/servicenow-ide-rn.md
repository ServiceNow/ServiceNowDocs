---
title: ServiceNow IDE release notes
description: The ServiceNow integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform. ServiceNow IDE was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# ServiceNow IDE release notes

The ServiceNow® integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform. ServiceNow IDE was enhanced and updated in the Zurich release.

## ServiceNow IDE highlights for the Zurich release

-   Clone a Git repository that contains multiple applications.
-   Use light and dark developer themes.
-   Use the ServiceNow IDE in any supported left-to-right language.

See [ServiceNow IDE](https://www.servicenow.com/docs/access?context=servicenow-ide-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

**Important:** ServiceNow IDE is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading ServiceNow IDE to Zurich

ServiceNow IDE version 2.1.2 is active by default on instances on the Zurich release. Update to ServiceNow IDE version 3.0 or later to use the latest features. For information about updating ServiceNow IDE, see [Install or update the ServiceNow IDE](https://www.servicenow.com/docs/access?context=install-servicenow-ide&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## New in the Zurich release

-   **[Clone a repository that contains multiple applications](https://www.servicenow.com/docs/access?context=clone-git-repository-servicenow-ide&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Clone a Git repository that contains multiple applications that support development in source code. The repository must contain at least one `package.json` file and one `now.config.json` file.

-   **[Default to using the latest version of the ServiceNow SDK in new or converted applications](https://www.servicenow.com/docs/access?context=servicenow-ide-properties&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Configure whether to use the bundled version or the latest version of the ServiceNow SDK when creating or converting applications in the ServiceNow IDE with the **sn\_glider.default\_to\_bundled\_sdk** system property. By default, the latest version of the ServiceNow SDK is used.


## UI changes

-   **[New developer themes](https://www.servicenow.com/docs/access?context=servicenow-ide-user-interface&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the Developer Light \(default\) and Developer Dark themes in the ServiceNow IDE. Select a theme from the user settings in the ServiceNow IDE or with the `Preferences: Color Theme` command from the command palette.

    The theme preference selected by a user from the ServiceNow IDE applies to other builder applications such as ServiceNow Studio and Creator Studio.


## Activation information

ServiceNow IDE is active by default and available for upgrade in the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

ServiceNow IDE uses the public npm registry \(`https://registry.npmjs.org`\) as its default package source. If your network blocks access to this registry, you must have access to an alternate registry to download packages and build applications in the ServiceNow IDE. If access to the public npm registry is blocked on your system, you must configure a private npm registry in your Package Manager user settings in the ServiceNow IDE. For more information, see [Install an npm package from a private registry with the ServiceNow IDE](https://www.servicenow.com/docs/access?context=use-library-private-npm-registry&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## Localization information

The ServiceNow IDE is localized in all supported left-to-right languages and reflects the language preference selected by users for the instance. For information about how to activate a language on an instance, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[ServiceNow SDK](https://www.servicenow.com/docs/access?context=servicenow-sdk-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    The ServiceNow SDK is used in the background of the ServiceNow IDE as the application packaging service that builds applications and provides the ServiceNow Fluent APIs for developing applications in source code. Scoped applications created or converted with the ServiceNow IDE or ServiceNow SDK can be developed with either application.

-   **[Build Agent](https://www.servicenow.com/docs/access?context=build-agent&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use Build Agent, an autonomous AI agent, to help you create and edit applications from a chat panel in the ServiceNow IDE.

-   **[Now Assist for Code](https://www.servicenow.com/docs/access?context=now-assist-code-landing&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    With Now Assist for Code, you can use the Code autocomplete skill to generate code suggestions for scripts in applications in the ServiceNow IDE.

-   **[Developer Sandboxes](https://www.servicenow.com/docs/access?context=sandboxes-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Developer Sandboxes provide admins and delegated developers the ability to request, access, and manage individual sandboxes on top of the same underlying development instance. Delegated Developers can write and merge code and configuration changes without the risk of their changes getting over-written on the instance mid-development.

-   **[ReleaseOps](https://www.servicenow.com/docs/access?context=releaseops-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    ReleaseOps automates deployment of changes across your pipeline, increases predictability and reliability of deployments, and reduces the risk of releasing changes to production.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)


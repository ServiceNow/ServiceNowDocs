---
title: ServiceNow IDE release notes
description: The ServiceNow integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform. ServiceNow IDE was enhanced and updated in the Zurich release.The ServiceNow integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform. ServiceNow IDE was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# ServiceNow IDE release notes

The ServiceNow® integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform. ServiceNow IDE was enhanced and updated in the Zurich release.

## About ServiceNow IDE

-   Clone a Git repository that contains multiple applications.
-   Use light and dark developer themes.
-   Use the ServiceNow IDE in any supported left-to-right language.

See  for more information.

## Activation and other requirements

**Important:** ServiceNow IDE is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    ServiceNow IDE is active by default and available for upgrade in the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    ServiceNow IDE version 2.1.2 is active by default on instances on the Zurich release. Update to ServiceNow IDE version 3.0 or later to use the latest features. For information about updating ServiceNow IDE, see .

-   **Additional requirements**

    ServiceNow IDE uses the public npm registry \(`https://registry.npmjs.org`\) as its default package source. If your network blocks access to this registry, you must have access to an alternate registry to download packages and build applications in the ServiceNow IDE. If access to the public npm registry is blocked on your system, you must configure a private npm registry in your Package Manager user settings in the ServiceNow IDE. For more information, see .


## Accessibility and localization

-   **Localization information**

    The ServiceNow IDE is localized in all supported left-to-right languages and reflects the language preference selected by users for the instance. For information about how to activate a language on an instance, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_ActivateALanguage.md).


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/build-automate-rn-landing.md)

## Zurich

The ServiceNow® integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform. ServiceNow IDE was enhanced and updated in the Zurich release.

### What's new

-   **Clone a repository that contains multiple applications**

    Clone a Git repository that contains multiple applications that support development in source code. The repository must contain at least one `package.json` file and one `now.config.json` file.

-   **Default to using the latest version of the ServiceNow SDK in new or converted applications**

    Configure whether to use the bundled version or the latest version of the ServiceNow SDK when creating or converting applications in the ServiceNow IDE with the **sn\_glider.default\_to\_bundled\_sdk** system property. By default, the latest version of the ServiceNow SDK is used.


### What's changed

-   **New developer themes**

    Use the Developer Light \(default\) and Developer Dark themes in the ServiceNow IDE. Select a theme from the user settings in the ServiceNow IDE or with the `Preferences: Color Theme` command from the command palette.

    The theme preference selected by a user from the ServiceNow IDE applies to other builder applications such as ServiceNow Studio and Creator Studio.



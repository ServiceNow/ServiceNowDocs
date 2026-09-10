---
title: ServiceNow IDE release notes
description: The ServiceNow integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform. ServiceNow IDE was enhanced and updated in the Australia release.The ServiceNow integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform. ServiceNow IDE was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# ServiceNow IDE release notes

The ServiceNow® integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform. ServiceNow IDE was enhanced and updated in the Australia release.

## About ServiceNow IDE

Create or convert applications in the global scope with instances on the Australia release.

See  for more information.

## Activation and other requirements

**Important:** ServiceNow IDE is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    ServiceNow IDE is active by default and available for upgrade in the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    ServiceNow IDE version 3.2.3 is active by default on instances on the Australia release. Update to ServiceNow IDE version 4.0 or later to use the latest features. For information about updating ServiceNow IDE, see .

-   **Additional requirements**

    ServiceNow IDE uses the public npm registry \(`https://registry.npmjs.org`\) as its default package source. If your network blocks access to this registry, you must have access to an alternate registry to download packages and build applications in the ServiceNow IDE. If access to the public npm registry is blocked on your system, you must configure a private npm registry in your Package Manager user settings in the ServiceNow IDE. For more information, see .


## Accessibility and localization

-   **Localization information**

    The ServiceNow IDE is localized in all supported left-to-right languages and reflects the language preference selected by users for the instance. For information about how to activate a language on an instance, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateALanguage.md).


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/build-automate-rn-landing.md)

## Australia

The ServiceNow® integrated development environment \(IDE\) application enables developers to create scoped applications in source code in an IDE based on Visual Studio Code for the Web on the ServiceNow AI Platform. ServiceNow IDE was enhanced and updated in the Australia release.

### What's new

-   **Create and convert global applications**

    Create and convert applications in the global scope that are accessible to other global applications with instances on the Australia release.

-   **Generated ServiceNow Fluent code organized in taxonomy-based directories**

    Configure a custom directory structure for metadata transformed into ServiceNow Fluent code with the `taxonomy` parameter in an application's `now.config.json` file. By default, generated ServiceNow Fluent files are organized in a taxonomy-based directory structure within the `fluent/generated` directory.


### What's changed

-   **Updated Activity Bar**

    The Activity Bar includes additional views for bookmarks and recent activity, and the Metadata Explorer view has been replaced with the File Categories and Apps views.



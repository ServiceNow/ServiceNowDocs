---
title: Localization Workspace
description: ServiceNowLocalization Workspace is a targeted translation management experience for content owners and translation fulfillers. With Localization Workspace you can manage and deliver multilingual content at scale. Localization Workspace is a new application in the Yokohama release.ServiceNowLocalization Workspace is a targeted translation management experience for content owners and translation fulfillers. With Localization Workspace you can manage and deliver multilingual content at scale. Localization Workspace is a new application in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-04-18"
reading_time_minutes: 2
---

# Localization Workspace

ServiceNow®Localization Workspace is a targeted translation management experience for content owners and translation fulfillers. With Localization Workspace you can manage and deliver multilingual content at scale. Localization Workspace is a new application in the Yokohama release.

## About Localization Workspace

-   Submit your translation requests from the workspace without having to open a Translation Management System \(TMS\) or other software.
-   Automatically identify and collect all untranslated or partially translated content in scope.
-   Plan and control your localization budget through informational cost estimates.

See [Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/localization-workspace.md) for more information.

## Activation and other requirements

**Important:** Localization Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Localization Workspace by requesting it from the ServiceNow Store. Localization Workspace is available with a Pro or Pro+ subscription. See [Localization Workspace on the ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/03226056b7125210a5e5911cde11a950). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Additional requirements**

    Localization Workspace has the following dependencies:

    -   [Language plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/exploring-system-localization.md) \(i18n\) have been activated according to your requirements.
    -   Localization Framework \(com.glide.localization\_framework.installer\) has been installed and configured.
    -   Dynamic Translation \(com.glide.dynamic\_translation\) has been installed and configured if using machine translation to fulfill translation requests.
    These dependencies are activated automatically with the installation of Localization Workspace.


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-admin-rn-landing.md)

## Yokohama

ServiceNow®Localization Workspace is a targeted translation management experience for content owners and translation fulfillers. With Localization Workspace you can manage and deliver multilingual content at scale. Localization Workspace is a new application in the Yokohama release.

### What's new

-   **Process translation requests in one interface**

    The following Localization Workspace workflow is accomplished in a single location:

    -   Preconfigure languages and translation providers.
    -   Choose your content type, such as KB articles or notifications, then select specific texts to translate.
    -   Generate cost estimates, then submit translation requests to third-party providers.
    -   Track and manage all open requests.
-   **[Request translations from English into other languages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/exploring-localization-workspace.md)**

    In this initial release, only translation requests where the current language of the source document is English and the language of the target is something other than English are supported.

-   **[Many types of content can be localized](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/lw-localizable-content.md)**

    Many types of text content can be localized, subject to table permissions. Surveys are not a supported content type.



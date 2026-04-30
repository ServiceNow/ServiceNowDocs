---
title: Localization Workspace
description: ServiceNowLocalization Workspace is a targeted translation management experience for content owners and translation fulfillers. With Localization Workspace you can manage and deliver multilingual content at scale. Localization Workspace is a new application in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-18"
reading_time_minutes: 2
---

# Localization Workspace

ServiceNow®Localization Workspace is a targeted translation management experience for content owners and translation fulfillers. With Localization Workspace you can manage and deliver multilingual content at scale. Localization Workspace is a new application in the Yokohama release.

## Localization Workspace highlights for the Yokohama release

-   Submit your translation requests from the workspace without having to open a Translation Management System \(TMS\) or other software.
-   Automatically identify and collect all untranslated or partially translated content in scope.
-   Plan and control your localization budget through informational cost estimates.

See [Localization Workspace](https://www.servicenow.com/docs/access?context=localization-workspace&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.

**Important:** Localization Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Localization Workspace features

-   **Process translation requests in one interface**

    The following Localization Workspace workflow is accomplished in a single location:

    -   Preconfigure languages and translation providers.
    -   Choose your content type, such as KB articles or notifications, then select specific texts to translate.
    -   Generate cost estimates, then submit translation requests to third-party providers.
    -   Track and manage all open requests.
-   **[Request translations from English into other languages](https://www.servicenow.com/docs/access?context=exploring-localization-workspace&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    In this initial release, only translation requests where the current language of the source document is English and the language of the target is something other than English are supported.

-   **[Many types of content can be localized](https://www.servicenow.com/docs/access?context=lw-localizable-content&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Many types of text content can be localized, subject to table permissions. Surveys are not a supported content type.


## Activation information

Install Localization Workspace by requesting it from the ServiceNow Store. Localization Workspace is available with a Pro or Pro+ subscription. See [Localization Workspace on the ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/03226056b7125210a5e5911cde11a950). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

Localization Workspace has the following dependencies:

-   [Language plugins](https://www.servicenow.com/docs/access?context=exploring-system-localization&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) \(i18n\) have been activated according to your requirements.
-   Localization Framework \(com.glide.localization\_framework.installer\) has been installed and configured.
-   Dynamic Translation \(com.glide.dynamic\_translation\) has been installed and configured if using machine translation to fulfill translation requests.

These dependencies are activated automatically with the installation of Localization Workspace.

## Related ServiceNow applications and features

-   **[Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    With Dynamic Translation configured, you can use machine translation on your instance to translate text such as user-entered text on forms.

-   **[Localization Framework](https://www.servicenow.com/docs/access?context=localization-framework-landing&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Localization Framework standardizes and enhances the translation process of artifacts across the platform through configurable workflows. Localization Workspace leverages and builds upon Localization Framework capabilities.

-   **[System Localization](https://www.servicenow.com/docs/access?context=system-localization-landing&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    System Localization enables administrators to accommodate users from a variety of different countries using different languages and currencies within the same instance.


**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)


---
title: Combined Localization Workspace release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Localization Workspace from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-localizationworkspace-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Localization Workspace release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Localization Workspace from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Localization Workspace release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Localization Workspace to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Localization Workspace.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Process translation requests in one interface](https://www.servicenow.com/docs/access?context=using-localization-workspace&family=yokohama&ft:locale=en-US)**

The following Localization Workspace workflow is accomplished in a single location:

    -   Preconfigure languages and translation providers.
    -   Choose your content type, such as KB articles or notifications, then select specific texts to translate.
    -   Generate cost estimates, then submit translation requests to third-party providers.
    -   Track and manage all open requests.
-   **[Request translations from English into other languages](https://www.servicenow.com/docs/access?context=exploring-localization-workspace&family=yokohama&ft:locale=en-US)**

In this initial release, only translation requests where the current language of the source document is English and the language of the target is something other than English are supported.

-   **[Many types of content can be localized](https://www.servicenow.com/docs/access?context=lw-localizable-content&family=yokohama&ft:locale=en-US)**

Many types of text content can be localized, subject to table permissions. Surveys are not a supported content type.


</td></tr><tr><td>

Zurich

</td><td>

-   **Guided Setups for [Configuring Localization Workspace](https://www.servicenow.com/docs/access?context=configuring-localization-workspace&family=zurich&ft:locale=en-US)**

Two Guided Setups are available in the interface to assist admins with configuration of Localization Workspace. Guided Setups provide an outline and actionable steps for the configuration process. From version 2.0.2.

-   **[Configuration hub](https://www.servicenow.com/docs/access?context=lw-configuration-hub&family=zurich&ft:locale=en-US)**

Configuration Hub provides centralized access to the tables and properties often used by admins. You can update the tables and properties of dependent applications such as Dynamic Translation without leaving the Localization Workspace interface. From version 2.0.2.

-   **[Language Groups](https://www.servicenow.com/docs/access?context=lw-configure-language-groups&family=zurich&ft:locale=en-US)**

You can optionally preconfigure language groups. Your users save time and effort by selecting an available language group rather than adding each target language individually to a translation request. From version 2.0.2.

-   **[Bulk select or deselect for content items](https://www.servicenow.com/docs/access?context=lw-request-translations-scope&family=zurich&ft:locale=en-US)**

When users create a translation request, Localization Workspace retrieves and displays all translatable documents for a content type. A bulk select/deselect option is available on the retrieved list to enhance efficiency. From version 2.0.2.

-   **[Text search for content items](https://www.servicenow.com/docs/access?context=lw-request-translations-scope&family=zurich&ft:locale=en-US)**

When users create a translation request, Localization Workspace retrieves and displays translatable content items in a list. You can search for terms in the titles of content items to filter the retrieved list. From version 2.0.2.

-   **[Optional due date field for translation requests](https://www.servicenow.com/docs/access?context=lw-estimate&family=zurich&ft:locale=en-US)**

Your users can enter a due date when creating a translation request. Translation request due dates can be used to trigger [email notifications](https://www.servicenow.com/docs/access?context=lw-email-notif-due-dates&family=zurich&ft:locale=en-US). From version 2.0.2.


</td></tr><tr><td>

Australia

</td><td>

-   **[Export a glossary from Language Asset Management](https://www.servicenow.com/docs/access?context=lw-lam-export-glossary&family=australia&ft:locale=en-US)**

Download a glossary from Language Asset Management as a CSV or spreadsheet file. From version 3.1.0.

-   **[Terminology Manager role](https://www.servicenow.com/docs/access?context=localization-workspace-roles&family=australia&ft:locale=en-US)**

Control access to glossary and terminology management with the Terminology Manager role \(sn\_lw.terminology\_manager\). This role contains roles that were previously contained in sn\_lw.user. The sn\_lw.user role is required for all users in Localization Workspace. From version 3.1.0.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Localization Workspace features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


 -   **[Dynamic artifact detection](https://www.servicenow.com/docs/access?context=lw-dynamic-artifact-detection&family=zurich&ft:locale=en-US)**

Dynamic artifact detection enables Localization Workspace to identify all translatable content, including your custom artifacts. From version 1.1.0.

-   **[Status synchronization](https://www.servicenow.com/docs/access?context=lw-status-synchronization&family=zurich&ft:locale=en-US)**

With status synchronization, you see the same status for your translation request in Localization Workspace as you see for the corresponding project in Localization Framework \(Submitted, In progress, Complete\). From version 1.1.0.


</td></tr><tr><td>

Australia

</td><td>

-   **[Cancel translation requests, delete draft requests, and review archived requests from the landing page](https://www.servicenow.com/docs/access?context=lw-status-synchronization&family=australia&ft:locale=en-US)**

Monitor and control your requests on the landing page with functions to cancel translation requests, delete draft requests, and review archived requests.

-   **[View the translation method from the translation request summary](https://www.servicenow.com/docs/access?context=lw-status-synchronization&family=australia&ft:locale=en-US)**

View the translation method, such as TMS or machine translation, from the translation request summary. The summary is available from the My Requests list on the landing page.

-   **[Use intelligent due date suggestions based on the size and scope of your requests](https://www.servicenow.com/docs/access?context=lw-estimate&family=australia&ft:locale=en-US)**

Use intelligent due date suggestions, which provide an estimated completion date for your translations, based on the size and scope of your translation request. You can accept the suggested due date when submitting your request.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Localization Workspace features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Localization Workspace features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Localization Workspace.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Localization Workspace by requesting it from the ServiceNow Store. See [Localization Workspace on the ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/03226056b7125210a5e5911cde11a950). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Localization Workspace by requesting it from the ServiceNow Store. See [Localization Workspace on the ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/03226056b7125210a5e5911cde11a950). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Localization Workspace we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Localization Workspace we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Localization Workspace, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Localization Workspace we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Localization Workspace we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   Dynamic artifact detection enables Localization Workspace to identify all translatable content, including your custom artifacts. From version 1.1.0.
-   With status synchronization, translation requests in Localization Workspace reflect the same status as the Localization Framework projects. From version 1.1.0.
-   A Configuration hub and two new Guided Setups are available to help admins configure Localization Workspace. From version 2.0.2.
-   Optional due dates and language groups enhance the efficiency of creating translation requests. From version 2.0.2.
-   When selecting specific documents to translate, translation requestors can take advantage of a bulk select/deselect option as well as text search of document titles. From version 2.0.2.

 See [Localization Workspace](https://www.servicenow.com/docs/access?context=localization-workspace&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Set up language providers and language groups with confidence, assisted by the new Guided Tours in the Localization Workspace interface.
-   Upload your glossaries to the new **Language Asset Management** tab for editing and storage.
-   Export a glossary from **Language Asset Management**.From version 3.1.0.
-   Assign the Terminology Manager role to users working with glossaries in **Language Asset Management**. From version 3.1.0.
-   Cancel translation requests, delete draft requests, and review archived requests from the Localization Workspace landing page.
-   View the translation method from the translation request summary.
-   Use intelligent due date suggestions based on the size and scope of your requests when creating translation requests.

 See [Localization Workspace](https://www.servicenow.com/docs/access?context=localization-workspace&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)


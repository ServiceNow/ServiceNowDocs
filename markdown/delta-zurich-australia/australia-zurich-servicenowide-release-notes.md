---
title: Combined ServiceNow IDE release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for ServiceNow IDE from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-servicenowide-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined ServiceNow IDE release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for ServiceNow IDE from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow IDE release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow IDE to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

ServiceNow IDE version 2.1.2 is active by default on instances on the Zurich release. Update to ServiceNow IDE version 3.0 or later to use the latest features. For information about updating ServiceNow IDE, see [Install or update the ServiceNow IDE](https://www.servicenow.com/docs/access?context=install-servicenow-ide&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

ServiceNow IDE version 3.2.3 is active by default on instances on the Australia release. Update to ServiceNow IDE version 4.0 or later to use the latest features. For information about updating ServiceNow IDE, see [Install or update the ServiceNow IDE](https://www.servicenow.com/docs/access?context=install-servicenow-ide&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ServiceNow IDE.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Clone a repository that contains multiple applications](https://www.servicenow.com/docs/access?context=clone-git-repository-servicenow-ide&family=zurich&ft:locale=en-US)**

Clone a Git repository that contains multiple applications that support development in source code. The repository must contain at least one `package.json` file and one `now.config.json` file.

-   **[Default to using the latest version of the ServiceNow SDK in new or converted applications](https://www.servicenow.com/docs/access?context=servicenow-ide-properties&family=zurich&ft:locale=en-US)**

Configure whether to use the bundled version or the latest version of the ServiceNow SDK when creating or converting applications in the ServiceNow IDE with the **sn\_glider.default\_to\_bundled\_sdk** system property. By default, the latest version of the ServiceNow SDK is used.


</td></tr><tr><td>

Australia

</td><td>

-   **[Create and convert global applications](https://www.servicenow.com/docs/access?context=creating-applications-servicenow-ide&family=australia&ft:locale=en-US)**

Create and convert applications in the global scope that are accessible to other global applications with instances on the Australia release.

-   **[Generated ServiceNow Fluent code organized in taxonomy-based directories](https://www.servicenow.com/docs/access?context=building-applications-source-code&family=australia&ft:locale=en-US)**

Configure a custom directory structure for metadata transformed into ServiceNow Fluent code with the `taxonomy` parameter in an application's `now.config.json` file. By default, generated ServiceNow Fluent files are organized in a taxonomy-based directory structure within the `fluent/generated` directory.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow IDE features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ServiceNow IDE features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some ServiceNow IDE features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ServiceNow IDE.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

ServiceNow IDE is active by default and available for upgrade in the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

ServiceNow IDE is active by default and available for upgrade in the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow IDE we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

ServiceNow IDE uses the public npm registry \(`https://registry.npmjs.org`\) as its default package source. If your network blocks access to this registry, you must have access to an alternate registry to download packages and build applications in the ServiceNow IDE. If access to the public npm registry is blocked on your system, you must configure a private npm registry in your Package Manager user settings in the ServiceNow IDE. For more information, see [Install an npm package from a private registry](https://www.servicenow.com/docs/access?context=use-library-private-npm-registry&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

ServiceNow IDE uses the public npm registry \(`https://registry.npmjs.org`\) as its default package source. If your network blocks access to this registry, you must have access to an alternate registry to download packages and build applications in the ServiceNow IDE. If access to the public npm registry is blocked on your system, you must configure a private npm registry in your Package Manager user settings in the ServiceNow IDE. For more information, see [Install an npm package from a private registry](https://www.servicenow.com/docs/access?context=use-library-private-npm-registry&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow IDE we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ServiceNow IDE, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ServiceNow IDE we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

The ServiceNow IDE is localized in all supported left-to-right languages and reflects the language preference selected by users for the instance. For information about how to activate a language on an instance, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

The ServiceNow IDE is localized in all supported left-to-right languages and reflects the language preference selected by users for the instance. For information about how to activate a language on an instance, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ServiceNow IDE we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Clone a Git repository that contains multiple applications.
-   Use light and dark developer themes.
-   Use the ServiceNow IDE in any supported left-to-right language.

 See [ServiceNow IDE](https://www.servicenow.com/docs/access?context=servicenow-ide-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

Create or convert applications in the global scope with instances on the Australia release.

 See [ServiceNow IDE](https://www.servicenow.com/docs/access?context=servicenow-ide-landing&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)


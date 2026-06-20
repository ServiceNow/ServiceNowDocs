---
title: Combined ServiceNow IDE release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for ServiceNow IDE from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-servicenowide-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined ServiceNow IDE release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for ServiceNow IDE from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow IDE release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow IDE to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

ServiceNow IDE version 1.1.4 is active by default on instances on the Yokohama release. Update to ServiceNow IDE version 2.0 or later to use the latest features. For information about updating ServiceNow IDE, see [Updating apps](https://servicenow-staging.fluidtopics.net/access?context=updating-apps-app-manager&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

ServiceNow IDE version 2.1.2 is active by default on instances on the Zurich release. Update to ServiceNow IDE version 3.0 or later to use the latest features. For information about updating ServiceNow IDE, see [Install or update the ServiceNow IDE](https://servicenow-staging.fluidtopics.net/access?context=install-servicenow-ide&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for ServiceNow IDE.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Work in an IDE based on Visual Studio Code for the Web](https://servicenow-staging.fluidtopics.net/access?context=servicenow-ide-user-interface&family=xanadu&ft:locale=en-US)**

Create and develop applications in a familiar integrated development environment based on Visual Studio Code for the Web. The ServiceNow IDE has many of the same features as Visual Studio Code, including type safety, IntelliSense, dependency enforcement, code search, and source control integration.

-   **[Build scoped applications in source code](https://servicenow-staging.fluidtopics.net/access?context=servicenow-fluent&family=xanadu&ft:locale=en-US)**

Write source code to define the metadata that makes up applications using ServiceNow Fluent. ServiceNow Fluent is a domain-specific programming language with APIs for defining the different types of application metadata. Developing applications in source code enables you to work in familiar development environments, create and modify complex applications, manage code in source control more easily, and catch errors at build time. Language processing and validation for ServiceNow Fluent is included in the ServiceNow IDE by default.

-   **[Create and use JavaScript modules and third-party libraries](https://servicenow-staging.fluidtopics.net/access?context=create-use-javascript-modules-ide&family=xanadu&ft:locale=en-US)**

Organize and reuse code within scoped applications with custom JavaScript modules and third-party JavaScript utilities.

-   **[Collaborate on applications with users of different skill sets](https://servicenow-staging.fluidtopics.net/access?context=developing-applications-servicenow-ide&family=xanadu&ft:locale=en-US)**

Collaborate on an application with users of different skill sets at the same time from the ServiceNow IDE and other ServiceNow AI Platform builder tools and interfaces. Developers build applications to compile source files into metadata, which they can view in embedded ServiceNow AI Platform user interfaces. Developers can synchronize applications to pull in changes to application metadata from other interfaces into source code.

-   **[Manage applications in source control](https://servicenow-staging.fluidtopics.net/access?context=integrating-source-control-servicenow-ide&family=xanadu&ft:locale=en-US)**

Integrate with remote Git repositories to use source control in the ServiceNow IDE. Use basic authentication or OAuth 2.0 to connect to remote Git providers and repositories.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Convert scoped applications for use in the ServiceNow IDE](https://servicenow-staging.fluidtopics.net/access?context=convert-application-servicenow-ide&family=yokohama&ft:locale=en-US)**

Convert existing scoped applications to support development in source code in the ServiceNow IDE.

-   **[Use TypeScript in JavaScript modules](https://servicenow-staging.fluidtopics.net/access?context=create-application-servicenow-ide&family=yokohama&ft:locale=en-US)**

Create an application that uses the TypeScript template to use TypeScript in modules and compile them to JavaScript when building your application.

-   **[Use npm packages from private registries as third-party libraries](https://servicenow-staging.fluidtopics.net/access?context=use-library-private-npm-registry&family=yokohama&ft:locale=en-US)**

Install npm packages from a private registry to use as third-party libraries in your application.

-   **[Switch between development experiences](https://servicenow-staging.fluidtopics.net/access?context=servicenow-ide-user-interface&family=yokohama&ft:locale=en-US)**

Work in the right environment for your task by using the experience switcher to switch between developing in ServiceNow IDE, ServiceNow Studio, and Creator Studio.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Clone a repository that contains multiple applications](https://servicenow-staging.fluidtopics.net/access?context=clone-git-repository-servicenow-ide&family=zurich&ft:locale=en-US)**

Clone a Git repository that contains multiple applications that support development in source code. The repository must contain at least one `package.json` file and one `now.config.json` file.

-   **[Default to using the latest version of the ServiceNow SDK in new or converted applications](https://servicenow-staging.fluidtopics.net/access?context=servicenow-ide-properties&family=zurich&ft:locale=en-US)**

Configure whether to use the bundled version or the latest version of the ServiceNow SDK when creating or converting applications in the ServiceNow IDE with the **sn\_glider.default\_to\_bundled\_sdk** system property. By default, the latest version of the ServiceNow SDK is used.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing ServiceNow IDE features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some ServiceNow IDE features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some ServiceNow IDE features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Xanadu

</td><td>

Install ServiceNow IDE \(sn\_glider\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

ServiceNow IDE is active by default starting in the Yokohama release and available for upgrade in the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

ServiceNow IDE is active by default and available for upgrade in the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow IDE we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

ServiceNow IDE uses the public npm registry \(`https://registry.npmjs.org`\) as its default package source. If your network blocks access to this registry, you must have access to an alternate registry to download packages and build applications in the ServiceNow IDE. If access to the public npm registry is blocked on your system, you must configure a private npm registry in your Package Manager user settings in the ServiceNow IDE. For more information, see [Install an npm package from a private registry](https://servicenow-staging.fluidtopics.net/access?context=use-library-private-npm-registry&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow IDE we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

The ServiceNow IDE is localized in all supported left-to-right languages and reflects the language preference selected by users for the instance. For information about how to activate a language on an instance, see [Activate a language](https://servicenow-staging.fluidtopics.net/access?context=t_ActivateALanguage&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ServiceNow IDE we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Develop scoped applications in an IDE based on Visual Studio Code on the ServiceNow AI Platform.
-   Write source code to define the metadata that makes up applications with ServiceNow Fluent.
-   Collaborate with users of different skill sets across an instance and view changes in embedded ServiceNow AI Platform user interfaces.
-   Manage applications in source control with common Git providers.

 See [ServiceNow IDE](https://servicenow-staging.fluidtopics.net/access?context=servicenow-ide-landing&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Convert existing scoped applications to support development in source code.
-   Use TypeScript in JavaScript modules.
-   Install and use npm packages from private registries.

 See [ServiceNow IDE](https://servicenow-staging.fluidtopics.net/access?context=servicenow-ide-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Clone a Git repository that contains multiple applications.
-   Use light and dark developer themes.
-   Use the ServiceNow IDE in any supported left-to-right language.

 See [ServiceNow IDE](https://servicenow-staging.fluidtopics.net/access?context=servicenow-ide-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)


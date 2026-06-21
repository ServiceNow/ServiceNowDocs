---
title: Combined Skills Foundation release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Skills Foundation from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-skillsfoundation-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Skills Foundation release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Skills Foundation from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Skills Foundation release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Skills Foundation to Australia

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

You cannot download industry skills data as part of the guided setup.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Skills Foundation.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Skills import](https://www.servicenow.com/docs/access?context=import-and-validate-custom-skills-onboarding&family=yokohama&ft:locale=en-US)**

Import skill sets from the Workday Employee spoke using the existing import flow in the Skills Workspace. The imported sets of skills can either be the full list of skills from a given input or a subset.

Import skills data from the external systems with the new Integration option in the Skills import.

Automatically identify skills that are similar to the existing skills in the library \(cmn\_skills\) and display them in the Existing matches section.

Import skills from any external source and harmonize them with the new **Custom import** option.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Skills Foundation features.

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

-   **[Skills Intelligence](https://www.servicenow.com/docs/access?context=skills-intelligence&family=zurich&ft:locale=en-US)**

Skills search is powered by AI Search capability instead of machine learning models. You can configure the skill search to be indexed based on the skill name or description or both. For Pro Plus License \(i.e. LLM Integration\) customers, AI search with RAG configuration is provided to power skill search.

Multilingual skill support is limited to the languages supported by AI Search, which is fewer than the previously supported 23 languages.

Resume parsing is done using Now Assist.

ITSM skills previously stored in the CDS plugin were moved back to the seed data plugin.


-   **[Skills Intelligence Workspace](https://www.servicenow.com/docs/access?context=skills-intelligence-workspace&family=zurich&ft:locale=en-US)**

The application name Skills Intelligence Workspace has been changed to Skills Workspace.

Role group skill recommendations will not be readily available unless you load your own ontology data to the industry plugin.

In Skill Harmonization, duplicate skills identification relies on AI search instead of ML models, which will have some quality impact in identifying duplicates.

In Skills Import, two new integration options are added for SAP SuccessFactors and skills and user skills imported go through harmonization pipeline.


-   **[Career tab in Employee Center](https://www.servicenow.com/docs/access?context=manage-skills-profile&family=zurich&ft:locale=en-US)**

In the Career tab, the recommended skills source is now derived both from skills that are tagged to activities that employees has been pursuing and from similar user skills.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Skills Foundation features or functionality were removed.

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

-   The LinkedIn Parsing capability is not supported because it is based on ML models.
-   The skills ontology, which contained skill structure with categories and definition, is no longer provided. Supply your own skills data and import it into the Skills Foundation application.
-   Legacy Data Science algorithms from Talent Development applications.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Skills Foundation features or functionality were deprecated.

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

Review information on how to activate Skills Foundation.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install Skills Foundation by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Skills Foundation by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Skills Foundation we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

The Skills Workspace plugin \(sn\_skills\_int\_ws\) must be installed to access the workspace experience.

</td></tr><tr><td>

Zurich

</td><td>

-   The Human Resources Scoped App \(sn\_hr\_core\) plugin on Australia family release must be installed for HR profile and Talent job profile synchronization.

**Note:** For earlier releases, you might encounter Restricted Caller Access \(RCA\) approval messages requesting for an update in the access request. Approve the message and re-import the plugin manually.

-   The Skills foundation \(sn\_skills\_int\) v 10.0 for the skills foundation features.
-   The Skills Workspace plugin \(sn\_skills\_int\_ws\) v 6.1 must be installed to access the workspace experience.
-   HRSD integration for SAP SuccessFactors \(sn\_hr\_sf\) Plugin which depends on SuccessFactors \(sn\_successfactors\) spoke v 4.6.1-7 to fetch skills and user skills data.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Skills Foundation we have noted them here.

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

Review details on accessibility information for Skills Foundation, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for Skills Foundation we have noted them here.

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

If there are specific highlight considerations for Skills Foundation we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Skill Harmonization lets you import and combines skills from the external learning management system \(LMS\) to have one source for skills.
-   Integrating Workday Learning skills and Workday Employee skills into the current import flow and relate them to the respective employees in the ServiceNow system.
-   Support for dynamic skills import requests from Credly \(OOTB source\) and other external sources. The skills are verified with the skills library \(exact or mapped match\), and new skills are added to the queue for processing. The harmonized skills are then linked back to the source using metadata.

 See [Skills Intelligence](https://www.servicenow.com/docs/access?context=skills-intelligence&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   The Skills Intelligence application name has been changed to Skills Foundation.
-   The skills ontology, which contained skill structure with categories and definition, is no longer provided. Supply your own skills data and import it into the Skills Foundation application.
-   Efficient skill search mechanism is provided by replacing machine learning models with AI search and AI search with RAG configuration for Pro Plus License \(i.e. LLM Integration\) customers.
-   Automatic HR job profile and Talent job profile synchronization when a new employee joins the organization, or​ an existing employee changes position. You must have Human Resources Scoped App \(sn\_hr\_core\) installed for this feature to work.
-   Integration between SAP SuccessFactors and ServiceNow enables customers to import skills and user skills into ServiceNow, unlocking Growth Experiences features and driving higher adoption​. The integration feature will only work for the customers who are using Job Profile Builder and will not work for those who are using Talent Intelligence Hub.

 See [Skills Intelligence](https://www.servicenow.com/docs/access?context=skills-intelligence&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)


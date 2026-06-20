---
title: Combined Clone Admin Console release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Clone Admin Console from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-cloneadminconsole-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Clone Admin Console release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Clone Admin Console from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Clone Admin Console release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Clone Admin Console to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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
</table>## New features

Between your current release family and Zurich, new features were introduced for Clone Admin Console.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Request a clone in Clone Admin Console](https://servicenow-staging.fluidtopics.net/access?context=clone-ui-request-clone&family=washingtondc&ft:locale=en-US)**

The app features a simplified clone request page with guidance and explanations for how various settings affect your clone. The new request page also features a scheduling tool to help prevent timing conflicts between the automatic rescheduling of clones and infrastructure maintenance windows.

-   **[Guidance](https://servicenow-staging.fluidtopics.net/access?context=Clone-UI&family=washingtondc&ft:locale=en-US)**

Learn how some clone options may affect your clone time with added information and guidance.

-   **[On-demand backup option](https://servicenow-staging.fluidtopics.net/access?context=clone-ui-request-clone&family=washingtondc&ft:locale=en-US)**

Use a fresh backup as part of your clone. This option can be useful if you want to include newly published changes in your clone and you don’t want to wait for the next nightly backup.

-   **[Clone Logs](https://servicenow-staging.fluidtopics.net/access?context=Clone-UI&family=washingtondc&ft:locale=en-US)**

See the **Show Logs** link that is added to display the Clone Logs on the Clone Status page when selected.

-   **[Recurring clones](https://servicenow-staging.fluidtopics.net/access?context=Clone-UI&family=washingtondc&ft:locale=en-US)**

Create recurring clones using the clone frequency options on the clone request page. The clone frequencies are **Weekly**, **Every two weeks**, and **Every four weeks**.

**Note:** Each occurrence is created as a separate clone request. If changes are required, you must change the individual clone requests that are created.

-   **[Target instance modal](https://servicenow-staging.fluidtopics.net/access?context=clone-ui-request-clone&family=washingtondc&ft:locale=en-US)**

Add an instance or select an existing instance without leaving the page using the **add an instance** option in the **clone request target instance** field.

-   **[Use the same backup as another clone](https://servicenow-staging.fluidtopics.net/access?context=clone-ui-request-clone&family=washingtondc&ft:locale=en-US)**

Use the same backup as another clone when selecting a backup option. If the backup no longer exists, it triggers an on-demand backup instead.

-   **[Clone storage](https://servicenow-staging.fluidtopics.net/access?context=clone-ui-request-clone&family=washingtondc&ft:locale=en-US)**

Legacy clones and new clones are stored separately. Clones requested via the Clone Admin Console are stored on a new table and displayed within the new console.  Legacy clones aren't shown in the console. Clones initiated via the legacy Request Clone page are stored on the legacy Clone History table.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Target instance modal](https://servicenow-staging.fluidtopics.net/access?context=clone-ui-request-clone&family=xanadu&ft:locale=en-US)**

Request a clone to copy the data from a production instance to a non-production instance or to copy the data between non-production instances. You can request a clone without leaving the form by using the **add an instance** option in the **clone request target instance** field.

-   **[Using the same backup from another clone](https://servicenow-staging.fluidtopics.net/access?context=Clone-UI&family=xanadu&ft:locale=en-US)**

Use the backup from another clone when you're selecting a backup option for a faster backup process. If the backup no longer exists, it triggers an on-demand backup instead.

-   **[Clone storage](https://servicenow-staging.fluidtopics.net/access?context=Clone-UI&family=xanadu&ft:locale=en-US)**

Legacy clones and new clones are stored separately. Clones that you request via the Clone Admin Console are stored on a new table and displayed within the new console.  Legacy clones aren't shown in the Clone Admin Console. Clones that you initiate via the legacy Request Clone page are stored on the legacy Clone History table.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Clone Admin Console features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Between your current release family and Zurich, some Clone Admin Console features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

The requirement to have at least one custom preserver in any custom clone profile for a clone request to be placed has been removed. You can now have a custom clone profile with only base system preservers to place a clone request.

</td></tr><tr><td>

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

Between your current release family and Zurich, some Clone Admin Console features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

-   The legacy clone request page clone\_instance.DO is going to be retired in the A release.
-   Update to the latest version for the best experience and performance improvements. To update Clone Admin Console, see [Clone Home \(dashboard\)](https://servicenow-staging.fluidtopics.net/access?context=Clone-UI&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Clone Admin Console.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Clone Admin Console is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

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

Install the Clone Admin Console by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Clone Admin Console we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Clone Admin Console we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Review details on accessibility information for Clone Admin Console, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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

If there are specific localization considerations for Clone Admin Console we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

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
</table>## Highlight information

If there are specific highlight considerations for Clone Admin Console we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Experience a simplified clone request experience.
-   Help prevent timing conflicts with a new scheduling tool.
-   Use the dashboard to view current clone activity with enhanced visibility.
-   View additional personalization options on the homepage list view.
-   Internationalization provides Clone Admin Console in multiple languages.

 See [Clone Admin Console](https://servicenow-staging.fluidtopics.net/access?context=Clone-UI&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Use a new backup when you’re backing up the Clone Admin Console to make the backup go more quickly.
-   View the Clone preserver guidance added to the Create a clone form to understand how to use Clone preservers.
-   Clone related queries now go through ACLs. Custom clone flows should be tested.

 See [Clone Admin Console](https://servicenow-staging.fluidtopics.net/access?context=Clone-UI&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   Configure the update set preservation up to 12 minutes before the clone executes.
-   Preserve your in-progress update sets, regardless of when the scope was created in the specified time frame.


 See [Clone Home \(dashboard\)](https://servicenow-staging.fluidtopics.net/access?context=Clone-UI&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)


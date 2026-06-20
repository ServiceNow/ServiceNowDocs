---
title: Combined Dispute Rules Content Pack for Visa release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Dispute Rules Content Pack for Visa from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-disputerulescontentpackforvisa-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Dispute Rules Content Pack for Visa release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Dispute Rules Content Pack for Visa from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Dispute Rules Content Pack for Visa release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Dispute Rules Content Pack for Visa to Zurich

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

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Dispute Rules Content Pack for Visa.

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
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Dispute Rules Content Pack for Visa features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Questionnaire and chargeback eligibility ruless](https://servicenow-staging.fluidtopics.net/access?context=reason-codes-supported-in-dispute-rules-content-pack-for-visa&family=xanadu&ft:locale=en-US)**
    -   Added new chargeback eligibility rules to reflect the latest dispute conditions from Visa.
    -   Updated the dispute questionnaire to support the following reason codes:
        -   10.3 \(Other fraud—card-present environment\)
        -   13.1 \(Merchandise/services not received\)
        -   13.5 \(Misrepresentation\)
-   **[Visa Resolve Online \(VROL\) 24.2 revision Alignment](https://servicenow-staging.fluidtopics.net/access?context=reason-codes-supported-in-dispute-rules-content-pack-for-visa&family=xanadu&ft:locale=en-US)**
    -   Updated chargeback reason codes and dispute questionnaire with VROL's latest release revision 24.2.
    -   Updated 12.1 chargeback rules to 11.3.
-   **[Visa Resolve Online \(VROL\) 25.2 revision Alignment](https://servicenow-staging.fluidtopics.net/access?context=reason-codes-supported-in-dispute-rules-content-pack-for-visa&family=xanadu&ft:locale=en-US)**

The chargeback eligibility rule under the 12.6 reason code that validates **Is the other transaction paid by other means? == N** has been removed,

-   **[Updated references in Card Operations tables](https://servicenow-staging.fluidtopics.net/access?context=components-installed-with-dispute-rules-content-pack-for-visa&family=xanadu&ft:locale=en-US)**

Updated references from the old questionnaire tables to the new intake tables in Card Operations.

-   **[Updated data model](https://servicenow-staging.fluidtopics.net/access?context=dispute-data-model&family=xanadu&ft:locale=en-US)**
    -   Enhanced Dispute Rules Content Pack for Visa to support the updated chargeback eligibility conditions and the fields used for validating disputed transactions.
    -   Moved the following tables as generic intake tables, from Dispute Rules Content Pack for Visa \[sn\_bom\_visa\_cp\] to Financial Services Card Operations \[sn\_bom\_credit\_card\]:
        -   Visa Dispute Intake \[sn\_bom\_visa\_cp\_visa\_dispute\_questionnaire\] → Dispute Intake \[sn\_bom\_credit\_card\_dispute\_intake\]
        -   Visa Dispute Cardholder Intake \[sn\_bom\_visa\_cp\_visa\_dispute\_cardholder\_intake\] → Cardholder Dispute Intake \[sn\_bom\_credit\_card\_cardholder\_dispute\_intake\]

**Note:** These tables have been moved only for new customers, but they are still available in the Dispute Rules Content Pack for Visa for existing customers.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.2 updates](https://servicenow-staging.fluidtopics.net/access?context=visa-spoke&family=yokohama&ft:locale=en-US)**

Updated the dispute questionnaire provided through Dispute Rules Content Pack for Visa to align with Visa Resolve Online \(VROL\) release 25.2 revision changes.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.2 updates](https://servicenow-staging.fluidtopics.net/access?context=visa-spoke&family=zurich&ft:locale=en-US)**

Updated the dispute questionnaire provided through the Dispute Rules Content Pack for Visa to align with Visa Resolve Online \(VROL\) release 25.2 revision changes.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Dispute Rules Content Pack for Visa features or functionality were removed.

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

Between your current release family and Zurich, some Dispute Rules Content Pack for Visa features or functionality were deprecated.

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

Review information on how to activate Dispute Rules Content Pack for Visa.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install Dispute Rules Content Pack for Visa by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Dispute Rules Content Pack for Visa by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Dispute Rules Content Pack for Visa by requesting it from ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Dispute Rules Content Pack for Visa we have noted them here.

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
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Dispute Rules Content Pack for Visa we have noted them here.

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

Review details on accessibility information for Dispute Rules Content Pack for Visa, such as specific requirements or compliance levels.

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

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Dispute Rules Content Pack for Visa we have noted them here.

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
</table>## Highlight information

If there are specific highlight considerations for Dispute Rules Content Pack for Visa we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Optimize the chargeback process by identifying eligibility immediately, prior to submitting the dispute to the card payment network.
-   Avoid penalties by identifying ineligible transactions that are based on the reason code and transaction data.

 See [Dispute Rules Content Pack for Visa](https://servicenow-staging.fluidtopics.net/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

Apply Visa Resolve Online \(VROL\) release 25.2 revision changes to Dispute Rules Content Pack for Visa questionnaire.

 See [Dispute Rules Content Pack for Visa](https://servicenow-staging.fluidtopics.net/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

Applied Visa Resolve Online \(VROL\) release 25.2 revision changes to Dispute Rules Content Pack for Visa questionnaire.

 See [Dispute Rules Content Pack for Visa](https://servicenow-staging.fluidtopics.net/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)


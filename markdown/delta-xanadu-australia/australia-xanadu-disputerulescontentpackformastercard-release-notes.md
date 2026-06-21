---
title: Combined Dispute Rules Content Pack for Mastercard release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Dispute Rules Content Pack for Mastercard from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-disputerulescontentpackformastercard-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Dispute Rules Content Pack for Mastercard release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Dispute Rules Content Pack for Mastercard from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Dispute Rules Content Pack for Mastercard release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Dispute Rules Content Pack for Mastercard to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Australia

</td><td>

The Australia release adds 14 new data fields to the Authorization and Financial Transaction tables to support the new eligibility rules. The `transactionAmountLocal` field already exists in the Financial Transaction table but is being extended to the Financial Transaction Authorization table in this release. No other pre-existing fields are affected. After upgrading, confirm that the new fields are available and populated on your instance. For a full list of new fields, see New in this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Dispute Rules Content Pack for Mastercard.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Decision tables](https://www.servicenow.com/docs/access?context=decision-designer-overview&family=xanadu&ft:locale=en-US)**

Streamline dispute processing by validating Mastercard transaction details and questionnaire answers against the eligibility rules in the decision tables that are included in this application.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Decision tables for Mastercard dispute processing](https://www.servicenow.com/docs/access?context=dispute-decision-tables&family=zurich&ft:locale=en-US)**

Streamline dispute processing by validating Mastercard transaction details and questionnaire answers against the eligibility rules in this application's decision tables.

-   **[New data fields for Mastercard chargeback eligibility rules](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

New data fields sourced from the Mastercard authorization API and Mastercard clearing API have been added to support the expanded eligibility rules. Fields sourced from the Mastercard authorization API are available on the Financial Transaction Authorization table. Fields sourced from the Mastercard clearing API are available on the Financial Transaction table.

-   **[New eligibility questionnaire questions](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

New Mastercard-specific questions have been added to the chargeback eligibility questionnaire.

For Authorization disputes \(all RC 4808 sub-categories\): A new mandatory certification statement appears in the dispute information section. It displays after the dispute amount modification reason field. Dispute agents must confirm that authorization was required for the transaction but was not properly obtained before an Authorization chargeback can proceed.

For Consumer Dispute RC 4853 Failed Travel Merchant: Two new questions support the bond or insurance scheme reimbursement requirement:

    -   When a bond or insurance scheme exists, agents are asked what response was received from the bonding authority or insurance scheme when reimbursement was requested.
    -   When no response has been received, agents are asked to provide the date on which the reimbursement request was submitted.

</td></tr><tr><td>

Australia

</td><td>

-   **[New data fields for Mastercard chargeback eligibility rules](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=australia&ft:locale=en-US)**

New data fields sourced from the Mastercard authorization API and Mastercard clearing API have been added to support the expanded eligibility rules. Fields sourced from the Mastercard authorization API are available on the Financial Transaction Authorization table. Fields sourced from the Mastercard clearing API are available on the Financial Transaction table.

-   **[New eligibility questionnaire questions](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=australia&ft:locale=en-US)**

New Mastercard-specific questions have been added to the chargeback eligibility questionnaire.

For Authorization disputes \(all RC 4808 sub-categories\): A new mandatory certification statement appears in the dispute information section. It displays after the dispute amount modification reason field. Dispute agents must confirm that authorization was required for the transaction but was not properly obtained before an Authorization chargeback can proceed.

For Consumer Dispute RC 4853 Failed Travel Merchant: Two new questions support the bond or insurance scheme reimbursement requirement:

    -   When a bond or insurance scheme exists, agents are asked what response was received from the bonding authority or insurance scheme when reimbursement was requested.
    -   When no response has been received, agents are asked to provide the date on which the reimbursement request was submitted.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Dispute Rules Content Pack for Mastercard features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Updated references from questionnaire tables to intake tables in Card Operations](https://www.servicenow.com/docs/access?context=components-installed-with-dispute-rules-content-pack-for-mastercard&family=xanadu&ft:locale=en-US)**

Updated references from the old questionnaire tables to the new intake tables in Card Operations.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Dispute Rules Content Pack for Mastercard chargeback eligibility rules updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

Transformed chargeback eligibility rules into technical formulas to determine the eligibility or ineligibility of a selected transaction for chargeback.

New ineligibility conditions have been added across all five existing RC 4808 Authorization sub-categories:

    -   Required Authorization Not Obtained \(RANO\)
    -   Expired Chargeback Protection Period \(ECPP\)
    -   Stand-in or X-Code Approval after Issuer Decline \(SIXCAID\)
    -   CAT 3 Devices \(CAT3D\)
    -   Transit First Ride Risk Framework Claims \(TFRR\)
Expanded eligibility rules for the following fraud dispute reason codes:

    -   RC 4837 \(No Cardholder Authorization\)
    -   RC 4849 \(Questionable Merchant Activity\)
    -   RC 4870 \(Chip Liability Shift\)
    -   RC 4871 \(Chip Liability Shift – Lost/Stolen/NRI Fraud\)
-   **[Dispute Rules Content Pack for Mastercard intake questionnaire updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

Updated the dispute questionnaire provided through Dispute Rules Content Pack for Mastercard by adding new questions and updating existing questions.Questionnaire questions include RC 4853 Failed Travel Merchant – Intra-EEA and Domestic European Transactions Only as an additional display condition.


</td></tr><tr><td>

Australia

</td><td>

-   **[Dispute Rules Content Pack for Mastercard chargeback eligibility rules updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=australia&ft:locale=en-US)**

Determine the eligibility of a selected transaction for chargeback through chargeback eligibility rules transformed into technical formulas.

New ineligibility conditions have been added across all five existing RC 4808 Authorization sub-categories:

    -   Required Authorization Not Obtained \(RANO\)
    -   Expired Chargeback Protection Period \(ECPP\)
    -   Stand-in or X-Code Approval after Issuer Decline \(SIXCAID\)
    -   CAT 3 Devices \(CAT3D\)
    -   Transit First Ride Risk Framework Claims \(TFRR\)
Expanded eligibility rules for the following fraud dispute reason codes:

    -   RC 4837 \(No Cardholder Authorization\)
    -   RC 4849 \(Questionable Merchant Activity\)
    -   RC 4870 \(Chip Liability Shift\)
    -   RC 4871 \(Chip Liability Shift – Lost/Stolen/NRI Fraud\)
-   **[Dispute Rules Content Pack for Mastercard intake questionnaire updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=australia&ft:locale=en-US)**

Benefit from the dispute questionnaire provided through Dispute Rules Content Pack for Mastercard with some modified questions and added hard stop alerts. Questionnaire questions include RC 4853 Failed Travel Merchant – Intra-EEA and Domestic European Transactions Only as an additional display condition.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Dispute Rules Content Pack for Mastercard features or functionality were removed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Dispute Rules Content Pack for Mastercard features or functionality were deprecated.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Dispute Rules Content Pack for Mastercard.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install Dispute Rules Content Pack for Mastercard by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Install Dispute Rules Content Pack for Mastercard by requesting it from ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Dispute Rules Content Pack for Mastercard by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Dispute Rules Content Pack for Mastercard we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

This application requires Financial Services Card Operations \(sn\_bom\_credit\_card\).

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

This application requires Financial Services Card Operations \(sn\_bom\_credit\_card\) to be installed.

</td></tr><tr><td>

Australia

</td><td>

This application requires Financial Services Card Operations \(sn\_bom\_credit\_card\) to be installed.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Dispute Rules Content Pack for Mastercard we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Dispute Rules Content Pack for Mastercard, such as specific requirements or compliance levels.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Dispute Rules Content Pack for Mastercard we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Dispute Rules Content Pack for Mastercard we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Run chargeback eligibility rules based on Mastercard rules.
-   Determine the chargeback eligibility for Mastercard transactions by using the provided decision tables. The eligibility is based on the reason code, intake responses, and transaction data from the dispute.

 See [Dispute Rules Content Pack for Mastercard](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   Developed and refined chargeback eligibility rules to validate dispute cases against Mastercard core rules.
-   Updated the intake questionnaire for various dispute categories.

 See [Dispute Rules Content Pack for Mastercard](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Verify that dispute cases are compliant with Mastercard core rules through refined chargeback eligibility rules.
-   Streamline dispute intake process through an updated questionnaire.

 See [Dispute Rules Content Pack for Mastercard](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)


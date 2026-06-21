---
title: Combined Dispute Rules Content Pack for Visa release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Dispute Rules Content Pack for Visa from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-disputerulescontentpackforvisa-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Dispute Rules Content Pack for Visa release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Dispute Rules Content Pack for Visa from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Dispute Rules Content Pack for Visa release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Dispute Rules Content Pack for Visa to Australia

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

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Dispute Rules Content Pack for Visa.

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

-   **[Special Condition Indicator field](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=zurich&ft:locale=en-US)**

A new **Special Condition Indicator** field on the Financial Transaction record identifies transactions involving non-fiat currency, non-fungible tokens \(NFTs\), and related digital assets. The chargeback eligibility rules engine uses this field to apply the correct dispute conditions for RC 10.4, RC 13.1, and RC 13.3.

-   **[New dispute intake questions for digital asset transactions](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=zurich&ft:locale=en-US)**

Two new questions have been added to the Visa dispute intake questionnaire to support the updated eligibility rules for non-fiat currency and NFT transactions.

    -   For fraud disputes where the Special Condition Indicator is 2, 3, 4, or 7: ask whether the cardholder claims they were deceived into sending non-fiat currency or an NFT to a fraudulent recipient.
    -   For consumer disputes filed under RC 13.3 \(Not as Described\) involving a non-fiat currency or NFT purchase: ask whether the cardholder has evidence that the merchant guaranteed or promised the asset would increase in value.

</td></tr><tr><td>

Australia

</td><td>

-   **[Special Condition Indicator field](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=australia&ft:locale=en-US)**

A new **Special Condition Indicator** field on the Financial Transaction record identifies transactions involving non-fiat currency, non-fungible tokens \(NFTs\), and related digital assets. The chargeback eligibility rules engine uses this field to apply the correct dispute conditions for RC 10.4, RC 13.1, and RC 13.3.

-   **[New dispute intake questions for digital asset transactions](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=australia&ft:locale=en-US)**

Two new questions have been added to the Visa dispute intake questionnaire to support the updated eligibility rules for non-fiat currency and NFT transactions.

    -   For fraud disputes where the Special Condition Indicator is 2, 3, 4, or 7: ask whether the cardholder claims they were deceived into sending non-fiat currency or an NFT to a fraudulent recipient.
    -   For consumer disputes filed under RC 13.3 \(Not as Described\) involving a non-fiat currency or NFT purchase: ask whether the cardholder has evidence that the merchant guaranteed or promised the asset would increase in value.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Dispute Rules Content Pack for Visa features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Questionnaire and chargeback eligibility ruless](https://www.servicenow.com/docs/access?context=reason-codes-supported-in-dispute-rules-content-pack-for-visa&family=xanadu&ft:locale=en-US)**
    -   Added new chargeback eligibility rules to reflect the latest dispute conditions from Visa.
    -   Updated the dispute questionnaire to support the following reason codes:
        -   10.3 \(Other fraud—card-present environment\)
        -   13.1 \(Merchandise/services not received\)
        -   13.5 \(Misrepresentation\)
-   **[Visa Resolve Online \(VROL\) 24.2 revision Alignment](https://www.servicenow.com/docs/access?context=reason-codes-supported-in-dispute-rules-content-pack-for-visa&family=xanadu&ft:locale=en-US)**
    -   Updated chargeback reason codes and dispute questionnaire with VROL's latest release revision 24.2.
    -   Updated 12.1 chargeback rules to 11.3.
-   **[Visa Resolve Online \(VROL\) 25.2 revision Alignment](https://www.servicenow.com/docs/access?context=reason-codes-supported-in-dispute-rules-content-pack-for-visa&family=xanadu&ft:locale=en-US)**

The chargeback eligibility rule under the 12.6 reason code that validates **Is the other transaction paid by other means? == N** has been removed,

-   **[Updated references in Card Operations tables](https://www.servicenow.com/docs/access?context=components-installed-with-dispute-rules-content-pack-for-visa&family=xanadu&ft:locale=en-US)**

Updated references from the old questionnaire tables to the new intake tables in Card Operations.

-   **[Updated data model](https://www.servicenow.com/docs/access?context=dispute-data-model&family=xanadu&ft:locale=en-US)**
    -   Enhanced Dispute Rules Content Pack for Visa to support the updated chargeback eligibility conditions and the fields used for validating disputed transactions.
    -   Moved the following tables as generic intake tables, from Dispute Rules Content Pack for Visa \[sn\_bom\_visa\_cp\] to Financial Services Card Operations \[sn\_bom\_credit\_card\]:
        -   Visa Dispute Intake \[sn\_bom\_visa\_cp\_visa\_dispute\_questionnaire\] → Dispute Intake \[sn\_bom\_credit\_card\_dispute\_intake\]
        -   Visa Dispute Cardholder Intake \[sn\_bom\_visa\_cp\_visa\_dispute\_cardholder\_intake\] → Cardholder Dispute Intake \[sn\_bom\_credit\_card\_cardholder\_dispute\_intake\]

**Note:** These tables have been moved only for new customers, but they are still available in the Dispute Rules Content Pack for Visa for existing customers.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.2 updates](https://www.servicenow.com/docs/access?context=visa-spoke&family=yokohama&ft:locale=en-US)**

Updated the dispute questionnaire provided through Dispute Rules Content Pack for Visa to align with Visa Resolve Online \(VROL\) release 25.2 revision changes.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Visa Resolve Online \(VROL\) version 26.1 updates](https://www.servicenow.com/docs/access?context=visa-spoke&family=zurich&ft:locale=en-US)**

Updated the dispute questionnaire provided through the Dispute Rules Content Pack for Visa to align with Visa Resolve Online \(VROL\) release 26.1 revision changes.

-   **[Updated chargeback eligibility rules for Visa reason codes 10.1, 10.2, 10.3, 10.4, 13.1, 13.2, 13.3, and 13.4](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=zurich&ft:locale=en-US)**

The chargeback eligibility rules for eight Visa reason codes have been updated to reflect Visa Chargeback Guide v1.1. The rules engine evaluates disputes automatically against the updated criteria; no manual configuration is required. Disputes that do not meet the updated eligibility criteria are flagged as ineligible before submission.

-   **[Updated dispute intake questionnaire for fraud disputes involving non-fiat currency and NFTs](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=zurich&ft:locale=en-US)**

The fraud dispute intake questionnaire now includes a conditional question for disputes involving non-fiat currency or NFT transactions, such as cryptocurrency and digital token purchases. When the transaction is identified as a digital asset purchase, dispute agents and cardholders are asked to confirm whether the cardholder claims they were deceived into sending the asset to a fraudulent recipient. The question is shown only when relevant and is cleared automatically when it does not apply. This supports accurate eligibility evaluation without requiring agents to manually identify digital asset transaction types.

-   **[Updated dispute intake questionnaire for RC 13.3 \(Not as Described\) disputes involving non-fiat currency and NFTs](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=zurich&ft:locale=en-US)**

The consumer dispute intake questionnaire for RC 13.3 now includes an additional question for disputes involving non-fiat currency or NFT purchases. After confirming whether the asset received matched the description at the time of purchase, dispute agents and cardholders are asked whether there is evidence that the merchant guaranteed or promised the asset would increase in value. This question determines whether a specific dispute right applies, and appears only after the preceding NFT description question is answered.


</td></tr><tr><td>

Australia

</td><td>

-   **[Updated questions for the dispute questionnaire](https://www.servicenow.com/docs/access?context=exploring-the-dispute-rules-content-pack-for-visa&family=australia&ft:locale=en-US)**

Added four new agent-facing questions to the dispute questionnaire under the authorization \(11\) and consumer disputes \(13\) categories. These questions map to the following reason codes:

    -   11.1 - Card recovery bulletin or exception file
    -   11.2 - Declined authorization
    -   11.3 - No authorization or late presentment
    -   13.6 - Credit not processed
    -   13.7 - Cancelled merchandise or services
-   **[Visa Resolve Online \(VROL\) version 26.1 updates](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=australia&ft:locale=en-US)**

Updated the dispute questionnaire provided through the Dispute Rules Content Pack for Visa to align with Visa Resolve Online \(VROL\) release 26.1 revision changes.

-   **[Updated chargeback eligibility rules for Visa reason codes 10.1, 10.2, 10.3, 10.4, 13.1, 13.2, 13.3, and 13.4](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=australia&ft:locale=en-US)**

The chargeback eligibility rules for eight Visa reason codes have been updated to reflect Visa Chargeback Guide v1.1. The rules engine evaluates disputes automatically against the updated criteria; no manual configuration is required. Disputes that do not meet the updated eligibility criteria are flagged as ineligible before submission.

-   **[Updated dispute intake questionnaire for fraud disputes involving non-fiat currency and NFTs](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=australia&ft:locale=en-US)**

The fraud dispute intake questionnaire now includes a conditional question for disputes involving non-fiat currency or NFT transactions, such as cryptocurrency and digital token purchases. When the transaction is identified as a digital asset purchase, dispute agents and cardholders are asked to confirm whether the cardholder claims they were deceived into sending the asset to a fraudulent recipient. The question is shown only when relevant and is cleared automatically when it does not apply. This supports accurate eligibility evaluation without requiring agents to manually identify digital asset transaction types.

-   **[Updated dispute intake questionnaire for RC 13.3 \(Not as Described\) disputes involving non-fiat currency and NFTs](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=australia&ft:locale=en-US)**

The consumer dispute intake questionnaire for RC 13.3 now includes an additional question for disputes involving non-fiat currency or NFT purchases. After confirming whether the asset received matched the description at the time of purchase, dispute agents and cardholders are asked whether there is evidence that the merchant guaranteed or promised the asset would increase in value. This question determines whether a specific dispute right applies, and appears only after the preceding NFT description question is answered.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Dispute Rules Content Pack for Visa features or functionality were removed.

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

Between your current release family and Australia, some Dispute Rules Content Pack for Visa features or functionality were deprecated.

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

Review information on how to activate Dispute Rules Content Pack for Visa.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install Dispute Rules Content Pack for Visa by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Dispute Rules Content Pack for Visa by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Dispute Rules Content Pack for Visa by requesting it from ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Dispute Rules Content Pack for Visa by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

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

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

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

</td></tr><tr><td>

Australia

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

 See [Dispute Rules Content Pack for Visa](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

Apply Visa Resolve Online \(VROL\) release 25.2 revision changes to Dispute Rules Content Pack for Visa questionnaire.

 See [Dispute Rules Content Pack for Visa](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

Applied Visa Resolve Online \(VROL\) release 26.1 revision changes to Dispute Rules Content Pack for Visa questionnaireand updated chargeback rules based on the Visa Chargeback Guide v1.1.

 See [Dispute Rules Content Pack for Visa](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

Applied Visa Resolve Online \(VROL\) release 26.1 revision changes to the Dispute Rules Content Pack for Visa questionnaireand updated chargeback rules based on the Visa Chargeback Guide v1.1.

 See [Dispute Rules Content Pack for Visa](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-visa-landing-page-1&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)


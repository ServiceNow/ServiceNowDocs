---
title: Combined Financial Services Operations Integration with Visa release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for Financial Services Operations Integration with Visa from Washington DC to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-financialservicesoperationsintegrationwithvisa-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Financial Services Operations Integration with Visa release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for Financial Services Operations Integration with Visa from Washington DC to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Financial Services Operations Integration with Visa release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Financial Services Operations Integration with Visa to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Financial Services Operations Integration with Visa.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Create a dispute case in the VROL system](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&family=washingtondc&ft:locale=en-US)**

Execute the Create Case From Transaction subflow to generate a dispute case in the Visa Resolve Online \(VROL\) system.

-   **[Initiate a dispute case from Transaction Inquiry \(TI\) or an existing case](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&family=washingtondc&ft:locale=en-US)**

Execute the Initiate Dispute from Transaction or Case subflow to start creating a dispute case in the VROL system, either from a Transaction Inquiry \(TI\) or an existing case.

-   **[Allow VROL users to Submit or Save Dispute Questionnaires](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&family=washingtondc&ft:locale=en-US)**

Execute the Submit Dispute Questionnaire subflow to submit or save dispute questionnaires for specific disputes in the VROL system.

-   **[Retrieve associated transaction list](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&family=washingtondc&ft:locale=en-US)**

Execute the Look up Associated Transactions subflow to retrieve the related transactions associated with the disputed transaction.

-   **[Select associated transactions](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&family=washingtondc&ft:locale=en-US)**

Use the Select Associated Transactions subflow to associate the disputed transaction with the retrieved related transactions.

-   **[Change dispute status](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&family=washingtondc&ft:locale=en-US)**

Utilize the Change Dispute Status subflow to modify the status of a dispute.

-   **[Submit transaction inquiry](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&family=washingtondc&ft:locale=en-US)**

Use the Submit Transaction Inquiry subflow, which allows users to search for transactions using specific criteria. This subflow contains sensitive information in the request and response body. To ensure seamless integration, users must have a tokenization solution.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Updated subflows for Visa Resolve Online \(VROL\) 24.2 revision](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&family=xanadu&ft:locale=en-US)**

Updated the following subflows to support the changes in the Visa Resolve Online \(VROL\) \(VROL\) release 24.2 revision:

    -   Look up Case Details
    -   Submit Fraud Report
    -   Update Case Resolution Status

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Added new VROL integration subflows](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&family=yokohama&ft:locale=en-US)**

Enables seamless integration with the card operations dispute management playbook with VROL subflows. The following new VROL subflows have been added:

    -   Look Up Transaction Inquiry Results
    -   Accept Dispute
    -   Conduct Cardholder Purchase Inquiry
    -   Look Up Transaction Details
    -   Look Up Dispute Response Details
    -   Create Dispute Pre-Arbitration
    -   Look Up Dispute Pre-Arbitration Details
    -   Create Dispute Pre-Arbitration Response
    -   Look Up Dispute Pre-Arbitration Response Details
    -   Submit Dispute Filing
    -   Look Up Dispute Filing Details
    -   Mark Batch Queue Item as Read

</td></tr><tr><td>

Zurich

</td><td>

-   **[Enable cardholder purchase inquiry property](https://www.servicenow.com/docs/access?context=properties-installed-with-fso-integration-with-visa&family=zurich&ft:locale=en-US)**

Enables or disables integration with the Cardholder Purchase Inquiry API in the Visa card dispute playbook.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Financial Services Operations Integration with Visa features.

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

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://www.servicenow.com/docs/access?context=visa-spoke&family=xanadu&ft:locale=en-US)**

Updated the following subflows to align with Visa Resolve Online \(VROL\) release 25.1 revision changes:

    -   Submit dispute questionnaire
    -   Submit fraud report

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&family=yokohama&ft:locale=en-US)**

Updated the following subflows to align with release 25.1 revision changes:

    -   Submit Dispute questionnaire
    -   Submit fraud report

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **[Updated subflows](https://www.servicenow.com/docs/access?context=components-installed-with-the-financial-services-operations-integration-with-visa&family=australia&ft:locale=en-US)**

The following subflows have been updated to support integration with the Card data security application:

    -   Look up Associated Transactions
    -   Look up Dispute Pre Arbitration Details
    -   Look up Dispute Filing Details
    -   Look up Dispute Response Details
    -   Look up Dispute Pre Arbitration Response Details

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Financial Services Operations Integration with Visa features or functionality were removed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Financial Services Operations Integration with Visa features or functionality were deprecated.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Financial Services Operations Integration with Visa.

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

Install Now Assist for FSO by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Install Financial Services Operations Integration with Visa by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Financial Services Operations Integration with Visa by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Financial Services Operations Integration with Visa we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Financial Services Operations Integration with Visa we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Financial Services Operations Integration with Visa, such as specific requirements or compliance levels.

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

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Financial Services Operations Integration with Visa we have noted them here.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Financial Services Operations Integration with Visa we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Leverage the integration layer with subflows to seamlessly use the Visa spokes.
-   Minimize the workload for dispute agents and enhance overall efficiency.
-   Effectively manage the entire card dispute process from beginning to end.

 See [Financial Services Operations Integration with Visa](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-visa-landing-page&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Handle various dispute lifecycle events including transaction searches, dispute case creation, questionnaire submissions, fraud reporting, and more.
-   Utilize data model elements to capture and store information used in subflows for seamless integration.

 See [Financial Services Operations Integration with Visa](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-visa-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Enables Visa VROL dispute resolution process by providing features such as accept dispute and cardholder purchase enquiry.
-   Ensures Visa conformance through error handling and timely updates on chargeback status.

 See [Integrating with Visa](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-visa-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

ِEnable system administrators to control settings for features in the Financial Services Operations Integration with Visa application, such as, integration with specific APIs.

 See [Visa](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-visa-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

Use updated subflows to help prevent storage or transmission of Payment Card Industry \(PCI\) data for card disputes within your ServiceNow instance.

 See [Visa](https://www.servicenow.com/docs/access?context=financial-services-operations-integration-with-visa-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)


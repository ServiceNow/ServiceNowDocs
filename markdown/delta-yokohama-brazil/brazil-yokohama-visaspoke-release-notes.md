---
title: Combined Visa Spoke release notes for upgrades from Yokohama to Brazil
description: Consolidated page of all release notes for Visa Spoke from Yokohama to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-brazil/brazil-yokohama-visaspoke-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 11
breadcrumb: [Products combined by family]
---

# Combined Visa Spoke release notes for upgrades from Yokohama to Brazil

Consolidated page of all release notes for Visa Spoke from Yokohama to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Visa Spoke release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Visa Spoke to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Visa Spoke.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Visa Stop Payment Service \(VSPS\) integration](https://www.servicenow.com/docs/access?context=visa-spoke&family=yokohama&ft:locale=en-US)**

The Visa Stop Payment Service \(VSPS\) enables Visa card issuers to stop card-on-file payments \(including recurring and installment payments\) from being authorized, cleared, and settled through VisaNet. This service helps Visa issuers handle cardholder stop payment requests.

The following Visa Spoke actions allow clients to integrate with VSPS APIs and work through the platform:

    -   Create Stop Payment Instruction by Merchant Identifier Request Builder​
    -   Create Stop Payment Instruction by Merchant Identifier Response Parser​
    -   Create Stop Payment Instruction by PAN Request Builder​
    -   Create Stop Payment Instruction by PAN Response Parser​
    -   Create Stop Payment Instructions by Merchant Category Code Request Builder​
    -   Create Stop Payment Instructions by Merchant Category Code Response Parser​
    -   Look up Eligible Transactions for Stop Payment by PAN and Date Range Request Builder​
    -   Look up Eligible Transactions for Stop Payment by PAN and Date Range Response Parser
    -   Look up Stop Instruction Details by Stop Instruction ID Request Builder​
    -   Look up Stop Instruction Details by Stop Instruction ID Response Parser​
    -   Look up Stop Payment Instructions by PAN Request Builder​
    -   Look up Stop Payment Instructions by PAN Response Parser​
    -   Update Stop Instructions Duration by Stop Instruction ID Request Builder​
    -   Update Stop Instructions Duration by Stop Instruction ID Response Parser​
    -   Update Stop Payment Instruction by Merchant Identifier Request Builder​
    -   Update Stop Payment Instruction by Merchant Identifier Response Parser​
    -   Update Stop Payment Instruction by Merchant Category Code Request Builder​
    -   Update Stop Payment Instruction by Merchant Category Code Response Parser​
    -   Look up all linked stop payment instructions by stop instruction id Request Builder​
    -   Look up all linked stop payment instructions by stop instruction id Response Parser
    -   Look up stopped transactions by PAN Request Builder​
    -   Look up stopped transactions by PAN Response Parser​
    -   Look up stopped transactions by stop Instruction id Request Builder​
    -   Look up stopped transactions by stop Instruction id Response Parser
    -   Cancel Multiple Stop Instructions Request Builder​
    -   Cancel Multiple Stop Instructions Response Parser​

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Virtual account and funding account fields**

These spoke actions now return the Virtual Account Number \(VAN\), Virtual Card Code \(with description\), and the underlying Funding Account Number \(FAN\) when a dispute or transaction involves a virtual card.

    -   `Look up Dispute Financial Details Response Parser`
    -   `Look up Transaction Details Response Parser`
    -   `Look up Transaction Details from Case Response Parser`
    -   `Look up All Transaction Details Response Parser`
Separately, on the request side, `Submit Transaction Inquiry Request Builder`'s Card/Account Number field now also accepts a Funding Account Number as search input.

-   **3-D Secure and Compelling Evidence \(CE\) 3.0 transaction detail fields**

These spoke actions now return Digital Authentication Indicator, Authentication Solution Indicator, VCDI device ID and IP address, and merchant-supplied device ID, device IP address, customer account/login ID, shipping address, order ID, foreign retailer indicator, and token requestor TSP ID, supporting liability-shift determinations under Visa's Compelling Evidence 3.0 framework.

    -   `Look up Transaction Details Response Parser`
    -   `Look up Transaction Details from Case Response Parser`
    -   `Look up All Transaction Details Response Parser`
Separately, these same three actions' Service Processing Type field \(the underlying Deferred OCT request type\) gained a new domain value for mobile back-to-back processing.

-   **CE indicator on queue responses**

These spoke actions now include a CE Indicator field, populated only when an acquirer receives an incoming CE 3.0 dispute-rejected case.

    -   `Look up Queue Response Parser`
    -   `Look up Batch Queue Response Parser`
-   **Spoke support for hotel dispute, facilities-withdrawal, and CE transaction detail questionnaire fields**

These spoke actions now submit and return three new dispute intake fields: the date facilities were withdrawn \(Cancelled Recurring Transaction disputes in Europe\), the date a cardholder checked out from a hotel \(Not as Described or Quality disputes involving hotel or lodging merchants\), and CE Transaction Details, a read-back field showing the original and matching historical transactions used in a compelling-evidence determination. The dispute agent and cardholder question wording and display conditions for these fields are documented in the Financial Services Card Operations release notes; this entry covers the underlying spoke-level transport.

    -   `Submit Dispute Questionnaire`
    -   `Look up Dispute Details Response Parser`

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Visa Spoke features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.2 updates](https://www.servicenow.com/docs/access?context=visa-spoke&family=yokohama&ft:locale=en-US)**

Updated the following Visa Spoke actions to align with Visa Resolve Online \(VROL\) release 25.2 revision changes:

    -   Submit Dispute Questionnaire
    -   Hypersearch Request Builder
    -   Hypersearch Response Parser
    -   Create Dispute Pre-Arbitration Request Builder
    -   Create Dispute Pre-Arbitration Response Parser
    -   Look up Dispute Response Details Request Builder
    -   Look up Dispute Response Details Response Parser
    -   Look up Dispute Pre-Arbitration Response Details Request Builder
    -   Look up Dispute Pre-Arbitration Response Details Response Parser
    -   Look up Dispute Pre-Arbitration Details Request Builder
    -   Look up Dispute Pre-Arbitration Details Response Parser
    -   Look up Dispute Details Request Builder
    -   Look up Dispute Details Response Parser

 -   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://www.servicenow.com/docs/access?context=visa-spoke&family=yokohama&ft:locale=en-US)**

Updated the following Visa Spoke actions to align with Visa Resolve Online \(VROL\) release 25.1 revision changes:

    -   Submit Fraud Report Request Builder
    -   Look up Fraud Report Details Response Parser
    -   Look up Dispute Response Details Response Parser
    -   Look up Dispute Details Response Parser
    -   Submit Dispute Questionnaire

</td></tr><tr><td>

Zurich

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


 -   **[Visa Resolve Online \(VROL\) version 25.2 updates](https://www.servicenow.com/docs/access?context=visa-spoke&family=zurich&ft:locale=en-US)**

Updated the following Visa Spoke actions to align with Visa Resolve Online \(VROL\) release 25.2 revision changes:

    -   Submit Dispute Questionnaire
    -   Hypersearch Request Builder
    -   Hypersearch Response Parser
    -   Create Dispute Pre-Arbitration Request Builder
    -   Create Dispute Pre-Arbitration Response Parser
    -   Look up Dispute Response Details Request Builder
    -   Look up Dispute Response Details Response Parser
    -   Look up Dispute Pre-Arbitration Response Details Request Builder
    -   Look up Dispute Pre-Arbitration Response Details Response Parser
    -   Look up Dispute Pre-Arbitration Details Request Builder
    -   Look up Dispute Pre-Arbitration Details Response Parser
    -   Look up Dispute Details Request Builder
    -   Look up Dispute Details Response Parser

</td></tr><tr><td>

Australia

</td><td>

-   **[Card data security updates](https://www.servicenow.com/docs/access?context=visa-spoke&family=australia&ft:locale=en-US)**

The following spoke actions have been updated to support integration with the Card data security application:

    -   Look up Associated Transaction List
    -   Look up Image
    -   Look up Report Output
    -   Download and Attach Image
-   **[VROL release 26.1 updates](https://www.servicenow.com/docs/access?context=visa-spoke&family=australia&ft:locale=en-US)**

Updated the following Visa Spoke actions to align with VROL release 26.1 revision changes. These changes support dispute agents and admins in processing disputes accurately:

    -   Submit Exception Request Builder
    -   Submit Fraud Bundle Dispute Questionnaire
    -   Look up Dispute Financial Details Request Builder
    -   Look up Dispute Financial Details Response Parser
    -   Submit Fraud Report Request Builder
    -   Look up Fraud Report Details Response Parser
    -   Look up Fraud Report Details Request Builder
    -   Look up Transaction Details Request Builder
    -   Look up Dispute Details Request Builder
    -   Look up Dispute Details Response Parser
    -   Look up Dispute Filing Details Response Parser
    -   Look up Transaction Details Response Parser
    -   Look up Transaction Details from Case Response Parser
    -   Look up All Transaction Details Response Parser
    -   Create Dispute Pre Arbitration Response
    -   Look up Dispute Pre Arbitration Details Request Builder
    -   Look up Dispute Pre Arbitration Response Details Request Builder
    -   Look up Dispute Pre Arbitration Details Response Parser
    -   Look up Dispute Response Details Request Builder
    -   Submit Dispute Questionnaire
    -   Look up Dispute Pre Arbitration Response Details Response Parser
    -   Look up Dispute Response Details Response Parser
    -       -   Initiate Dispute from Transaction or Case
    -   Create Dispute Pre Arbitration

</td></tr><tr><td>

Brazil

</td><td>

-   **Updated response field mapping for dispute response details**

Updated response field mapping for the following spoke actions so FSO can parse and surface the additional fields Visa introduced under the Reference Doc Summary tab's flexible schema for revision 26.2, including document-type, billing- and shipping-address, and travel-itinerary \(outbound/inbound passenger name and departure/arrival date\) fields for compelling-evidence documentation.

    -   `Look up Dispute Response Details Response Parser`
    -   `Look up Dispute Pre Arbitration Details Response Parser`
    -   `Look up Dispute Pre Arbitration Response Details Response Parser`
-   **Updated case, collaboration, and related Spoke actions**

Updated the following spoke actions for IES corrections:

    -   `Look up GMFP Details Response Parser` to correct the case stage/state description field length \(widened to String \(100\)\)
Also updated `Look up Dispute Financial Details Response Parser` to return the Virtual Account Number, Virtual Card Code, and Funding Account Number fields.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Visa Spoke features or functionality were removed.

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Visa Spoke features or functionality were deprecated.

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

</td></tr><tr><td>

Brazil

</td><td>

-   **Authentication Program field**

The Authentication Program field is removed from these spoke actions, per Visa IES 26.2. There is no replacement for this field.

    -   `Look up Transaction Details Response Parser`
    -   `Look up Transaction Details from Case Response Parser`
    -   `Look up All Transaction Details Response Parser`

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Visa Spoke.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Activation information**

Install Visa Spoke by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


**Important:** Visa Spoke is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Visa Spoke by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


**Important:** Visa Spoke is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Visa Spoke by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Visa Spoke is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Visa Spoke we have noted them here.

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Visa Spoke we have noted them here.

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Visa Spoke, such as specific requirements or compliance levels.

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Visa Spoke we have noted them here.

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Visa Spoke we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Manage card disputes with Visa Resolve Online \(VROL\) and card-on-file payments with the Visa Stop Payment Service \(VSPS\) API suite using Visa Spoke.
-   Accept and close dispute items in a queue with Visa Spoke actions.
-   Download images from an endpoint using Visa Spoke actions.
-   Handle card operations and dispute resolution services with Visa Spoke actions.

 See [Visa Spoke](https://www.servicenow.com/docs/access?context=visa-spoke&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

Apply Visa Resolve Online \(VROL\) release 25.2 revision changes to some Visa Spoke actions.

 See [Visa Spoke](https://www.servicenow.com/docs/access?context=visa-spoke&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Use updated Visa Spoke APIs to help prevent storage or transmission of Payment Card Industry \(PCI\) data within ServiceNow.
-   Apply Visa Resolve Online \(VROL\) release 26.1 revision changes to some Visa Spoke actions.

 See [Visa Spoke](https://www.servicenow.com/docs/access?context=visa-spoke&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-yokohama-brazil/rn-combined-intro.md)


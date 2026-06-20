---
title: Combined Financial Services Card Operations release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Financial Services Card Operations from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-financialservicescardoperations-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Financial Services Card Operations release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Financial Services Card Operations from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Financial Services Card Operations release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Financial Services Card Operations to Zurich

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

During the upgrade to Yokohama, the Financial Services Card Operations plugin reparents the Card Disputes Transaction table \[sn\_bom\_credit\_card\_disputes\_transaction\] to the Financial Task table \[sn\_bom\_task\] in Financial Services Operations Core.

 Reparenting leverages the benefits and advancements of ServiceNow® Financial Services Operations Core while preserving the functionality of existing applications.

**Note:** If your instance uses the Card Disputes Transaction table \[sn\_bom\_credit\_card\_disputes\_transaction\] and it contains a large amount of data, you may experience increased upgrade times.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Financial Services Card Operations.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Playbook enhancements for dispute](https://servicenow-staging.fluidtopics.net/access?context=dispute-playbook-for-portal&family=xanadu&ft:locale=en-US)**

These enhancements enable the cardholders to do the following:

    -   Initiate disputes directly through the portal by selecting your financial account and the transactions that you want to dispute.
    -   Simplify the process of initiating and tracking disputes with the user-friendly dispute portal interface.
    -   Collect detailed information about the dispute through a questionnaire on the portal.
    -   Enable cardholders to attach relevant documents to their dispute cases.
    -   Receive real-time updates on your case through the dispute tracker on the portal.
    -   Submit the dispute through the portal to land on a review page, where the agent can review and modify the details for the case as required before submitting it for investigation.
-   **[Card disputes enhancements](https://servicenow-staging.fluidtopics.net/access?context=dispute-management&family=xanadu&ft:locale=en-US)**
    -   Added a common dispute questionnaire table with questions relevant to various card networks for both agents and cardholders.
    -   Moved the reason code field to the card dispute transaction table.
    -   Updated the logic to determine the reason code from the case to the card dispute transaction table.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Detect friendly fraud](https://servicenow-staging.fluidtopics.net/access?context=resolve-friendly-fraud&family=yokohama&ft:locale=en-US)**

Resolve friendly fraud disputes with predefined rules to ensure consistent and precise detection of friendly fraud in Visa disputed transactions. Agents can decline requests, issue credits, or proceed with chargebacks, allowing for tailored responses based on the situation.

-   **[Enhanced Visa disputes playbook](https://servicenow-staging.fluidtopics.net/access?context=managing-card-disputes&family=yokohama&ft:locale=en-US)**

Leverage an updated card disputes processing flow to associate additional transactions, manage multiple transaction disputes, and handle pre-arbitration, arbitration, and appeal requests to Visa for allocation and collaboration chargeback workflows.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Workflow](https://servicenow-staging.fluidtopics.net/access?context=dispute-management-workflows&family=zurich&ft:locale=en-US)**

Resolve Mastercard disputes quickly with an enhanced end-to-end workspace that supports all stages of the dispute life cycle, including pre-arbitration and arbitration. Use comprehensive tools to simplify and accelerate the dispute management process.

-   **[ACH disputes workflow](https://servicenow-staging.fluidtopics.net/access?context=work-dispute-ach&family=zurich&ft:locale=en-US)**

Resolve ACH disputes faster with a guided, end-to-end workflow that unifies intake, investigation, and resolution—built on a framework ready for any non-card transaction. The unified intake now features a new dispute reason framework for accurate regulatory mapping and embedded WSUD signature collection for seamless authorization capture. The overall workflow centralizes data, applies real-time regulatory checks, and surfaces next best actions to reduce manual effort and speed decisioning, all on a modular design that can scale to additional non-card dispute types.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Financial Services Card Operations features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Updated data model](https://servicenow-staging.fluidtopics.net/access?context=installed-with-card-operations&family=xanadu&ft:locale=en-US)**

Introduced the following two new tables for questionnaire intake:

    -   Dispute Intake \[sn\_bom\_credit\_card\_dispute\_intake\]
    -   Cardholder Dispute Intake \[sn\_bom\_credit\_card\_cardholder\_dispute\_intake\]

-   **[Updated Card disputes transaction table](https://servicenow-staging.fluidtopics.net/access?context=installed-with-card-operations&family=xanadu&ft:locale=en-US)**

Removed the following fields from the Card disputes case table:

    -   Account status as of transaction date
    -   Dispute amount modification reason
    -   Reason code
    -   Reason code message
    -   Suggested reason code

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://servicenow-staging.fluidtopics.net/access?context=card-operations-reference&family=xanadu&ft:locale=en-US)**

The domain value description for the **DisputeResponseReason** column has been updated from **Copy of ATM Cash Disbursement or Load Transaction** to **Copy of ATM Cash Disbursement**.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://servicenow-staging.fluidtopics.net/access?context=card-operations-reference&family=yokohama&ft:locale=en-US)**

Updated the following columns to align with release 25.1 revision changes:

    -   The **is\_parcelado** column has been removed from the dispute intake table.
    -   The domain value description for the **DisputeResponseReason** column has been updated from **Copy of ATM Cash Disbursement or Load Transaction** to **Copy of ATM Cash Disbursement**.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Workflow](https://servicenow-staging.fluidtopics.net/access?context=dispute-management-workflows&family=zurich&ft:locale=en-US)**

Track the progress of the investigation workflow intuitively with a redesigned user interface that presents each transaction within a dispute case using a clear, process-based layout. This new layout visualizes the distinct stages of the investigation workflow, Investigate, Chargeback, and Closure, which enhances visibility and dispute management efficiency.


-   **[Resolving disputes with Mastercard](https://servicenow-staging.fluidtopics.net/access?context=work-on-disputes-integrated-with-mc&family=zurich&ft:locale=en-US)**

Integrate the Dispute Management workflow with subflows that communicate with Mastercom, supporting an end-to-end dispute life-cycle from raising an initial dispute to final resolution.

-   **[Unified dispute intake experience](https://servicenow-staging.fluidtopics.net/access?context=dispute-intake-overview&family=zurich&ft:locale=en-US)**

The dispute intake process has been streamlined to provide a clear, intuitive experience for customers and dispute agents, resulting in faster resolution and reduced manual effort. A unified interface now allows cardholders, account holders, and agents to raise disputes for both card and non-card \(ACH\) transactions seamlessly.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Financial Services Card Operations features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Moved the reason code for Late Presentment from the processing error decision question to the authorization category.
-   Updated the 12.1 chargeback rules to 11.3, aligning with VROL’s latest release revision 24.2.
-   Removed the **is\_parcelado** column from the dispute intake table, in alignment with VROL’s latest release revision 24.2.

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

Between your current release family and Zurich, some Financial Services Card Operations features or functionality were deprecated.

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

Review information on how to activate Financial Services Card Operations.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install Financial Services Card Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Financial Services Card Operations by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Financial Services Card Operations we have noted them here.

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

If any specific browser requirements were introduced or changed for Financial Services Card Operations we have noted them here.

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

Review details on accessibility information for Financial Services Card Operations, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Financial Services Card Operations we have noted them here.

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

If there are specific highlight considerations for Financial Services Card Operations we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Enable cardholders to create and track disputes with a dispute playbook experience on the portal.
-   Enhance navigation with intuitive transitions between different role-based landing pages.
-   Permit scoped admins to modify landing pages with extensive capabilities, confirming that content aligns with the specific needs and preferences of their user base.

 See [Financial Services Card Operations](https://servicenow-staging.fluidtopics.net/access?context=card-ops-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Resolve friendly fraud disputes by incorporating friendly fraud detection and resolution in the existing dispute flow for Visa transactions. You can take actions such as crediting the customer, denying the dispute, or initiating an exception process.
-   The Financial Services Card Operations data model is updated in this release with reparented tables to align the data and manage the dispute transactions more effectively. See [Card Operations](https://servicenow-staging.fluidtopics.net/access?context=card-ops-landing-page&family=yokohama&ft:locale=en-US) for more information.
-   Enhance the card disputes process with an updated end-to-end Visa disputes playbook that now includes support for reviewing associated transactions and handling pre-arbitration, arbitration, and appeals.
-   Manage and work on multiple disputed transactions for a case with individual playbooks for each disputed transaction.
-   Integrate new VROL subflows into the enhanced Visa card disputes playbook.

</td></tr><tr><td>

Zurich

</td><td>

-   Resolve disputes with a new dispute life cycle for Mastercard dispute transactions.
-   Leverage a new workspace page in Financial Services Card Operations to resolve Mastercard disputes.
-   Integrate Mastercard's Mastercom APIs into the Dispute Management workflow to resolve card disputes faster and more efficiently.
-   Resolve ACH disputes faster with a guided, end-to-end workflow that unifies intake, investigation, and resolution—built on a framework ready for any non-card transaction.
-   Streamline operations with a single, consistent intake process that applies across all dispute workflows.

 See [Workflow](https://servicenow-staging.fluidtopics.net/access?context=dispute-management-workflows&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)


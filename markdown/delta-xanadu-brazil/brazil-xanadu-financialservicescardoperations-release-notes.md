---
title: Combined Financial Services Card Operations release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Financial Services Card Operations from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-financialservicescardoperations-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Financial Services Card Operations release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Financial Services Card Operations from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Financial Services Card Operations release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Financial Services Card Operations to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

-   **Upgrade information**

During the upgrade to Yokohama, the Financial Services Card Operations plugin reparents the Card Disputes Transaction table \[sn\_bom\_credit\_card\_disputes\_transaction\] to the Financial Task table \[sn\_bom\_task\] in Financial Services Operations Core.

Reparenting leverages the benefits and advancements of ServiceNow® Financial Services Operations Core while preserving the functionality of existing applications.

**Note:** If your instance uses the Card Disputes Transaction table \[sn\_bom\_credit\_card\_disputes\_transaction\] and it contains a large amount of data, you may experience increased upgrade times.


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

Between your current release family and Brazil, new features were introduced for Financial Services Card Operations.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Playbook enhancements for dispute](https://www.servicenow.com/docs/access?context=dispute-playbook-for-portal&family=xanadu&ft:locale=en-US)**

These enhancements enable the cardholders to do the following:

    -   Initiate disputes directly through the portal by selecting your financial account and the transactions that you want to dispute.
    -   Simplify the process of initiating and tracking disputes with the user-friendly dispute portal interface.
    -   Collect detailed information about the dispute through a questionnaire on the portal.
    -   Enable cardholders to attach relevant documents to their dispute cases.
    -   Receive real-time updates on your case through the dispute tracker on the portal.
    -   Submit the dispute through the portal to land on a review page, where the agent can review and modify the details for the case as required before submitting it for investigation.
-   **[Card disputes enhancements](https://www.servicenow.com/docs/access?context=dispute-management&family=xanadu&ft:locale=en-US)**
    -   Added a common dispute questionnaire table with questions relevant to various card networks for both agents and cardholders.
    -   Moved the reason code field to the card dispute transaction table.
    -   Updated the logic to determine the reason code from the case to the card dispute transaction table.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Enhanced Visa disputes playbook](https://www.servicenow.com/docs/access?context=managing-card-disputes&family=yokohama&ft:locale=en-US)**

Leverage an updated card disputes processing flow to associate additional transactions, manage multiple transaction disputes, and handle pre-arbitration, arbitration, and appeal requests to Visa for allocation and collaboration chargeback workflows.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Workflow](https://www.servicenow.com/docs/access?context=dispute-management-workflows&family=zurich&ft:locale=en-US)**

Resolve Mastercard disputes quickly with an enhanced end-to-end workspace that supports all stages of the dispute life cycle, including pre-arbitration and arbitration. Use comprehensive tools to simplify and accelerate the dispute management process.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Date facilities were withdrawn**

Dispute agents and cardholders can now record the date facilities were withdrawn by answering the question "Date of the facilities were withdrawn." This question displays only after answering Yes to "Certification that the facilities were withdrawn," and supports chargeback eligibility evaluation for reason code 13.2 \(Cancelled Recurring Transaction\).

-   **Date cardholder checked out from hotel**

Dispute agents and cardholders can now record the date a cardholder checked out from a hotel by answering the question "Date cardholder checked out from hotel." This question displays only for disputes filed as Not as Described \(reason code 13.3\) or for a services dispute, where the merchant is categorized under a hotel or lodging merchant category code \(MCC 7011, or the 3501-3856 hotel-chain range\).

-   **CE Transaction Details**

View compelling-evidence transaction details as a read-back field when reviewing Visa dispute details.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Financial Services Card Operations features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Updated data model](https://www.servicenow.com/docs/access?context=installed-with-card-operations&family=xanadu&ft:locale=en-US)**

Introduced the following two new tables for questionnaire intake:

    -   Dispute Intake \[sn\_bom\_credit\_card\_dispute\_intake\]
    -   Cardholder Dispute Intake \[sn\_bom\_credit\_card\_cardholder\_dispute\_intake\]

-   **[Updated Card disputes transaction table](https://www.servicenow.com/docs/access?context=installed-with-card-operations&family=xanadu&ft:locale=en-US)**

Removed the following fields from the Card disputes case table:

    -   Account status as of transaction date
    -   Dispute amount modification reason
    -   Reason code
    -   Reason code message
    -   Suggested reason code

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://www.servicenow.com/docs/access?context=card-operations-reference&family=xanadu&ft:locale=en-US)**

The domain value description for the **DisputeResponseReason** column has been updated from **Copy of ATM Cash Disbursement or Load Transaction** to **Copy of ATM Cash Disbursement**.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://www.servicenow.com/docs/access?context=card-operations-reference&family=yokohama&ft:locale=en-US)**

Updated the following columns to align with release 25.1 revision changes:

    -   The **is\_parcelado** column has been removed from the dispute intake table.
    -   The domain value description for the **DisputeResponseReason** column has been updated from **Copy of ATM Cash Disbursement or Load Transaction** to **Copy of ATM Cash Disbursement**.

</td></tr><tr><td>

Zurich

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


 -   **[Workflow](https://www.servicenow.com/docs/access?context=dispute-management-workflows&family=zurich&ft:locale=en-US)**

Track the progress of the investigation workflow intuitively with a redesigned user interface that presents each transaction within a dispute case using a clear, process-based layout. This new layout visualizes the distinct stages of the investigation workflow, Investigate, Chargeback, and Closure, which enhances visibility and dispute management efficiency.


</td></tr><tr><td>

Australia

</td><td>

-   **[Visa dispute management on the one-pager workspace](https://www.servicenow.com/docs/access?context=work-on-a-dispute-case-integrated-with-visa&family=australia&ft:locale=en-US)**

All Visa dispute tasks across the investigation, collaboration, and allocation stages are available in a single-page workspace, replacing the previous playbook-based experience. Dispute agents can view associated transactions from the Visa network directly on the task form and access the pre-arbitration questionnaire inline, with status tracking.

-   **[Updated dispute intake questionnaire for July Store release](https://www.servicenow.com/docs/access?context=installed-with-card-operations&family=australia&ft:locale=en-US)**

New questions have been added to the dispute intake questionnaire to support updated Mastercard chargeback ineligibility rule assessment.

    -   For Goods or Services Not Provided disputes \(RC 4853\): Dispute agents must select the applicable waiver and insurance status for merchandise delivery. Options are: a liability waiver was signed by the buyer; shipment insurance was declined by the buyer; both a liability waiver was signed and shipment insurance was declined; or neither applied. This question is mandatory for dispute agents and is also displayed to cardholders.
    -   For Authorization disputes \(RC 4808\): Dispute agents must identify the current account status. Options include: account closed; suspended or restricted; fraud or compromise; credit-related issue; or account active and in good standing. This question is specific to Mastercard and is not displayed to cardholders.
The following additional changes have been made to existing questionnaire questions in this release:

    -   The **What is the dispute about?** question choice list has been updated: the Multiple Authorization Requests option has been removed from the RC 4808 Authorization list, and Late Presentment has been removed from the RC 4834 Processing Errors list. The following labels have been updated: CAT 3 Devices \(formerly Cardholder-Activated Terminal\); Transit First Ride Risk \(FRR\) and Transit First Ride Issuer Liability \(FRIL\) claims; Installment Billing Dispute-Participating Countries; Cardholder Dispute-Not Elsewhere Classified-United States Domestic \(new\).
    -   Display conditions have been updated for several existing RC 4853 Cardholder Disputes questions — including merchandise return date, date the cardholder first notified the issuer, and whether previous negotiation with the merchant occurred — to reflect the addition of the Cardholder Dispute-Not Elsewhere Classified- United States Domestic sub-category.
    -   For Refund Not Processed disputes \(RC 4853\): The question asking for the date the cardholder first notified the issuer of the dispute is displayed when the credit voucher or transaction receipt is not dated. This question applies to dispute agents only.

</td></tr><tr><td>

Brazil

</td><td>

-   **Price-discrepancy question for Visa consumer disputes**

An existing question, originally used under the Processing Errors dispute category, has been repurposed for consumer disputes filed under reason code 13.3 \(Not as Described or Defective Merchandise/Services\). Dispute agents are asked "Is the dispute due to the difference between the quoted price and the actual charges made by the merchant?" and cardholders are asked "Is the dispute related to a discrepancy between the quoted price and the actual charges made by the merchant?" A Yes answer marks the dispute ineligible for reason code 13.3, since a price discrepancy is not a valid basis for that reason code under the Visa Chargeback Guide.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Financial Services Card Operations features or functionality were removed.

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

Between your current release family and Brazil, some Financial Services Card Operations features or functionality were deprecated.

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

</td></tr><tr><td>

Brazil

</td><td>

-   **Now LLM Service deprecation notice**

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


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

Install Financial Services Card Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   **Activation information**

Install Financial Services Card Operations by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

**Important:** Financial Services Card Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Financial Services Card Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Financial Services Card Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).


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

 See [Financial Services Card Operations](https://www.servicenow.com/docs/access?context=card-ops-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Resolve friendly fraud disputes by incorporating friendly fraud detection and resolution in the existing dispute flow for Visa transactions. You can take actions such as crediting the customer, denying the dispute, or initiating an exception process.
-   The Financial Services Card Operations data model is updated in this release with reparented tables to align the data and manage the dispute transactions more effectively. See [Card Operations](https://www.servicenow.com/docs/access?context=card-ops-landing-page&family=yokohama&ft:locale=en-US) for more information.
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

 See [Workflow](https://www.servicenow.com/docs/access?context=dispute-management-workflows&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Work on Visa dispute transactions and associated transactions from a unified **Dispute Workspace** for all active transactions.
-   Streamline dispute document submission to Mastercard with the document attachment and validation enhancement.
-   Improve dispute resolution accuracy with updated internal policy rules that evaluate the dispute amount rather than the original transaction amount.

 See [Card Operations](https://www.servicenow.com/docs/access?context=card-ops-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Manage credit card openings and closings on one platform.
-   Simplify credit card blocking and credit ​limit processes.
-   Enable agents to create and manage dispute cases for both personal and business, debit and credit card accounts, and ACH dispute cases.
-   Enhanced user experience through guided workflows and real-time visibility.

 See [Card Operations](https://www.servicenow.com/docs/access?context=card-ops-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)


---
title: Combined Financial Services Card Operations release notes for upgrades from Yokohama to Brazil
description: Consolidated page of all release notes for Financial Services Card Operations from Yokohama to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-brazil/brazil-yokohama-financialservicescardoperations-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined Financial Services Card Operations release notes for upgrades from Yokohama to Brazil

Consolidated page of all release notes for Financial Services Card Operations from Yokohama to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Financial Services Card Operations release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Financial Services Card Operations to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Yokohama

</td><td>

-   **[Detect friendly fraud](https://www.servicenow.com/docs/access?context=resolve-friendly-fraud&family=yokohama&ft:locale=en-US)**

Resolve friendly fraud disputes with predefined rules to ensure consistent and precise detection of friendly fraud in Visa disputed transactions. Agents can decline requests, issue credits, or proceed with chargebacks, allowing for tailored responses based on the situation.


 -   **[Enhanced Visa disputes playbook](https://www.servicenow.com/docs/access?context=managing-card-disputes&family=yokohama&ft:locale=en-US)**

Leverage an updated card disputes processing flow to associate additional transactions, manage multiple transaction disputes, and handle pre-arbitration, arbitration, and appeal requests to Visa for allocation and collaboration chargeback workflows.


</td></tr><tr><td>

Zurich

</td><td>

-   **[ACH disputes workflow](https://www.servicenow.com/docs/access?context=work-dispute-ach&family=zurich&ft:locale=en-US)**

Resolve ACH disputes faster with a guided, end-to-end workflow that unifies intake, investigation, and resolution—built on a framework ready for any non-card transaction. The unified intake now features a new dispute reason framework for accurate regulatory mapping and embedded WSUD signature collection for seamless authorization capture. The overall workflow centralizes data, applies real-time regulatory checks, and surfaces next best actions to reduce manual effort and speed decisioning, all on a modular design that can scale to additional non-card dispute types.


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

Yokohama

</td><td>

-   **[Visa Resolve Online \(VROL\) version 25.1 updates](https://www.servicenow.com/docs/access?context=card-operations-reference&family=yokohama&ft:locale=en-US)**

Updated the following columns to align with release 25.1 revision changes:

    -   The **is\_parcelado** column has been removed from the dispute intake table.
    -   The domain value description for the **DisputeResponseReason** column has been updated from **Copy of ATM Cash Disbursement or Load Transaction** to **Copy of ATM Cash Disbursement**.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Updated dispute intake questionnaire for July Store release](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

New questions have been added to the dispute intake questionnaire to support updated Mastercard chargeback ineligibility rule assessment.

    -   For Goods or Services Not Provided disputes \(RC 4853\): Dispute agents must select the applicable waiver and insurance status for merchandise delivery. Options are: a liability waiver was signed by the buyer; shipment insurance was declined by the buyer; both a liability waiver was signed and shipment insurance was declined; or neither applied. This question is mandatory for dispute agents and is also displayed to cardholders.
    -   For Authorization disputes \(RC 4808\): Dispute agents must identify the current account status. Options include: account closed; suspended or restricted; fraud or compromise; credit-related issue; or account active and in good standing. This question is specific to Mastercard and is not displayed to cardholders.
The following additional changes have been made to existing questionnaire questions in this release:

    -   The **What is the dispute about?** question choice list has been updated: the Multiple Authorization Requests option has been removed from the RC 4808 Authorization list, and Late Presentment has been removed from the RC 4834 Processing Errors list. The following labels have been updated: CAT 3 Devices \(formerly Cardholder-Activated Terminal\); Transit First Ride Risk \(FRR\) and Transit First Ride Issuer Liability \(FRIL\) claims; Installment Billing Dispute-Participating Countries; Cardholder Dispute-Not Elsewhere Classified-United States Domestic \(new\).
    -   Display conditions have been updated for several existing RC 4853 Cardholder Disputes questions — including merchandise return date, date the cardholder first notified the issuer, and whether previous negotiation with the merchant occurred — to reflect the addition of the Cardholder Dispute-Not Elsewhere Classified- United States Domestic sub-category.
    -   For Refund Not Processed disputes \(RC 4853\): The question asking for the date the cardholder first notified the issuer of the dispute is displayed when the credit voucher or transaction receipt is not dated. This question applies to dispute agents only.

 -   **[Updated chargeback eligibility questionnaire for May Store release](https://www.servicenow.com/docs/access?context=dispute-rules-content-pack-for-mastercard-landing-page&family=zurich&ft:locale=en-US)**

New Mastercard-specific questions have been added to the chargeback eligibility questionnaire.

For Authorization disputes \(all RC 4808 sub-categories\): A new mandatory certification statement appears in the dispute information section. It displays after the dispute amount modification reason field. Dispute agents must confirm that authorization was required for the transaction but was not properly obtained before an Authorization chargeback can proceed.

For Consumer Dispute RC 4853 Failed Travel Merchant: Two new questions support the bond or insurance scheme reimbursement requirement:

    -   When a bond or insurance scheme exists, agents are asked what response was received from the bonding authority or insurance scheme when reimbursement was requested.
    -   When no response has been received, agents are asked to provide the date on which the reimbursement request was submitted.
Questionnaire questions were updated including RC 4853 Failed Travel Merchant – Intra-EEA and Domestic European Transactions Only as an additional display condition.


 -   **[Resolving disputes with Mastercard](https://www.servicenow.com/docs/access?context=work-on-disputes-integrated-with-mc&family=zurich&ft:locale=en-US)**

Integrate the Dispute Management workflow with subflows that communicate with Mastercom, supporting an end-to-end dispute life-cycle from raising an initial dispute to final resolution.

-   **[Unified dispute intake experience](https://www.servicenow.com/docs/access?context=dispute-intake-overview&family=zurich&ft:locale=en-US)**

The dispute intake process has been streamlined to provide a clear, intuitive experience for customers and dispute agents, resulting in faster resolution and reduced manual effort. A unified interface now allows cardholders, account holders, and agents to raise disputes for both card and non-card \(ACH\) transactions seamlessly.


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

 -   **[Internal policy rule evaluation using dispute amount](https://www.servicenow.com/docs/access?context=dispute-decision-tables&family=australia&ft:locale=en-US)**

Internal policy rules in the **Card dispute rules for internal policy** decision table now evaluate using the dispute amount instead of the original transaction amount. Previously, if a cardholder or agent modified the disputed amount while answering additional transactional questions during intake, policy rules still evaluated against the original transaction value. Rules now use the dispute amount field \(**sn\_bom\_credit\_card\_disputes\_transaction.dispute\_amount**\), so any amount adjustments made during intake are correctly reflected in rule outcomes.


 -   **[Updated chargeback eligibility questionnaire for May Store release](https://www.servicenow.com/docs/access?context=installed-with-card-operations&family=australia&ft:locale=en-US)**

New Mastercard-specific questions have been added to the chargeback eligibility questionnaire.

For Authorization disputes \(all RC 4808 sub-categories\): A new mandatory certification statement appears in the dispute information section. It displays after the dispute amount modification reason field. Dispute agents must confirm that authorization was required for the transaction but was not properly obtained before an Authorization chargeback can proceed.

For Consumer Dispute RC 4853 Failed Travel Merchant: Two new questions support the bond or insurance scheme reimbursement requirement:

    -   When a bond or insurance scheme exists, agents are asked what response was received from the bonding authority or insurance scheme when reimbursement was requested.
    -   When no response has been received, agents are asked to provide the date on which the reimbursement request was submitted.
Questionnaire questions were updated including RC 4853 Failed Travel Merchant – Intra-EEA and Domestic European Transactions Only as an additional display condition.


 -   **[Automated document submission in Mastercard transaction dispute process](https://www.servicenow.com/docs/access?context=chargeback-stage-mastercard&family=australia&ft:locale=en-US)**

Streamline the submission of supporting documents to Mastercard in the Mastercard Dispute Management workflow through document attachment and validation. Attached files are automatically checked against Mastercard requirements for file type and size. This update reduces the need for manual intervention, minimizes rework, and helps avoid rejection risk.

-   **[New subflow and action to support Card data security](https://www.servicenow.com/docs/access?context=card-data-security&family=australia&ft:locale=en-US)**

Support attaching documents to a specified table record using the following subflow and action in Card data security:

    -   Attach Document to Table Record
    -   Attach Tokenized Document to Table Record

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

Yokohama

</td><td>

-   **Activation information**

Install Financial Services Card Operations by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


**Important:** Financial Services Card Operations is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Zurich

</td><td>

**Important:** Financial Services Card Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Financial Services Card Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Financial Services Card Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-yokohama-brazil/rn-combined-intro.md)


---
title: Financial Services Card Operations release notes
description: The ServiceNow Financial Services Card Operations application enables dispute agents to expedite dispute resolutions by providing the required data and improve the overall experience. Financial Services Card Operations was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Financial Services Card Operations release notes

The ServiceNow® Financial Services Card Operations application enables dispute agents to expedite dispute resolutions by providing the required data and improve the overall experience. Financial Services Card Operations was enhanced and updated in the Australia release.

## Financial Services Card Operations highlights for the Australia release

-   Work on Visa dispute transactions and associated transactions from a unified**Dispute Workspace** for all active transactions.
-   Streamline dispute document submission to Mastercard with the document attachment and validation enhancement.
-   Improve dispute resolution accuracy with updated internal policy rules that evaluate the dispute amount rather than the original transaction amount.

See [Financial Services Card Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/card-ops-landing-page.md) for more information.

**Important:** Financial Services Card Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Changed in this release

-   **[Automated document submission in Mastercard transaction dispute process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/chargeback-stage-mastercard.md)**

    Streamline the submission of supporting documents to Mastercard in the Mastercard Dispute Management workflow through document attachment and validation. Attached files are automatically checked against Mastercard requirements for file type and size. This update reduces the need for manual intervention, minimizes rework, and helps avoid rejection risk.

-   **[New subflow and action to support Card data security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/card-data-security.md)**

    Support attaching documents to a specified table record using the following subflow and action in Card data security:

    -   Attach Document to Table Record
    -   Attach Tokenized Document to Table Record
-   **[Updated chargeback eligibility questionnaire for May Store release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/installed-with-card-operations.md)**

    New Mastercard-specific questions have been added to the chargeback eligibility questionnaire.

    For Authorization disputes \(all RC 4808 sub-categories\): A new mandatory certification statement appears in the dispute information section. It displays after the dispute amount modification reason field. Dispute agents must confirm that authorization was required for the transaction but was not properly obtained before an Authorization chargeback can proceed.

    For Consumer Dispute RC 4853 Failed Travel Merchant: Two new questions support the bond or insurance scheme reimbursement requirement:

    -   When a bond or insurance scheme exists, agents are asked what response was received from the bonding authority or insurance scheme when reimbursement was requested.
    -   When no response has been received, agents are asked to provide the date on which the reimbursement request was submitted.
    Questionnaire questions were updated including RC 4853 Failed Travel Merchant – Intra-EEA and Domestic European Transactions Only as an additional display condition.

-   **[Internal policy rule evaluation using dispute amount](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-decision-tables.md)**

    Internal policy rules in the **Card dispute rules for internal policy** decision table now evaluate using the dispute amount instead of the original transaction amount. Previously, if a cardholder or agent modified the disputed amount while answering additional transactional questions during intake, policy rules still evaluated against the original transaction value. Rules now use the dispute amount field \(**sn\_bom\_credit\_card\_disputes\_transaction.dispute\_amount**\), so any amount adjustments made during intake are correctly reflected in rule outcomes.

-   **[Visa dispute management on the one-pager workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/work-on-a-dispute-case-integrated-with-visa.md)**

    All Visa dispute tasks across the investigation, collaboration, and allocation stages are available in a single-page workspace, replacing the previous playbook-based experience. Dispute agents can view associated transactions from the Visa network directly on the task form and access the pre-arbitration questionnaire inline, with status tracking.

-   **[Updated dispute intake questionnaire for July Store release](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/installed-with-card-operations.md)**

    New questions have been added to the dispute intake questionnaire to support updated Mastercard chargeback ineligibility rule assessment.

    -   For Goods or Services Not Provided disputes \(RC 4853\): Dispute agents must select the applicable waiver and insurance status for merchandise delivery. Options are: a liability waiver was signed by the buyer; shipment insurance was declined by the buyer; both a liability waiver was signed and shipment insurance was declined; or neither applied. This question is mandatory for dispute agents and is also displayed to cardholders.
    -   For Authorization disputes \(RC 4808\): Dispute agents must identify the current account status. Options include: account closed; suspended or restricted; fraud or compromise; credit-related issue; or account active and in good standing. This question is specific to Mastercard and is not displayed to cardholders.
    The following additional changes have been made to existing questionnaire questions in this release:

    -   The **What is the dispute about?** question choice list has been updated: the Multiple Authorization Requests option has been removed from the RC 4808 Authorization list, and Late Presentment has been removed from the RC 4834 Processing Errors list. The following labels have been updated: CAT 3 Devices \(formerly Cardholder-Activated Terminal\); Transit First Ride Risk \(FRR\) and Transit First Ride Issuer Liability \(FRIL\) claims; Installment Billing Dispute-Participating Countries; Cardholder Dispute-Not Elsewhere Classified-United States Domestic \(new\).
    -   Display conditions have been updated for several existing RC 4853 Cardholder Disputes questions — including merchandise return date, date the cardholder first notified the issuer, and whether previous negotiation with the merchant occurred — to reflect the addition of the Cardholder Dispute-Not Elsewhere Classified- United States Domestic sub-category.
    -   For Refund Not Processed disputes \(RC 4853\): The question asking for the date the cardholder first notified the issuer of the dispute is displayed when the credit voucher or transaction receipt is not dated. This question applies to dispute agents only.

## Activation information

Install Financial Services Card Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Financial Services Operations Integration with Mastercard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services-operations-integration-with-mastercard-landing-page.md)**

    The ServiceNow® Financial Services Operations Integration with Mastercard application enables financial institutions to manage the complete Mastercard dispute process from start to closure, including automated document submission.

-   **[Card Data Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/card-data-security.md)**

    Card data security provides a tokenizer service to tokenize and detokenize data for Dispute Cases and Dispute Transactions to meet Payment Card Industry \(PCI\) requirements.

-   **[Financial Services Operations Integration with Visa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services-operations-integration-with-visa-landing-page.md)**

    The ServiceNow® Financial Services Operations Integration with Visa application enables financial institutions to integrate with the Visa network for card dispute processing, including the subflows that retrieve associated transactions and submit the pre-arbitration questionnaire in the dispute workspace.


**Parent Topic:**[Financial Services Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/financial-services-operations-rn-landing.md)

